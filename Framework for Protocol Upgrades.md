# Framework for Protocol Upgrades

The threshold for which changes require a governance vote is based on the User Protections clause of the [Law of Chains](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Law%20of%20Chains.md). In summary, these protections are:

1. ********************State Transition and Messaging Validity:******************** OP Chain state transitions or cross-chain messages sent to or from OP Chains must follow the rules of the latest governance-approved release of the OP Stack. This means that changes to the block derivation function or messenger contracts are always subject to a governance vote.
2. **************************Security, Uptime, and Liveness:************************** Block production, sequencing, and bridging must satisfy uniform standards for security, uptime, and liveness across all OP Chains. This means that  changes that could cause users to be unable to transact (e.g., changing the gas limit to something untenable) are subject to a governance vote.
3. **************Universal, Governance-Approved Upgrades:************** OP Chains must upgrade together under OP Stack releases that are approved by governance. Any upgrades that aren’t backwards compatible are therefore subject to a governance vote.

Using this framework, we can define the following rough upgrade types and whether or not each upgrade type needs a governance vote. If you are uncertain if an upgrade requires governance approval, please request delegate feedback on the forum. 

<details>
  <summary>Consensus Changes</summary>

**Vote required:** Yes
    
  Consensus changes modify the state transition function or messaging validity. As such, they must be approved by governance to satisfy protection 1 above. 
    
  For example:

  - Bedrock
  - EIP-4844
  - Shanghai
  - Any L1 upgrade that modifies a contract under the control of the Security Council. The Security Council cannot make any changes to L1 unless they are approved by governance **or** the result of an active or impending security issue.

</details>
<details>
  <summary>Predeploy Updates</summary>
    
  **Vote required:** Yes
    
  Predeploy updates must be approved by governance in order to satisfy protection 3 above. More specifically, changes to predeploys must be rolled out across all OP Chains in order to prevent functionality on one chain from diverging from all the others.
    
</details>
<details>
<summary>Cross-Chain Contracts</summary>
   
**Vote required:** No
    
   “Cross-chain contracts” refers to smart contracts like Gnosis SAFE or `create2deployer` which are deployed at the same address across multiple chains. These contracts do not require a governance vote because anyone can deploy them at any time on any chain. This is true even if we decide to add these contracts to the genesis state, since someone could always deploy them after the chain comes online.
    
   Note that any changes to the `0x42...` namespace **do** need to go through governance, as do any contract deployments that require irregular state transitions.
    
</details>

<details>
<summary>Parameter Updates</summary>

**Vote required:** Change Dependent
    
Parameter updates that impact protections one or two above will need to be approved by governance. For example, setting the gas limit or changing the EIP-1559 parameters will require governance approval since modifying these parameters can prevent users from transacting.
    
Examples:
    
  - Updating gas parameters requires a governance vote until they’re explicitly configurable by the Chain Governor
  - Updating the batcher/proposer addresses (among addresses already on the allowlist) do not require a governance vote as long as they are within the set of governance-approved addresses
</details>

<details>
<summary>Non-Consensus Client Features</summary>      

 **Vote required:** No
    
  Network-wide features introduce functionality that may require coordination with alt-client developers, but without risk of a chain split. As such these changes satisfy all three user protections above as long as they are backwards-compatible and meet our bar for engineering rigor.
    
  Examples:
    
   - Snap sync
</details>

<details>
<summary>Changes Affecting Transaction Inclusion/Ordering</summary>  

  **Vote required:** Yes
    
  Even though the mempool is technically not part of consensus, it affects the way in which transactions get included into the chain and can negatively effect user experience. As a result, unilateral changes that affect transaction ordering violate protection 2 above and therefore need a vote. If the community detects that nonstandard ordering software is being run, it is grounds for removal from the sequencer allowlist.
    
  Examples:
    
   - Moving to a public mempool
   - Running custom PBS/transaction pool software
</details>

<details>
<summary>Non-Consensus, No-Coordination, Non-Ordering Change</summary>  

    
  **Vote required:** No
    
  These changes are a catch-all for any change that doesn’t modify consensus or require coordination. These changes can be rolled out unilaterally without input from governance since they do not impact any of the protections described above.
   </details> 

*Note: The above sets are not always mutually exclusive. If a given change might fall into multiple buckets, if any one of them requires a vote, then the change requires a vote*
