# Standard Rollup Charter
---
# Introduction
The Standard Rollup is the Optimism Collective’s flagship, high-security blockspace product. The Standard Rollup targets the Collective’s highest bar for security, uptime, and decentralization.

This Charter applies the principles of the [Law of Chains](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Law%20of%20Chains.md) to the specific context of Standard Rollups, and does not modify or supersede the Law of Chains in any way.  All conflicts between this Charter and the provisions of Law of Chains will be resolved in favor of the Law of Chains.

Optimism Governance is responsible for upholding the standards and policies outlined in this Charter and ensuring their consistency with the Law of Chains.  All potential changes to the Standard Rollup should be treated with careful consideration by the governance community, to enable long-term, sustainable ecosystems to be built around Standard Rollup blockspace with confidence. 


# Criteria

The criteria for being a Standard Rollup consist of:

* A set of deterministic **onchain criteria** to ensure that chains are well-configured, on an up-to-date version, and have authorized the Optimism Security Council to perform upgrades.
* A set of lightweight, **offchain criteria** checked by the Optimism Foundation, which are expected to carry on until they are ready to be safely transitioned to Optimism Governance.
* Completion of a “**history integrity check**” by the Optimism Foundation, which is expected to be deprecated in the future (as chains deploy directly as Standard Rollups from day 1).

## Onchain Criteria

The onchain criteria for Standard Rollups consist of two components: a **version check** and a **configuration check**.

### Version Validation
The most important onchain criteria is that a chain be on a standard, governance-approved release of the OP Stack. This check is performed by comparing all bytecode for the chain’s L1 smart contracts to the standard bytecode corresponding to a governance-approved release of the OP Stack.

Version validation is a strict, critical requirement. To securely hand over upgradability to the Collective, a chain’s L1 smart contracts must be deployed by the canonical OP Contracts Manager ("OPCM") address as identified in [this link](todo-commit-permalink). This is an automated L1 deployment contract which deploys chains based on `op-contracts@v1.8.0-rc.3`.

For those interested, the code currently used in the Superchain Registry to perform version (and configuration) checks can be found [here](todo-update-validation-link). These checks generate a simple-to-read "report" ([example](todo-green-link)) for easy validation. The Optimism Foundation may, from time to time, update this code (e.g. for quality-of-life improvements or other refactors), **requirement that these contracts were deployed by OPCM at the canonical address above, which is subject to Governance approval**.

#### "Legacy" chain grace period

The OPCM is a relatively new tool, and "legacy" chains (i.e. chains deployed prior to or near its release) may not have used it during deployment despite best efforts to meet the Onchain Criteria. As such, chains merged into the Superchain Registry before March 1, 2025 still satisfy these Version Criteria, so long as their L1 contracts are functionally equivalent to what the OPCM would create for a new deployment. The Foundation may grant an exception to this policy for administrative convenience.

### Configuration Check
Beyond being on a standard version of the OP Stack, all configuration values for the chain must be within high-security, well-tested bounds, and all administrative roles must be  set correctly. There are two main components:
* **Parameter Configuration**: A set of requirements for the “protocol parameters” of a chain — things like block time, gas metering, fault proof configuration, and other low-level variables — to either equal a certain value, or fall within a specified range. The specific requirements can be found [here](https://github.com/ethereum-optimism/superchain-registry/blob/9095778d45a5066649890ee838f87b27062a0d4d/validation/standard/standard-config-params-mainnet.toml).
* **Role Configuration**: A set of requirements for the privileged administrative roles for the chain. The specific requirements can be found [here](https://github.com/ethereum-optimism/superchain-registry/blob/9095778d45a5066649890ee838f87b27062a0d4d/validation/standard/standard-config-roles-mainnet.toml). Primarily, these checks involve ensuring that the Security Council holds authorization to perform upgrades, and other minor Stage 1 requirements (see [here](https://gov.optimism.io/t/final-protocol-upgrade-8-guardian-security-council-threshold-and-l2-proxyadmin-ownership-changes-for-stage-1-decentralization/8157)).
* **Prestate Configuration**: The pre-state is a single onchain hash which commits to the State Transition Function used to credit withdrawals from the bridge. Chains' L1 smart contracts must use a valid prestate hash which corresponds to the standard node software used to sync the chain. This list is maintained [here](todo-prestate-link), according to the rules below.

A more human-readable breakdown of these requirements, including supporting rationale choices, can be found in the[ configurability page](https://specs.optimism.io/protocol/configurability.html) of the OP Stack docs. However, the ultimate source of truth for configuration requirements are the two TOML files linked above, as modified from time to time by Optimism Governance.

The Optimism Foundation may, from time to time, update the[ validation code](https://github.com/ethereum-optimism/superchain-registry/blob/main/validation/validation_test.go) used in the Superchain Registry to perform these checks, **so long as it does not violate the semantic interpretation of the above TOML files, which are subject to Governance approval.**

The Optimism Foundation may, from time to time, add additional permitted prestates to the array in the TOML linked above, **so long as it is a valid output of the [`make reproducible-prestate`](https://github.com/ethereum-optimism/optimism/blob/develop/Makefile#L133) command, made to consume a Chain Config which otherwise passes the rest of the Criteria in this document.**

#### Role Configuration Exceptions
Certain chains’ `L1ProxyAdmin` role shall satisfy the Standard Rollup Criteria, without the default address `0x5a0Aae59D09fccBdDb6C6CcEB07B7279367C3d2A`, so long as that role is a 3/3 gnosis SAFE between the Chain Governor, Optimism Foundation, and Security Council. These chains are:

1. Base
2. Unichain

These Chain Governors have publicly committed to using their upgrade key consistent with the “[Normal Operation](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Security%20Council%20Charter%20v0.1.md#normal-operation:~:text=of%20key%20holders.-,Normal%20Operation,-During%20normal%20operation)” and “[Emergency Response](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Security%20Council%20Charter%20v0.1.md#normal-operation:~:text=Collective%E2%80%99s%20governance%20calendar.-,Emergency%20Response,-The%20Security%20Council)” sections of the Security Council Charter.

While not currently anticipated, the Optimism Foundation may propose expansions of this list from time to time, subject to governance approval via the Protocol Upgrade process.

#### Note on un-announced chains
Some Chain Governors have expressed a desire to deploy their chains in advance of a full public rollout and formally publicizing their information to the Superchain Registry. For the avoidance of doubt, this Charter permits the Security Council and Optimism Foundation to take governance-approved actions for such chains, so long as 1) the chain passes all Onchain Criteria above, and 2) the Optimism Foundation provides indication to the Security Council that the chain passes all Offchain Criteria and intends to merge it into the Superchain Registry once publicized.

## Offchain Criteria

In addition to the above deterministic criteria, the Optimism Foundation may perform a limited set of manual, offchain checks at its discretion before inclusion as a Standard Rollup. These checks include:

1. **ChainID check**: ensuring that the Chain ID is unique and does not collide with a pre-existing EVM chain.
2. **Gas Limit check**: ensuring that the Chain's initial GasLimit is configured to a reasonable value based on the then-current status of OP Stack performance testing. (See below for additional context on Gas Limit policy.)
3. **Security Monitoring**: ensuring certain standard monitoring tools have been deployed for every chain.
4. **Governor/Servicer verification**: verifying at the social layer that the chain is indeed deployed and operated by the parties in question, and are not being impersonated.
5. **Other checks**: running other checks (e.g. compliance-related checks) as deemed appropriate.

Given the fundamentally subjective nature of these checks, they are expected to be administered by the Foundation until they can be safely transitioned to Governance.

## History Integrity Checks
The Optimism Foundation has implemented a suite of history integrity checks, which can be used to identify historical discrepancies between chains and manually assess their impact. The Optimism Foundation will assess these discrepancies on an as-needed basis. If it believes that these discrepancies risk violating the Law of Chains (e.g., User Protections) in the future once the chain is added as a Standard Rollup, it will deny the chain’s inclusion, even if all other criteria in this document are met.

The importance of history integrity checks should quickly diminish over time towards deprecation, since the expectation is that all Standard Rollups launched after the ratification of this Charter are deployed correctly at launch. 

For more information on the motivation for history integrity checks, see [this post](https://gov.optimism.io/t/9067).

### Note on Superchain Registry
The "promotion” of a chain (i.e. setting its `superchain_level` to `1`) in the `superchain-registry` repo will be the canonical indicator of passing the offchain criteria and history integrity checks. Thus, the community can determine whether a given chain falls under the scope of this Charter by checking that:

* The Chain passes all Onchain Criteria checks
* The Chain has been included by the Foundation in the `superchain-registry` repo.

Even after history integrity checks are deprecated, it should be expected that the Foundation’s subjective checks are also either eliminated, or transitioned to a process run directly by the community, so that inclusion may be determined purely by onchain data.

# Governing Policies

The Standard Rollup’s governing policies implement additional “reactive” procedures in the event that one or more stakeholder protections in the Law of Chains are violated in such a way that the protocol cannot naturally handle them. Each of these governing policies include reference to a specific protection in the Law of Chains. 

As such, these governing policies are applications of the existing principles of the Law of Chains. Subject to the provisions of the Law of Chains, these policies are intended to establish predictable enforcement paths for an illustrative (but not exhaustive) list of potential violations of that document.

In its current form, all governing policies’ relevant enforcement actions would be taken by the `L1ProxyAdmin` role, which is held by the Phase 0 Security Council, a 2/2 shared by the Foundation and the Optimism Governance-approved Council (or in the case of the chains listed in “Onchain Criteria–Role Configuration Exceptions” above, a 3/3 with the Phase 0 Council plus the Chain Governor). As such, all enforcement actions are expected to follow the standard Protocol Upgrade vote procedure, which is the existing path used for governance to exercise the `L1ProxyAdmin` role. In the future, policies may include different enforcement mechanisms (e.g. via unilateral action by other councils, or via direct onchain governor outcomes given explicit authority in the protocol.)

### Governor Key Recovery

In the current version of the OP Stack, the `SystemConfigOwner` is permitted to change certain chain configuration values. According to the Law of Chains, control of some of these values are afforded to the Chain Governor (e.g. transaction fee margin), and others are afforded to the Chain Servicer (e.g. the batcher hotkey).

For convenience, the Configuration Check in the above criteria permits either the Chain Servicer or the Chain Governor to be the `SystemConfigOwner`, so that Chain Governors can delegate all configuration updates to Servicers. However, because the Chain Governor is also protected by the Law of Chains to[ be able to switch between Chain Servicers](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Law%20of%20Chains.md#:~:text=This%20should%20include%20the%20ability%20for%20the%20Chain%20Governor%20to%20change%20the%20Sequencer%20on%20its%20OP%20Chain), ultimate control of the `SystemConfigOwner` role should belong to the Chain Governor.

In the event that a Chain Servicer stops fulfilling the wishes of the Chain Governor for those values which the Law of Chains states they should be able to control, or refuses to transfer control of the `SystemConfigOwner` role in the event that the Chain Governor desires to switch to a different servicer, then the Chain Governor may submit a vote to Optimism Governance to have the Security Council recover the role to an account they control.

### Sequencer Censorship
In the event that a sequencer is determined to be maliciously censoring valid user transactions, or experiencing unreasonable downtime impacting applications on the chain, they are violating the User Protection of[ Security, Uptime, and Liveness](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Law%20of%20Chains.md#:~:text=a%20timely%20manner.-,Security%2C%20Uptime%2C%20and%20Liveness,-%3A%20Block%20production) in the Law of Chains.

In the event that a Chain Governor refuses to change its sequencer in reaction (after it has clearly been put on notice of the violation), the community may submit a vote to Optimism Governance to remove the Chain Governor as the `SystemConfigOwner` and appoint a new non-censoring sequencer.

### Responsible GasLimits
The OP Stack is rapidly evolving and the boundaries of its performance continue to be pushed. As such, the protocol currently does not implement a hardcoded upper bound on the Gas Limit for a chain. However, this ability must be responsibly exercised to ensure [fulfillment of User Protections](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Law%20of%20Chains.md#:~:text=Frequently%20experiences%20unreasonable%20downtime%2C%20such%20that%20User%20access%20to%20the%20OP%20Chain%20is%20regularly%20degraded.). Thus:

* Before any GasLimit increase, Chain Governors should submit to the community a public load test which demonstrates stability at that limit.
* After any GasLimit increase, if the chain experiences a significant degradation in performance or stability, the GasLimit should promptly be lowered back to its previous value.

If a Chain Governor fails to take these steps, the community may submit a vote to Optimism Governance to remove the Chain Governor as the `SystemConfigOwner` and lower the GasLimit.

### Responsible Batch Submission
The current version of the OP Stack allows for batches to be submitted with up to a 12 hour delay after initial reception by the sequencer (the “sequencing window”). However, Sequencers are expected to submit at least twice as frequently (i.e. every 6 hours). This affords sufficient time to batch submit in the case of failures or downtime, fulfilling the User Protection to[ Security, Uptime, and Liveness](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Law%20of%20Chains.md#:~:text=a%20timely%20manner.-,Security%2C%20Uptime%2C%20and%20Liveness,-%3A%20Block%20production).

In the event that a Chain Governor refuses (after it has clearly been put on notice of the violation) to change its sequencer which repeatedly and intentionally violates this practice, the community may submit a vote to Optimism Governance to remove the Chain Governor as the `SystemConfigOwner` and appoint a new compliant sequencer.

### Fee Margins
The Law of Chains affords Chain Governors the ability to set fee margins for the chain. However, setting the fee margin significantly high can be a form of economic censorship — by making transactions prohibitively expensive to submit, the Governor could [effectively violate the User Protection to censorship resistance](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Law%20of%20Chains.md#:~:text=A%20Chain%20Governor%20that%20configures%20the%20OP%20Chain%20in%20such%20a%20way%20that%20Users%20indirectly%20cannot%20transact%20(e.g.%2C%20by%20setting%20a%20prohibitively%20high%20gas%20markup).).

The Standard Rollup should allow a maximum fee margin of 100% (i.e., the average cost of transactions should not exceed twice the cost of batch submission). If a Chain Governor sets the fee margin in excess of this, the community may submit a vote to Optimism Governance to remove the Chain Governor as the `SystemConfigOwner` and lower the Fee Margin.

### ResourceMetering

The `SystemConfigOwner` role is currently able to modify the `ResourceMetering` struct, a low-level set of values which set certain properties of L1→L2 message rules. This is a low-level variable with no reason to be changed outside of a protocol upgrade.

If a `SystemConfigOwner` (either Servicer or Governor) changes this value, the community may submit a vote to Optimism Governance to remove the relevant party and revert the change.

# Precommitments

This section commits to anticipated changes (or lack thereof) for future upgrades to this Charter.  While by no means an exhaustive description of the Standard Rollup’s full future development path, the following commitments are core to the expectations of existing and future Superchain ecosystem participants.  The Collective should endeavor to do everything in its power to ensure the following commitments are actualized, understanding that non-adherence will fundamentally and irrevocably undermine the legitimacy and trustworthiness of Optimism Governance.     

### Collective Fee Take

This Charter specifies a fee split of the greater of 1) 2.5% of transaction fee revenue and 2) 15% of chain profit (fee revenue - L1 submission cost). 

It is extremely important to provide stakeholders in the Collective with a reliable economic model on which they can build sustainable long-term ecosystems. By ratifying this Blockspace Charter, the Collective is signaling its precommitment to **all Standard Rollups** that it will not modify the fee split parameters outlined above until December 31, 2029 (at the earliest).

This does not preclude changes or improvements to the implementation of the fee split contracts, so long as they preserve the original economic spirit. In the event that new sources of fees (or operating costs) are introduced to the protocol, the economics should be updated with minimized impact to the existing expectations and ecosystems in the Superchain.

### Governor/Servicer Role Separation

Some policies above (e.g. Governor Key Recovery) arise from an overloading of the `SystemConfigOwner` role to control configurability options which the Law of Chains affords separately to Governors and Servicers. In a future upgrade (or upgrades), the Collective should transition to a model which establishes independent roles for the Governors and Servicers of Standard Rollups, allowing them to modify the configuration values afforded to them independently. This change should also remove controllability of the Resource Metering Config without a protocol upgrade.

### Ossified GasLimits

Because the OP Stack’s performance is rapidly improving, the onchain GasLimit criteria is bounded above by a significantly higher value (based on the limits of fault provability) than what chains in practice require for stability. The Governing Policy above reflects the fast-paced nature of gas limits today, in which chains frequently increase their gas limits to test stability. However, as the rate of change slows, the Collective should set a more realistic upper bound, which can only be changed via upgrade.

### Direct Fee Margin Controls

Today, the “fee margin” discussed in the relevant Governing Policy above is only indirectly influenceable via the control of multiple other configuration variables. In the future, the Collective should implement a protocol improvement which allows the margin to be set more directly, and which imposes a strict upper bound of 100%, to remove the ability to perform economic censorship even temporarily.
