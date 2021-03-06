This document describes the current governance proposal process of the Optimism Collective. It will evolve, with the Collective, over time. The authoritative version is maintained [here](https://github.com/ethereum-optimism/OPerating-manual) on the Optimism Foundation Github.

### **OPerating Manual v0.1.2:  The Token House and OP Holders**

Governance in the Optimism Collective begins with the launch of the Token House and its members, the OP holders.

As Token House members, OP holders are responsible for submitting, deliberating, and voting on various types of Optimism Collective governance proposals.

In carrying out these functions, OP holders may either vote their OP directly, or delegate their OP voting power to an eligible third party.

The Token House is just the first part of the Optimism Collective [governance structure](https://community.optimism.io/docs/governance/). Launch of the Citizens’ House will soon follow and this OPerating Manual will be updated accordingly.

### **Governance Toolkit**

The two primary tools for Optimism Collective governance are:

- [**Snapshot**](https://snapshot.org/#/opcollective.eth): Where all Token House governance proposals are submitted for vote.
- [**The Optimism Forum**](http://gov.optimism.io): A platform for discussion and deliberation about governance proposals.

### **Proposal Process – Components of a Valid Proposal**

The lifecycle of a Token House governance proposal involves four phases:  (1) feedback; (2) submission; (3) voting; and (4) implementation. Each phase, and its associated requirements, are described below.

1 . **Feedback**

Anyone submitting a proposal should make an effort to gather feedback from the community and from Delegates prior to submitting a proposal for vote. There are two primary avenues for feedback:
    a. For lightweight or early feedback, authors may post a proposal (or an abbreviated version of your proposal) in the **#gov-temp-check channel on [Discord](https://discord-gateway.optimism.io/)**. This channel is open to the entire Optimism community and can be used as an easy way to get a quick temperature check.
    b. For formal feedback from governance participants, authors may **post a proposal in the Forum with a [DRAFT] label in the title**. This signals your proposal is ready for feedback from Token House delegates.
All feedback from these two forums is non-binding, but proposers are expected to engage in good faith. This step is designed to help craft thoughtful, effective proposals.

After incorporating feedback, the proposal author may remove `[DRAFT]` from the proposal title and advance to proposal submission.

2 . **Submission**

To be eligible for voting, a Token House governance proposal must be formally submitted by an OP holder or their delegate. This means that the proposal must be:

- **A valid Proposal Type.** All v0.1 governance proposals must fall within one of the following categories:
    - Governance Fund (Phase 0 or Phase 1)
    - Protocol Upgrade
    - Inflation Adjustment
    - Director Removal
    - Treasury Appropriations
    - Rights Protections

For a more detailed description of each Proposal Type, see “Proposal Process – By Proposal Type” below.

- **Properly formatted to the applicable template.** Each Proposal Type will have a specific Template associated with it in the Forum. Prior to submission, a proposal author must conform their proposal to the format of the applicable Template in all material respects. This will include, for the time being, a requirement that all submissions be made in English.
- **Approved by at least one delegate.** Over the course of discussion and feedback, at least one Delegate with more than 0.0005% of voting power must signal that they believe the proposal is ready for vote. In the spirit of governance minimization, this document will not codify an explicit approval mechanism but will expect community members to interpret this appropriately.
- **Formally submitted to voting**. One week before the start of each voting cycle, the Foundation will start a Voting Period Submission thread on the Forum. To formally submit a proposal for voting, the proposal author must either (a) update their proposal title to start with `[READY]` or (b) add a link to this Voting Period Submission thread that points to their proposal on the Forum. At the start of the next Voting Period, the Optimism Foundation will submit all valid proposals marked as ready to Snapshot for voting.

Submitted proposals must satisfy all the above criteria to be considered valid. Invalid proposals will be thrown out.

Anyone submitting a proposal is welcome to submit a draft version of the proposal for feedback on the Optimism Forum. To do so, please include `[Draft]` in your Forum title, then update the proposal title once the proposal body is finalized.

3 . **Voting**

To minimize overhead, all votes are conducted on Snapshot at regular intervals called **voting periods**. Voting periods begin each Thursday at 7pm GMT and end 1 week and 6 days later, on the following Wednesday at 7pm GMT. Proposal types may require one or more voting periods before a resolution to the vote can be reached.

A Token House governance proposal will only be approved if it satisfies the following minimum vote thresholds:

- **Quorum:** The minimum number of total OP votes required to be cast in connection with a proposal. Here, a quorum is measured as *a % of the total votable OP supply*.
    - The total votable OP supply will be determined based on a reasonable estimate provided by the Optimism Foundation prior to each voting period.
- **Approval threshold:**  The minimum number of OP votes required to be cast in favor of approving a proposal. The approval threshold for each proposal is measured as *% of votes cast to approve relative to the total number of votes cast in connection with a proposal*.

**A snapshot to determine voting power** for each delegate or OP holder will be taken at the commencement of a given voting period.

Depending on the Proposal Type, exact quorum and approval threshold requirements may vary.

4 . **Implementation**

Proposals that are rejected due to invalidity or insufficient support can be resubmitted. Approved proposals are routed to the Optimism Foundation for implementation, as more fully described in the “Implementation and Administration” section below.

### **Proposal Process – Lifecycle**

While the details of a particular Token House governance proposal may vary by Proposal Type, a proposal’s lifecycle will generally look something like this:

![Proposal Process Lifecycle](/images/lifecycle.png)

### **Proposal Process  – By Proposal Type**

The different requirements for submission and approval of each Proposal Type are summarized below.

|Proposal Type                   |Description                                                                                                                                                                                                                                                                                            |Submission Requirements                                                                                                                                                                                                                                                                                                                                                      |Vote Duration (# of voting periods)|Quorum (minimum % of votable OP supply actually voted)|Approval Threshold(minimum % of votes cast to approve relative to total **non-abstaining** votes cast)|
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------|-----------------------------------------------------------------------------------|
|Governance Fund  (Phase 0 Batch)|OP distributions to proactively incentivize future growth of projects and communities in the Optimism ecosystem. [Phase 0](https://community.optimism.io/docs/governance/gov-fund/#:~:text=%23-,Phase%200,-Phase%200%20) specifically rewards existing projects that drove growth to Optimism before Airdrop #1|Eligibility requirements described [here](https://community.optimism.io/docs/governance/gov-fund/#:~:text=%23-,Phase%200,-Phase%200%20).   The Optimism Foundation will assist eligible Phase 0 candidates to structure submissions. Snapshot proposal for batch to be initiated by the Foundation.|1 (~2 weeks)                       | 10%                                                   | 51%                                                                               |
|Governance Fund  (Phase 1)      |OP distributions to proactively incentivize future growth of projects and communities in the Optimism ecosystem. [Phase 1](https://community.optimism.io/docs/governance/gov-fund/#:~:text=%23-,Phase%201,-Phase%201%20) begins after Airdrop #1                                                              |Forum + Snapshot                                                                                                                                                                                                                                                                          |1 (~2 weeks)                       | 10%                                                   |51%                                                                               |
|Protocol Upgrade                |Scheduled changes to the on-chain smart contracts comprising the mainnet Optimism protocol                                                                                                                                                                                                             |Snapshot                                                                                                                                                                                                                                                                                                                                                          |2 (~4 weeks)                       | 10%                                                   | 51%                                                                               |
|Inflation Adjustment            |Changes to the inflation rate of newly minted OP (currently capped at 2% annually)                                                                                                                                                                                                                     |Snapshot                                                                                                                                                                                                                                                                                                                                                         |2 (~4 weeks)                       |10%                                                   |76%                                                                               |
|Director Removal                |Removal of a director of the Optimism Foundation                                                                                                                                                                                                                                                       |Snapshot                                                                                                                                                                                                                                                                                                                                                         |2 (~4 weeks)                       |10%                                                   |76%                                                                               |
|Treasury  Appropriations        |The amount of OP the Optimism Foundation may spend or distribute annually, beginning in Year 2 of its existence (the Year 1 budget is 30% of the initial total OP supply)                                                                                                                              |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                  |2 (~4 weeks)                       |10%                                                   |51%                                                                               |
|Rights Protections              |OP holders must consent to any changes to the founding documents of the Optimism Foundation, if those changes would materially reduce their rights                                                                                                                                                     |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                  |2 (~4 weeks)                       |10%                                                   |51%                                                                               |

### **Implementation and Administration**

In all cases, Optimism Collective governance is intended to be carried out consistent with the terms of its [Working Constitution](https://gov.optimism.io/t/working-constitution-of-the-optimism-collective/55), the spirit of its [Code of Conduct](https://gov.optimism.io/t/code-of-conduct/5/3), and the pursuit of its [Optimistic Vision](https://www.optimism.io/vision). The Optimism Foundation will steward this process as described below.

**Administration**

The Optimism Foundation will facilitate the administration of the governance procedures described in this OPerating Manual with the aim of ensuring that OP holders may participate thoughtfully in Token House governance. Such administrative services may include:

- Moderation of governance proposals to ensure they are validly submitted and voted upon;
- Removal of proposals that reasonably appear to be fraudulent, spam-oriented, defamatory, hateful, or otherwise inappropriate or inconsistent with the values of the Collective;
- Monitoring of votes, the votable token supply, and voting periods for purposes of determining whether quorums and approval thresholds are met;
- Management of mutually contradictory proposals that are submitted simultaneously or in close proximity to one another;
- Administration of network maintenance, such as emergency bug fixes or release rollbacks (with or without a governance vote); and
- Such other things as the Foundation deems appropriate in connection with the above.

**Implementation**

Approved Token House governance proposals will be routed to the Optimism Foundation for implementation.

Upon receipt of an approved proposal, the Optimism Foundation will determine whether the proposal is safe, secure, consistent with the purposes of the Foundation and the Collective, and capable of being implemented in a legally compliant manner.

- If it is, the Foundation will act diligently and in a commercially reasonable manner to cause the proposal to be implemented.
- If it is not, the Foundation may remove the proposal for resubmission or cause the proposal to be implemented with certain guardrails, in its discretion, and coupled with an explanation to the Collective as to why the proposal was rejected or limited.

The Optimism Foundation will undertake this ministerial work with a view towards increasingly decentralizing its role over time.

### **Amendments**

The procedures described in this OPerating Manual will go into effect at the time of Airdrop #1, and be adjusted later in connection with a series of governance experiments. These changes include but are not limited to introducing the Citizens’ House, and adding, removing, and modifying Proposal Types and rules relating to voting processes. Any non-clerical updates to the OPerating Manual will be reflected with a new version number at the top of this document, at which point the updated version will go into effect.
