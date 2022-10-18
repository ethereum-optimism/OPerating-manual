This document describes the current governance proposal process of the Optimism Collective. It will evolve, with the Collective, over time. The authoritative version is maintained [here](https://github.com/ethereum-optimism/Operating-manual) on the Optimism Foundation Github.

### **Operating Manual v0.2.1:  The Token House and OP Holders**

Governance in the Optimism Collective begins with the launch of the Token House and its members, the OP holders.

As Token House members, OP holders are responsible for submitting, deliberating, and voting on various types of Optimism Collective governance proposals.

In carrying out these functions, OP holders may either vote their OP directly (by delegating their OP voting power to their own address), or delegate their OP voting power to an eligible third party. Addresses with delegated OP voting power are called “delegates.” Delegates are expected to exercise their authority responsibly and in accordance with community standards.

The Token House is just the first part of the Optimism Collective [governance structure](https://community.optimism.io/docs/governance/). Launch of the Citizens’ House will soon follow and this Operating Manual will be updated accordingly.

### **Governance Toolkit**

The primary tools for Optimism Collective governance are:

- [**Snapshot**](https://snapshot.org/#/opcollective.eth): Where all Token House governance proposals are submitted for vote.
- [**The Optimism Forum**](http://gov.optimism.io): A platform for discussion and deliberation about governance proposals.
- [**Discord**](https://discord-gateway.optimism.io/): For informal governance discussion and feedback.


### **Proposal Process**

The Optimism Collective makes decisions through governance proposals. Proposals are accepted or rejected using a voting process. Anyone can submit a proposal to Optimism governance. The proposal must be one of the **valid proposal types** listed below, and it must follow the **voting process** described here.

### **Voting Process**

The proposal Voting Cycle takes place in three one-week stages.

Each “week” runs from Thursday at 19:00p GMT (12p PST) until Wednesday at 19:00 GMT (12p PST).

#### **Week 1: Community and Delegate Feedback (`[Draft]`)**

In the first week, draft proposals are open for review by anyone in the Optimism community as a form of temperature check. Proposal authors are expected to be responsive to community and delegate feedback and use this period of time to prepare their proposal for committee review.

Proposals should be:

- Submitted as a new discussion thread on the [Governance Forum](http://gov.optimism.io/) in the appropriate category.
- Marked with [Draft] in the title.

Once posted on the form create a discussion thread in the Optimism [Discord](https://discord-gateway.optimism.io/) in the #gov-temp-check channel. To create a thread simply click the "+ Post" button and fill in your name, your projects name, and the link to your draft proposal. 

At the start of the Week 1, a governance administrator will create a Voting Cycle Roundup thread in the forum to collect all proposals that meet the requirements for committee review in Week 2.

For a proposal to proceed to Week 2 (committee review), two delegates with >0.5% of the current votable token supply must give explicit approval on the discussion thread. Delegates may not approve their own proposals. Delegates may signal approval by pasting the following comment on the proposal discussion thread: *”I am an Optimism delegate [link to your [delegate commitment](https://gov.optimism.io/t/delegate-commitments/235)] with sufficient voting power and I believe this proposal is ready to move to a vote."*

If a committee member approves a proposal to move to a vote, it is not an endorsement of that proposal by the associated committee. It simply signifies that the proposal should move to the next stage of the cycle. 

After a proposal has received two delegate approvals, the proposal author should update the proposal title from [Draft] to [Review] and add a link to their proposal in the Voting Cycle Roundup thread by the last day of Week 1 at 7pm GMT (12:00p PST). Authors should also include a summary of incorporated feedback as a comment on their proposal thread so future reviewers can understand the proposal’s progress. If feedback was gathered outside of the Forum (e.g. on Discord), proposal authors should include relevant links.

If a proposal author does not get explicit delegate approval or wants more time for feedback, they should continue to seek feedback from the community and submit an updated proposal in the next voting cycle.

#### **Week 2: Committee Review (`[Review]`)**

In the second week, committees will review all approved proposals listed on the Voting Cycle Roundup thread and publicly post their recommendations before the last day of Week 2 at 19:00 GMT (12:00p PST).


#### **Week 3: Voting**

In the third week, all delegates (including OP token holders who have self-delegated) are invited to vote on proposals on Snapshot. Proposals will be included in Snapshot only if they were (a) added to the Voting Cycle Roundup thread before the deadline, and (b) have two approval comments from two delegates with >0.5% voting power. Without explicit delegate approval, proposals will not move to a Snapshot vote.

A Token House governance proposal is **approved** if it satisfies the following minimum vote thresholds:

- **Quorum:** The minimum number of total OP votes required to be cast in connection with a proposal. Here, a quorum is measured as *a % of the total votable OP supply*. “Votable supply” is the total amount of OP that has been delegated, and therefore can participate in voting. The total votable OP supply will be determined based on a reasonable estimate provided by the Optimism Foundation prior to each Voting Cycle. OP votable supply will be included in each Voting Roundup Thread. 
- **Approval threshold:** The minimum number of OP votes required to be cast in favor of approving a proposal. The approval threshold for each proposal is measured as *% of votes cast to approve relative to the total number of votes cast in connection with a proposal*.

**A snapshot to determine voting power** for each delegate will be taken at the commencement of a given voting period, and voting will be hosted on the [Optimism Collective Snapshot page](https://snapshot.org/#/opcollective.eth).

Depending on the Proposal Type, exact quorum and approval threshold requirements may vary. For more information, refer to the proposal types below.

If a proposal is submitted for a vote and does not pass, the proposal will not be executed. If a proposal author wishes to iterate on a proposal that has been rejected, they should:

1. Create a **new proposal thread** on the Forum.
2. Include a link to the first proposal that did not pass.
3. Clearly identify what has changed in the new proposal.

#### **Valid Proposal Types**

All v0.2 governance proposals must fall within one of the following categories:
- Governance Fund (Phase 0 or Phase 1)
- Protocol Upgrade
- Inflation Adjustment
- Director Removal
- Treasury Appropriations
- Rights Protections

The different requirements for submission and approval of each Proposal Type are summarized below.

|Proposal Type|Description|Submission Requirements|Vote Duration|Quorum|Approval Threshold|
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------|-----------------------------------------------------------------------------------|
|Governance Fund  (Phase 1)      |OP distributions to proactively incentivize future growth of projects and communities in the Optimism ecosystem. Proposals should follow [this template](https://gov.optimism.io/t/governance-fund-phase-1-how-to-create-a-proposal/216).                                                             |Forum + Snapshot                                                                                                                                                                                                                                                                          |one three-week cycle                    | 30%                                                   |51%                                                                               |
|Protocol Upgrade                |Scheduled changes to the on-chain smart contracts comprising the mainnet Optimism protocol                                                                                                                                                                                                             |Snapshot                                                                                                                                                                                                                                                                                                                                                          |three-week cycle plus two week extended vote window                     | 30%                                                   | 76%                                                                               |
|Inflation Adjustment            |Changes to the inflation rate of newly minted OP (currently capped at 2% annually)                                                                                                                                                                                                                     |Snapshot                                                                                                                                                                                                                                                                                                                                                         |three-week cycle plus two week extended vote window                       |30%                                                   |76%                                                                               |
|Director Removal                |Removal of a director of the Optimism Foundation                                                                                                                                                                                                                                                       |Snapshot                                                                                                                                                                                                                                                                                                                                                         |three-week cycle plus two week extended vote window                      |30%                                                   |76%                                                                               |
|Treasury  Appropriations        |The amount of OP the Optimism Foundation may spend or distribute annually, beginning in Year 2 of its existence (the Year 1 budget is 30% of the initial total OP supply)                                                                                                                              |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                  |three-week cycle plus two week extended vote window                     |30%                                                   |51%                                                                               |
|Rights Protections              |OP holders must consent to any changes to the founding documents of the Optimism Foundation, if those changes would materially reduce their rights                                                                                                                                                     |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                  |three-week cycle plus two week extended vote window                     |30%                                                   |51%                                                                               |

### **Implementation and Administration**

In all cases, Optimism Collective governance is intended to be carried out consistent with the terms of its [Working Constitution](https://gov.optimism.io/t/working-constitution-of-the-optimism-collective/55), the spirit of its [Contributor Code of Conduct](https://gov.optimism.io/t/code-of-conduct/5/3) and upcoming Delegate Code of Conduct, and the pursuit of its [Optimistic Vision](https://www.optimism.io/vision). The Optimism Foundation will steward this process as described below.

**Administration**

The Optimism Foundation will facilitate the administration of the governance procedures described in this Operating Manual with the aim of ensuring that OP holders may participate thoughtfully in Token House governance. Such administrative services may include:

- Moderation of governance proposals to ensure they are validly submitted and voted upon;
- Removal of proposals that reasonably appear to be fraudulent, spam-oriented, defamatory, hateful, or otherwise inappropriate or inconsistent with the values of the Collective;
- Monitoring of votes, voting power, the votable token supply, and voting periods for purposes of determining whether quorums and approval thresholds are met or accurately reflected;
  -In the event of bugs in the Snapshot tool, the Foundation may manually count votes and override the results of a Snapshot vote -- however, it will only do so where the the expected, bug-free outcome is unambiguous (for example, votes that are verifiable on-chain, but which did not propagate to the off-chain Snapshot tool);   
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

The procedures described in this Operating Manual will go into effect as releases are published on GitHub. Major releases to the manual will be made in connection with a series of governance experiments (“Seasons”). These changes include but are not limited to introducing the Citizens’ House, and adding, removing, and modifying Proposal Types and rules relating to voting processes. Any non-clerical updates to the Operating Manual will be reflected with a new version number at the top of this document, at which point the updated version will go into effect.

## Process TLDR
- Optimism has a three-week proposal review cycle.
- When you’re ready, draft a proposal and post it on the Forum with `[Draft]` in the title for feedback from the community and delegates. Remember to post your proposal in the #gov-temp-check channel on Discord to get community feedback. Delegates will also provide feedback on your proposal in the forum. Use your judgment to incorporate feedback. 
- Once your proposal has been approved by two delegates with >0.5% of voting supply, add a link to your proposal to the Voting Cycle Roundup thread by the last day of Week 1 and update the title from `[Draft]` to `[Review]`. These proposals will move on to Week 2: Committee Review. 
- Committees will provide recommendations on proposals by the last day of Week 2. These proposals will be automatically added to Snapshot during the next one-week voting window.
- If your proposal is passed, the Optimism Foundation will facilitate its administration, including by distributing any approved OP grants. Note the Foundation may be in touch to collect additional information from your project in order to execute the grant.
- If your proposal fails, you can make a new proposal in the next cycle specifying how you have incorporated significant changes from your first proposal.
