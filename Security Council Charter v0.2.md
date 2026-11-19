

This Charter outlines the structure and responsibilities of the Security Council and its participants. 

The exact number of participants depends upon candidate outreach, which is ongoing. This Charter will be updated with exact participant numbers and signing thresholds according to the change process outlined below before the Security Council is implemented.

# **Security Council Charter v0.2** 

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

The Council Lead will coordinate the ongoing operations of the key holding Council participants. The Council Lead is elected by the Token House and appoints the key holding participants, subject to confirmation veto by the Token House (see “Participants – Lead Election, Appointment, and Terms,” below). The Council Lead’s role is procedural, communicative, and includes recruiting and nominating key holders. It has no ability to influence the substantive signing decisions of key holders.

### **Normal Operation**

During normal operation, the Security Council is intended to act as an oracle for the Optimism Governance process: initiating protocol upgrades and changing role designations (such as designations for the Sequencer, Proposer, and Challenger roles, as well as designating the composition of the participants on the Security Council multisig), solely as directed by Optimism Collective governance outcomes. Changes to the composition of the Security Council multisig follow the Council Lead’s appointment and the Token House’s confirmation process described below.

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

### **Lead Election, Appointment, and Terms**

**Lead election:** The Council Lead is elected by the Token House through an Elections proposal using approval voting, with one seat. The election runs a one-week nomination period followed by a one-week vote.

**Appointment:** The Council Lead nominates the key holding participants, applying the requirements defined in the Security Council Member Selection Criteria. Before a nomination is posted, the Optimism Foundation completes eligibility screening for the nominee. Each nominee is submitted as a separate Council Appointment proposal with a one-week review period and a one-week veto period. An appointment is vetoed if veto votes reach 20% of active votable OP supply. A vetoed nominee is not seated, and the Council Lead nominates a replacement.

Participants are subject to eligibility screening prior to joining the Council and receiving signing authorization on the multisig (see “Participants – Eligibility,” below). There is no limit to the number of terms a Security Council participant may serve.

### **Eligibility**

Participants on the Security Council need to be selected in accordance with the criteria outlined in the [Security Council Member Selection Criteria](./Security%20Council%20Member%20Selection%20Criteria%20v0.1.md) document. The Council Lead may not nominate a candidate whose appointment would breach the Security Council Member Selection Criteria.

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
- Onboarding new Council participants;
- Recruiting and nominating key holding participants, and nominating replacements when seats become vacant; and
- Communicating with external stakeholders, including Optimism Governance, as to Council operations.
All Security Council participants are expected to perform these responsibilities with the awareness that OP Chains, the OP Stack, the developing Superchain, and the associated products, tools, and documentation are in a rapidly evolving nascent state. To the extent that unforeseeable circumstances or ambiguities arise (including in connection with potential responses to Exception Events), the participants will work in good faith to resolve them consistent with this Charter and the Law of Chains.

Finally, all Security Council participants are also responsible for complying with (i) the Code of Conduct of the Optimism Collective and (ii) any additional, internal conflict of interest procedures that the Council may develop from time to time.

### **Accountability**

The Security Council is accountable to Optimism Governance. The Token House may vote to remove Security Council members at any time for severe violations of the Code of Conduct. The Token House may also remove the Council Lead through a Representative Removal proposal, in which case a new Lead election is held.

The Security Council can also act unilaterally to remove a participant who fails to satisfy the requirements of this Charter if such failure falls within the defined scope of the Council’s emergency powers (see “Structure – Emergency Response” above).

Governance votes for removal of a Security Council participant for violation of the Code of Conduct will occur before the end of the next voting cycle. The Council Lead will nominate a replacement through a Council Appointment proposal.

Security Council members may be removed for failure to satisfy the requirements of this Charter immediately via an Emergency Response. The Council Lead will nominate a replacement through a Council Appointment proposal.

Additionally, if a Security Council key holder fails to prove access to their keys by satisfying the requirements of a scheduled liveness check (see “Participants – Responsibilities,” above), that participant will be automatically removed from the Council. The Council Lead will nominate a replacement through a Council Appointment proposal.

Any time a key holder is removed from the Council, the threshold may also be reduced to as long as the ratio of the threshold to the number of signers remains above 75%. If the number of signers is reduced below 8, then a safety mechanism is activated which hands control of the Security Council to the Foundation.

### **Budget**

The Council Lead is expected to propose operating budgets for the Security Council every 12 months, with the opportunity for a re-adjustment proposal after 6 months. The Security Council operates a dedicated budget multisig managed by the Council Lead, from which Council compensation is paid. Recipients must complete KYC/KYB before payment.

## **Iteration**
The canonical version of the Charter will be published to GitHub. Any material updates to the Charter will be reflected with a new version number at the top of this document, at which point the updated version will go into effect.

For clarity, however, this Charter cannot be altered in any way that would have the effect of fundamentally altering the security model of an OP Chain or constitute a de facto protocol upgrade (both of which require an Optimism Governance vote).

It should finally be reiterated that the role of the Security Council is intended to be progressively and programmatically reduced over time, as its functionalities are no longer needed or can be effectively managed directly by Governance. Ultimately, it is the goal of the Collective and this Council that we reach a state of protocol and governance reliability that allows for the full deprecation of the Council’s multisig, and the full and final dissolution of the Council.
