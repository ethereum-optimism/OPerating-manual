

This Charter outlines the structure and responsibilities of the Security Council and its participants. 

The exact number of participants depends upon candidate outreach, which is ongoing. This Charter will be updated with exact participant numbers and signing thresholds according to the change process outlined below before the Security Council is implemented.

# **Security Council Charter v0.1** 

## **Goals**
In short, the goal of the Security Council is to turn admin keys for OP Mainnet, and eventually, all OP Chains in the Superchain, over to a public, decentralized set of individual actors (“participants”) accountable to Optimism Governance. Executed correctly:

- No single party should be able to upgrade the system, modify rollup state, or censor transactions.
- Each participant custodies and uses their key securely.
- During normal operations, the Council simply implements the upgrade and role permission decisions made by Governance, rather than making decisions itself.
- During defined emergency situations, the Security Council is empowered to act without direct Governance approval to keep the network safe and secure.
- Dysfunctional participants, either individually or acting as a quorum, can be effectively checked, without undermining the security advantages motivating the formation of the Council in the first place.
- Finally, a successful Security Council is one whose role is progressively and programmatically reduced over time.

## **Structure**
The structure of the Security Council is designed to satisfy the multisig requirements of Stage 1 decentralization while, wherever practicable, prioritizing safety over liveness.  Security Council participants will be expected to carry out their responsibilities consistent with this Charter and the provisions of the Law of Chains.

### **Council Composition**

The Security Council will operate a Gnosis Safe multisig wallet. The multisig will have a 75% threshold. Each participant will control one key, with the exception of the Council Lead (who is not a key holder).

The Council Lead will coordinate the ongoing operations of the key holding Council participants. The Council Lead’s role is procedural, communicative, and ministerial. It has no ability to influence the substantive signing decisions of key holders.

### **Normal Operation**

During normal operation, the Security Council is intended to act as an oracle for the Optimism Governance process: initiating protocol upgrades and changing role designations (such as designations for the Sequencer, Proposer, and Challenger roles, as well as designating the composition of the participants on the Security Council multisig), solely as directed by Optimism Collective governance outcomes.

Council participants are expected to verify that a proposed protocol upgrade or role designation decision has been approved by Optimism Governance. They are not expected to directly evaluate the “merit” of the accompanying proposed code (e.g., for security purposes).

In typical cases, signing should be scheduled in advance and in accordance with the Collective’s governance calendar.

### **Emergency Response**

The Security Council is permitted to preemptively address actual or anticipated bugs, defects, unplanned maintenance, or stability, integrity, availability, non-repudiation or other security issues with the OP Stack or any OP Chain.

To protect Security Council members, each participant may also take actions they or the Optimism Foundation believes to be necessary to comply with applicable law.

These emergency response measures may be taken without specific Governance approval.

If the Security Council ever utilizes this discretion, however, it should endeavor to provide the community with a prompt and comprehensive retrospective (within the bounds of any legal commitments to, or security requirements for, confidentiality) on the action taken and the rationale for it.

### **Multisig Actions**

The Security Council multisig is responsible for two types of action:

- **Protocol upgrades:** Upgrades to the L1 protocol contracts of an OP Chain.
- **Designation changes:** The designation of the onchain addresses that are authorized to perform the following roles on OP Chains: sequencers (i.e., batchers), proposers, challengers, and membership on the Security Council multisig.
All protocol upgrades, and designation changes for removing a sequencer from the sequencer allowlist, are subject to a delayed upgrade mechanism (see below). All other permission changes are not.

### **Delayed Upgrades**

All protocol upgrades, and the specific designation change that removes a sequencer for the sequencer allowlist, are subject to a 14 day delay period before becoming effective. This delay period applies regardless of whether the corresponding multisig action is first approved by Optimism Governance or implemented preemptively by the Security Council as an emergency response.

During that 14 day period, the Optimism Foundation may veto the upgrade. The Foundation will endeavor to use this veto authority consistent with the “Emergency Response” parameters outlined above and the provisions of the Law of Chains. As with the existence of the Security Council in general, the Foundation’s role in vetoing upgrades should be reduced over time.

### **Challenging** 

In addition to implementing protocol upgrades and role permissioning, the Security Council will initially be authorized to perform the Challenger role (on a 1-of-3 basis) for each OP Chain, along with each OP Chain’s Governor, and Foundation.

In this role, the Council will be responsible for challenging faulty output proposals within the applicable challenge period (currently 7 days) in the event that all other Challengers fail to challenge.

A faulty output proposal is a commitment to an L2 state root by an OP Chain’s proposer that can be independently verified as faulty by an OP Stack node which observes L1 and derives the L2 state from it.

It is expected that various members of the Optimism Collective would call attention to a faulty L2 output proposal. The Security Council participants would then:

1. Run scripts to independently verify that the output is faulty; and

2. Submit and approve a call to delete this output.

The OP Stack includes infrastructure for identifying a faulty output. Security Council participants will not be required to run this infrastructure (although it is encouraged).

The Council’s responsibility to perform a Challenger role is intended to be reduced as multi-client fault proofs are rolled out.

## **Participants**
This section describes the expectations for Security Council participants, including both key holders and the Council Lead.

### **Cohorts and Election Terms**

Security Council participants will serve in two cohorts, subject to recurring, staggered re-election periods. The initial Cohort 1 (at least 50% of the total number of participants) will serve for 12 months. The initial Cohort 2 (the remaining participants) will serve for 18 months. These initial cohorts of Security Council participants will be proposed by the Optimism Foundation, subject to ratification by the Token House.

Six months prior to the expiration of the cohorts’ respective terms, there will be elections to replace or renew the signers in that cohort. All subsequently elected cohorts will serve a 12 month term. Elections are expected to follow the standard election format used for all Councils in the Collective.

Participants are subject to eligibility screening prior to joining the Council and receiving signing authorization on the multisig (see “Participants – Eligibility,” below). There is no limit to the number of terms a Security Council participant may serve.

### **Eligibility**

Participants on the Security Council should be selected in accordance with the following criteria:

- **Technical competency.** Baseline proficiency with the OP Stack and secure key management and signing standards.
- **Reputation.** Known, trusted individuals or entities that have demonstrated consistent alignment with the Optimistic Vision.
- **Geographic diversity.** The number of participants that reside in any country should be less than the quorum required for multisig action. To avoid requiring participants to publicly disclose their physical locations, this requirement will be enforced by the Optimism Foundation as part of the eligibility screening process.
- **Diversity of interests.** No more than 1 participant is associated with a particular entity, or that entity’s employees or affiliates.
- **Alignment.** Participants should not possess conflicts of interest that will regularly impact their ability to make impartial decisions in the performance of their role.

In addition, all participants will be required to pass an eligibility screening process before being added to the Council. This process may include KYC/AML and sanctions screening and a requirement that the member sign a standard contract, which will be implemented at the discretion of the Optimism Foundation.

### **Responsibilities**

Security Council key holding participants will be responsible for developing and complying with procedures to facilitate:

- Communication and coordination among the participants;
- Secure key management;
- Verifying and promptly enacting Optimism Governance-approved upgrades and permission changes;
- Notifying the other participants of, and collaborating in good faith to promptly resolve, defined emergency situations (see “Emergency Response,” above); and
- Proving continued access to keys via periodic liveness checks, where participants must prove they can access their keys within a set time limit.
For security purposes, the details of these procedures should remain private among the Council.

The Council Lead, meanwhile, is responsible for supporting the implementation and operationalization of the aforementioned procedures, including by:

- Alerting key holders of upcoming protocol upgrade or role permissioning proposals going through Governance;
- Managing required timelines;
- Scheduling, setting agendas, and hosting Council meetings and facilitating discussions;
- Monitoring compliance with the procedures;
- Onboarding new Council participants; and
- Communicating with external stakeholders, including Optimism Governance, as to Council operations.
All Security Council participants are expected to perform these responsibilities with the awareness that OP Chains, the OP Stack, the developing Superchain, and the associated products, tools, and documentation are in a rapidly evolving nascent state. To the extent that unforeseeable circumstances or ambiguities arise (including in connection with potential responses to Exception Events), the participants will work in good faith to resolve them consistent with this Charter and the Law of Chains.

Finally, all Security Council participants are also responsible for complying with (i) the Code of Conduct of the Optimism Collective and (ii) any additional, internal conflict of interest procedures that the Council may develop from time to time.

### **Accountability**

The Security Council is accountable to Optimism Governance. The Token House may vote to remove Security Council members at any time for severe violations of the Code of Conduct.

The Security Council can also act unilaterally to remove a participant who fails to satisfy the requirements of this Charter if such failure falls within the defined scope of the Council’s emergency powers (see “Structure – Emergency Response” above).

Governance votes for removal of a Security Council participant for violation of the Code of Conduct will occur before the end of the next voting cycle (a delay of 3 weeks maximum). A contingent vote for their replacement on the Council will run in the same voting cycle.

Security Council members may be removed for failure to satisfy the requirements of this Charter immediately via an Emergency Response. A vote for their replacement on the Council would run in the next nearest voting cycle.

Additionally, if a Security Council key holder fails to prove access to their keys by satisfying the requirements of a scheduled liveness check (see “Participants – Responsibilities,” above), that participant will be automatically removed from the Council. A vote for their replacement on the Council would run in the next nearest voting cycle.

Any time a key holder is removed from the Council, the threshold may also be reduced to as long as the ratio of the threshold to the number of signers remains above 75%. If the number of signers is reduced below 8, then a safety mechanism is activated which hands control of the Security Council to the Foundation.

### **Budget**

Initially, the Optimism Foundation will cover member expenses and may provide members with a stipend. The Security Council will not request a budget from the Governance Fund at this time.

## **Iteration**
The canonical version of the Charter will be published to GitHub. Any material updates to the Charter will be reflected with a new version number at the top of this document, at which point the updated version will go into effect.

For clarity, however, this Charter cannot be altered in any way that would have the effect of fundamentally altering the security model of an OP Chain or constitute a de facto protocol upgrade (both of which require an Optimism Governance vote).

It should finally be reiterated that the role of the Security Council is intended to be progressively and programmatically reduced over time, as its functionalities are no longer needed or can be effectively managed directly by Governance. Ultimately, it is the goal of the Collective and this Council that we reach a state of protocol and governance reliability that allows for the full deprecation of the Council’s multisig, and the full and final dissolution of the Council.
