## Law of Chains v0.1
The Law of Chains is an open neutrality framework that establishes certain protections for participants in the Superchain ecosystem. Its purpose is to promote core principles of user protection, decentralization and economic autonomy as foundations for the developing Superchain.

> Version note. The Law of Chains is a living document, and should evolve alongside protocol innovation across the Collective. Version 0.1 of the Law of Chains is immediately applicable to the current, single-sequencer release of the OP Stack, and establishes fundamental principles: core expectations of users and economic participants, homogenous blockspace, and universal upgrades on a shared standard. Anticipated improvements to the OP Stack that remain technologically unspecified (e.g., shared sequencing and zero-knowledge proofs) are correspondingly economically unspecified in this initial version. As the Law of Chains evolves, two critical freedoms should be preserved: (1) the freedom of Optimism Governance to introduce new protocol constructions with different technological and economic specifications, and (2) the freedom of ecosystem participants to choose, at the appropriate time, with full information, and without coercion, whether to opt into those constructions.

> Finally, part of the Law of Chains is this [Important Disclaimer](https://community.optimism.io/docs/governance/law-of-chains-disclaimer/). To fully understand this document, you must read the disclaimer. It clarifies that the Law of Chains is not a legal contract, provides no legally enforceable warranties, representations, indemnities, rights, or obligations, and does not commit participants to any form of legal partnership or joint venture with any others. The Law of Chains is intended to function solely as a guiding framework for participants in the Collective and Optimism Governance.

**1. Covered Participants.**

  1. The Law of Chains applies to:
     - **Users:** The end users of OP Chain smart contracts and applications, and the developers and deployers of such smart contracts and applications.
       - Any party that holds assets or transacts on an OP Chain or deploys a smart contract to an OP Chain is acting in their capacity as a User.
     - **Chain Governors:** The party or smart contract responsible for deploying an OP Chain or configuring an OP Chain following deployment.
       - A party or smart contract “configures” an OP Chain by setting the configuration values that are parameterized by, but not specifically hardcoded into, the Protocol Contracts or offchain protocol software.
       - For example, in the future a Chain Governor might configure its OP Chain to run a particular OP Stack sequencing scheme (among various potentially compatible sequencing schemes) on the chain.
     - **Chain Servicers:** Sequencers, Proposers, and Challengers for an OP Chain.
  2. The identity or scope of Covered Participants may change over time. For example:
      - A Chain Governor may transition from being a single party to a decentralized governance system (e.g., where OP Chain configuration decisions are made by a ‘DAO’). In that case, the decentralized governance system would become the Chain Governor.
      - With future development milestones, Sequencers, Proposers, and Challengers may become separate categories of Covered Participants with expectations under the Law of Chains that are different from one another.
      - New, currently unidentified roles may emerge within the ecosystem and be included as additional categories of Covered Participants (e.g., zk-Provers).
  3. A single party may be a Covered Participant in multiple capacities. For example, a Chain Governor may also be a Chain Servicer, and a Chain Servicer may be any combination of Sequencer, Proposer, and Challenger. In such cases, the party’s expectations under the Law of Chains are determined separately, as relevant to each respective role.
  4. The Law of Chains only applies to Covered Participants of OP Chains: i.e., those that have affirmatively opted-in, and followed any relevant governance process to be committed to and covered by the Law of Chains. It does not extend to chains running on the OP Stack which are not “OP Chains.”

**2. The Platform.** In addition to Covered Participants, the Law of Chains establishes expectations for the Platform itself. The Platform is not an individual OP Chain; it is the fundamental protocol on which all OP Chains run today, and in the future, which will evolve into the Superchain.

**3. User Protections.** Users are to be protected with assurances that are (a) highly similar to the assurances afforded to analogous users of Ethereum and (b) as uniform as possible for all Users across all OP Chains. This means ensuring, at minimum:

 - **State Transition and Messaging Validity:** OP Chain state transitions, and cross-chain messages sent to or from OP Chains, must only be finalized if they follow the rules defined by the most recent Optimism Governance-approved release of the OP Stack. For example, the User Protection to state transition and messaging validity would be violated by:
   - For Chain Servicers, a:
     - Sequencer that represents an L2 block (e.g., by serving an eth_getBlockByNumber RPC request) to a User where that block does not match the result of the op-geth, op-node, and L1 Ethereum node services.
     - Proposer that proposes an output which does not match the result of the batch-submitter service in coordination with aforementioned software.
     - Challenger that does not challenge the aforementioned proposal in a timely manner.

 -  **Security, Uptime, and Liveness:** Block production, sequencing, and bridging must satisfy uniform standards for security, uptime, and liveness across all OP Chains. For example, the User Protection to security, uptime, and liveness would be violated by:
     - A Chain Servicer that:
       - Illegitimately censors, reorders, or limits transactions (e.g., by running off-chain sequencing code that is not approved by Optimism Governance, or by colluding with L1 validators to artificially inflate sequencer batch submission costs) in order to extract a profit or violate User Protections.
       - Frequently experiences unreasonable downtime, such that User access to the OP Chain is regularly degraded.
       - Does not promptly address emergency bug fixes or other security compromises.
     - A Chain Governor that configures the OP Chain in such a way that Users indirectly cannot transact (e.g., by setting a prohibitively high gas markup).
- **Universal, Governance-Approved Upgrades:** OP Chains must upgrade together under OP Stack releases that are approved by Optimism Governance. Such upgrades must be backwards compatible with prior OP Stack releases such that User Protections are not compromised. For example, the User Protection to universal, governance-approved upgrades would be violated by:
  - A Chain Servicer that facilitates an upgrade of the OP Chain to an Ethereum bridge implementation that is not identical to the implementation shared by all other OP Chains.
  - A Chain Servicer that facilitates a change to the OP Chain’s L2 smart contract execution semantics in a way that breaks previously safe assumptions (e.g., by allowing a timelock contract to unlock ahead of schedule).

For the avoidance of doubt, any unilateral attempts by a Chain Servicer or Chain Governor to migrate an OP Chain to an unapproved release of the OP Stack or to an entirely different technical stack – i.e., a “Unilateral Migration” attempt – would violate the User Protections described above:

  - Changing the rules of the existing OP Chain to the rules of the other stack violates the User Protection to state transition validity.
  - Migrating assets from the existing OP Chain bridge via a non-standard withdrawal violates the User Protection to messaging validity.
  - Migrating funds directly out of the existing OP Chain bridge via an upgrade violates the User Protection to universal, governance-approved upgrades.

This does not mean that a Chain Governor or Chain Servicer should not take any action to move users to a new technical stack. It does mean that there must be a voluntary migration transaction taken on a per-User basis, similar to the historical migration between Uniswap versions on L1.

**4. Chain Governor Protections.** The configuration choices afforded to Chain Governors by releases of the OP Stack are to be preserved according to the following principles:

  - **Economic Autonomy:** Chain Governors may make their own free economic choices in the marketplace within existing OP Stack parameters established by the Platform, so long as those decisions are otherwise consistent with the Law of Chains. Moreover, Chain Governors should not be retroactively deprived of economic reward that resulted from decisions that were valid at the time they were made. For example, the Chain Governor Protection to economic autonomy would be violated by upgrades that:
    - Deny the ability of a Chain Governor to choose to run a single-sequencer OP Stack sequencing scheme (even where governance has approved a release of the OP Stack which supports an alternative sequencing scheme).
    - Deny the ability of a Chain Governor that runs a single-sequencer configuration to set a configurable profit margin for sequencing on its OP Chain.
    - Remove network fee revenue previously accrued to an L2 fee vault by a Chain Governor, or limit the ability of the Chain Governor to legitimately collect additional revenue or access those historical or legacy assets earned and presently owned by them.
    - Introduce mechanisms designed directly to prevent Chain Governors from encouraging a voluntary per-User migration to a different chain (since the possibility of voluntary exit is critical for Users as well as Chain Governors, the ability of a Chain Governor to legitimately exit the system should be respected regardless of Chain Governor conduct).
  - **Technical Configurability:** Chain Governors may make basic technical configurations permitted to them by the OP Stack. This should include the ability for the Chain Governor to change the Sequencer on its OP Chain between those which have been approved by Optimism Governance, and to appoint a new Chain Governor to take its place in the event it elects to make such a transition.

**5. Chain Servicer Protections.** The participatory expectations of Chain Servicers are to be preserved according to the following principles. Like Chain Governor Protections, Chain Servicer Protections are focused on the Chain Servicer’s expectations of economic autonomy and technical configurability within, initially, the framework of an OP Stack single-sequencer sequencing scheme:

   - **Economic Autonomy:** Chain Servicers may make their own free economic choices in the marketplace within existing OP Stack parameters established by the Platform, so long as those decisions are otherwise consistent with the Law of Chains. Moreover, Chain Servicers should not be retroactively deprived of economic reward that resulted from decisions that were valid at the time they were made. For example:
      - If a Chain Governor makes changes to parameters, or Optimism Governance approves an upgrade, which impacts the margin that a Chain Servicer (e.g., in its capacity as Sequencer) may earn going forward, the Chain Servicer may cease operations if economically nonviable under the new margin.
      - If a Chain Servicer has previously accumulated assets to an L2 fee vault contract, it may access those assets and any upgrade removing such assets or access would be a violation.
- **Technical Configurability:** Chain Servicers may make basic technical configurations permitted to them by the OP Stack. This includes changing the hotkey used for batch submission in a Sequencer capacity, or the hotkey used for proposing in a Proposer capacity.

**6. Platform as Commons.** The Platform is the fundamental public good on which all ecosystem participants, as a Collective, rely. It establishes the underlying economics applicable to all OP Chains, backstops the security assumptions of all OP Chains, and exists for the benefit of all OP Chains. On behalf of the entire Collective, therefore, it is essential that its basic Platform Requirements be preserved:

- **Sustainability:** The Platform must be able to economically sustain itself and the public goods that support it.
- **Security:** The Platform must be able to prevent or respond to Security or Stability Incidents that would impact it.
- **Survival:** The Platform must be able to evolve in response to threats that pose a real, existential risk to the Platform as whole.

The Collective should thoroughly consider any claim that a protocol upgrade or modification is necessary or appropriate to preserve a Platform Requirement:

  - Violations of Participant Protections are to be avoided wherever practicable to do so, and minimized, reasonable, and proportionate to the need posed by the Platform Requirement wherever it is not.
     - For example, Platform downtime imposed in connection with protocol upgrades is acceptable (even though it marginally violates a series of Participant Protections for a limited period of time), but wherever practicable, that downtime should be limited, communicated well in advance, and Covered Participants should be provided with substantial time to prepare in a way that minimizes adverse impact.
- A proposed response to one Platform Requirement should always beg the question of what other Platform Requirements could be collaterally undercut in the process.
     - For example, a proposed upgrade may be allegedly justified in the name of the Platform Requirement of survival, while violating the Chain Governor Protection to economic autonomy. But of course, very few projects may launch an OP Chain if the Platform is not a fair, predictable commons on which to build. And less OP Chains on the Platform could undercut the Platform Requirement of sustainability. In that case, the threat to the Platform Requirement of survival should predominate the threat to the Platform Requirement of sustainability in order to justify such a change.

**7. Users First.** Subject to any Platform Requirements, User Protections must not be violated, including by the exercise or enforcement of any other Participant Protections. In the event there is a conflict between different Participant Protections, (a) User Protections will supersede all other Participant Protections and (b) conflicts among other Participant Protections will be resolved in the following order of priority: first, as required by the Platform; second, as necessary or appropriate to ensure the protection of User Protections; and third, in a manner otherwise consistent with the interpretive principles of Section 9 below.

**8. Enforcement.** The Law of Chains is intended to be enforced solely through resolutions of Optimism Governance. Participant Protections are not, should not be relied on as, and do not create legally binding or enforceable rights or obligations independent of any actual, separate legal agreement between independent contracting parties (which the Law of Chains is not).

This means that standing alone, the Law of Chains is fundamentally social in nature: it establishes social expectations for (a) how Covered Participants should conduct themselves, (b) how Optimism Governance can step in to remedy a violation, and (c) how to evaluate future upgrades. For example:

  - If a Sequencer impermissibly censors users, or intentionally represents a faulty state to users, Optimism Governance can intervene by executing an upgrade to replace the Sequencer on all OP Chains it serviced.
  - If an invalid proposal is submitted and a Challenger fails to use a Challenger Key to delete the proposal, Optimism Governance can intervene by executing an upgrade to replace the Challenger.
  - If an upgrade to the OP Stack is proposed, which is insufficiently backwards compatible, Optimism Governance can validly reject the proposal on those grounds.

As Optimism Governance evolves, further accountability and enforcement mechanisms may evolve alongside it.

Finally, for the avoidance of doubt, no Covered Participant is required under the Law of Chains to take actions that it reasonably believes are contrary to applicable law.

**9. Interpretation.**

  1. In interpreting the scope, authority, and meaning of the Law of Chains, the guiding principles contained in the [Working Constitution](https://gov.optimism.io/t/working-constitution-of-the-optimism-collective/) will apply as follows:
     - **Governance minimization.** The OP Stack and OP Chains should be designed, operated, and governed in a manner that progressively and programmatically (a) removes the ability of ecosystem participants to violate the Law of Chains and therefore (b) removes the need for Optimism Governance to proactively enforce it. For example, future releases of the OP Stack should enable:
       - Chain Governors to exercise Chain Governor Protections via (and solely to the extent permitted by) configurable parameters that are encoded and enforced at the Protocol Contract level.
       - Anyone to act as a Proposer permissionlessly, removing the ability of any single Proposer to censor User withdrawals.
       - Anyone to act as a Challenger permissionlessly, removing the need for the Law of Chains to require affirmative conduct by any single Challenger.
       - Fault proof implementations that remove Chain Servicers’ ability to violate the User Protection to state transition validity.
     - **Forking.** The ability to fork and exit the system remains a critical mechanism to protect individual freedoms. However, the prohibition against Unilateral Migrations clarifies that exit by individual Chain Servicers or Chain Governors should not undermine the individual freedom of Users, who should have the option to migrate, rather than being forced into it.
     - **Anti-plutocracy.** Like Optimism Governance as a whole, enforcement of the Law of Chains cannot ultimately be the domain of OP token holders alone; the influence of the Token House must be balanced with Citizenship.
     - **Impact = Profit.** The Superchain ecosystem will, like all digital commons, be impacted by marketplace dynamics. In cases where these dynamics give rise to conflicts for Optimism Governance to resolve, the resolution should strive to preserve Platform Requirements and protect Participant Protections, while interpreting the Law of Chains in a manner that rewards all ecosystem participants commensurate with their Collective contributions.

  2. It is further understood that the Law of Chains will require adaptation to changing circumstances as the Collective defines itself, evolves, and grows iteratively over time. Accordingly, the Law of Chains adopts additional interpretive principles:
     - **Long-term applicability.** As the Law of Chains is applied to events such as the Superchain Migration, which will involve significant and unforeseen changes to protocol specifications and code, it should be interpreted and updated in a way that favors flexibility, adaptability, and consistency with the principles underlying the Law of Chains, as opposed to rigid adherence to its text. For example:

       - Optimism Governance may approve future releases of the OP Stack that cause some of the specific references and examples included in this document to no longer apply. This should not undermine ecosystem participants’ adherence to the Law of Chains’ underlying principles, or inhibit the legitimacy of efforts by Optimism Governance to enforce it.
     - **Modularity and evolution.** The modular design of the OP Stack opens the door for alternate L2 constructions in the future, which may make known tradeoffs (e.g., between decentralization and performance, or between composability and economic autonomy) that establish fundamentally different User expectations. For example:

       - A future L2 construction might move data availability off of L1 to reduce fees, but decrease fundamental censorship resistances properties.
       - A future L2 construction might include a decentralized sequencing network which facilitates cross-OP Chain composability, but decreases the ability of individual OP Chains to have independently configured economic systems.
       The mere fact that such a protocol is less censorship resistant or more uniform in its economic model than a current OP Chain does not mean that Optimism Governance should reject its inclusion in a release of the OP Stack for failure to uphold particular Participant Protections. Instead, Optimism Governance should consider whether, or how, to expand the Law of Chains to facilitate the Superchain’s ongoing evolution.
     - **Reputational awareness.** Optimism Governance must understand that the decisions it makes are never in a vacuum, and the manner in which it applies the Law of Chains will establish its reputation for existing – but also future – ecosystem participants. For example (and as noted above), undermining the settled expectations of Chain Governors will not just impact current participation, it will also pose significant long-term risk of driving away future Chain Governors, and corresponding fee revenue. “The most important scarce resource is legitimacy.”

**10. Always. Stay Optimistic** :red_circle::large_blue_circle::orange_circle::green_circle::yellow_circle::purple_circle::white_circle::brown_circle::sparkles:

### **DEFINITIONS** 

*“Challengers”* = the Ethereum address authorized to delete output proposals for an OP Chain.

*“Collective”* = the [Optimism Collective](https://community.optimism.io/docs/governance/), including participants in the Superchain ecosystem.

*“Covered Participants”* = Users, Chain Governors, and Chain Servicers.

*“OP Chain”* = a production L2 blockchain running on the OP Stack and which has affirmatively opted-in and followed any relevant governance process to be committed to and covered by the Law of Chains.

*“OP Stack”* = an Optimism Governance-approved, standardized, shared, and open-source development stack release that [powers](https://stack.optimism.io/) the Optimism L2 blockchain protocol; together with all future such releases.

*“Optimism Governance”* = the governance system for the OP Stack, OP Mainnet, and the Superchain, which is currently the bicameral system of the [Token House](https://community.optimism.io/docs/governance/#:~:text=%23-,Token%20House,-Governance%20of%20the) and the [Citizens’ House](https://community.optimism.io/docs/governance/#:~:text=%23-,Citizens%27%20House,-The%20Citizens%27%20House); and future iterations thereof.

*“Participant Protections”* = User Protections, Chain Governor Protections, and Chain Servicer Protections, collectively.

*“Proposers”* = the L1 Ethereum wallet or smart contract authorized to append output root hashes for an OP Chain, which form the basis for withdrawals and other L2-to-L1 messages.

*“Protocol Contracts”* = the OP Stack smart contacts that comprise the onchain code that powers an OP Chain.

*“Security or Stability Incident”* = bugs or defects, unplanned maintenance, or stability, integrity, availability, non-repudiation or other security issues with the OP Stack, Protocol Contracts, or any OP Chain.

*“Sequencers”* = the node(s) providing block production services which produces transaction confirmations and state updates, constructs and executes L2 blocks, and submits L2 block data transactions to layer 1.

*“Superchain”* = [a proposed network of L2 rollups](https://app.optimism.io/superchain/) that share bridging, security, data availability, and communication layers; which uses the OP Stack as a common development stack, and Optimism Governance as the common governance system.
