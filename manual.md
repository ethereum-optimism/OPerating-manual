This document describes the current governance proposal process of the Optimism Collective. It will evolve, with the Collective, over time. The authoritative version is maintained [here](https://github.com/ethereum-optimism/Operating-manual) on the ethereum-optimism Github.

### **Operating Manual v2.0.0**

The Optimism Collective is governed by the Token House.

In the Token House, OP holders are responsible for voting on various types of Optimism Collective governance proposals. They may do so by either voting their OP directly (after delegating their OP voting power to their own address), or by delegating their OP voting power to an eligible third party. Addresses with delegated OP voting power are called “delegates.” 

All Token representatives are expected to exercise their authority responsibly and in accordance with the [Rules of Engagement](https://gov.optimism.io/t/rules-of-engagement-2-0/5728) and [Optimist Expectations](https://gov.optimism.io/t/optimist-expectations/7241). 


## **Optimism Governance**
### **Governance Toolkit**

The primary tools for Optimism governance are currently:

- [Token House Governance Contract:](https://optimistic.etherscan.io/address/0xcdf27f107725988f2261ce2256bdfcde8b382b10) The on-chain voting contract for Token House governance proposals. Where all Token House qualifying governance proposals are submitted for vote. 
- [Optimism Governance Portal:](https://vote.optimism.io/) A front-end interface that enables Token House members to delegate and vote their OP on-chain.
- [The Optimism Forum:](http://gov.optimism.io/) A platform for discussion and deliberation about governance proposals.

These tools or their uses may change over time as governance evolves. While voting in the Token House currently takes place on-chain through the Governance Contract, some successful votes are administered and implemented by the Optimism Foundation (see below), which should not be the case indefinitely. 

### **Proposal Process**

The Collective makes decisions through governance proposals. Proposals are accepted or rejected using a voting process. The proposal must be one of the valid proposal types listed in the table below, and it must follow the voting process described here.

Governance proposals typically undergo a three-week cycle, with some exceptions as outlined below. All public voting periods last 7 days.

Each “Voting Cycle” runs from Thursday at 19:00p GMT (12p PST) until Wednesday at 19:00 GMT (12p PST). All governance votes correspond to regular Voting Cycles, which you can reference [here](https://calendar.google.com/calendar/embed?src=c_4hui70itm089e7t8q50heh1kno%40group.calendar.google.com&ctz=Europe%2FBerlin), with the exception of Protocol Upgrades which may begin the process described below at any point in time. Once a valid Protocol Upgrade draft has been posted to the forum, a governance administrator will add a comment with the date the proposal will move to a vote, subject to the required approvals.  


### **All Other Proposal Types**


#### **Feedback and Review**

All proposals should be posted to the Forum for review by anyone in the Optimism community. Proposal authors are expected to be responsive to delegate feedback. Authors should include a summary of incorporated feedback as a comment on their proposal thread so future reviewers can understand the proposal’s progress. If feedback was gathered outside of the Forum (e.g. on Discord), proposal authors should include relevant links.

Proposals should be:

- Submitted as a new discussion thread on the [Governance Forum](http://gov.optimism.io/) in the appropriate category.
- Marked with [Draft] in the title.
- Formatted and contains information consistent with the [standard proposal template.](https://gov.optimism.io/t/standard-proposal-template-optimism-token-house/5443)

For a proposal proposed in the Token House to proceed to a vote, four of the top 100 delegates must give explicit approval on the discussion thread. Proposals initiated by the Foundation do not require delegate approvals. Delegates may not approve their own proposals. Delegates may signal approval by pasting the following comment on the proposal discussion thread: *”I am an Optimism delegate [link to your [delegate commitment](https://vote.optimism.io/delegates/your_address)] with sufficient voting power and I believe this proposal is ready to move to a vote."*

If a delegate approves a proposal to move to a vote, it is not an endorsement of that proposal.  It simply signifies that they believe the proposal is ready to move to a vote.

After a proposal has received the required approvals, the proposal author should update the proposal title from [Draft] to [Final] and tag a governance administrator. 

If a proposal author does not get explicit approval or wants more time for feedback, they should continue to seek feedback from the community and submit an updated proposal in the next Voting Cycle.


### **Voting**

All delegates are invited to vote on valid proposals. Without the necessary approvals, proposals will not move to a vote.

If a proposal is submitted for a vote and does not pass, but is not vetoed, the proposal will not be executed. If a proposal author wishes to iterate on a proposal that has been rejected, they should:

1. Create a new proposal thread on the Forum.
2. Include a link to the first proposal that did not pass.
3. Clearly identify what has changed in the new proposal.


### **Valid Proposal Types**

**Submission:** All proposals must be submitted on the forum before moving to on-chain voting, except maintenance upgrades, which proceed directly to on-chain voting. 

The different requirements for submission and approval of each Proposal Type are summarized below.  If a specific template is not specified below, proposals should follow this [standard proposal template.](https://gov.optimism.io/t/standard-proposal-template-optimism-token-house/5443) All governance proposals must fall within one of the following categories. Additional proposal types may be added in future Seasons, according to the Change Process outlined below. 

**Duration:** Most proposals go through a two-week review period and a one week voting or veto period. Exceptions:

- Maintenance upgrades do not go through a review period, but move straight to one-week veto period.
- The Protocol Upgrade process has a one week stakeholder veto period. 

**Quorum:** All votes require 30% quorum. 

Depending on the Proposal Type, exact approval and veto threshold requirements may vary. Please note all thresholds may be adjusted iteratively. 
| **Proposal Type** | **Description** | **Proposer** | **Voting Type** | **Approval Threshold** | **Veto Threshold**** | Duration |
| --- | --- | --- | --- | --- | --- | --- |
| Maintenance Upgrade Proposals* | Protocol maintenance required to continue network operations on a shorter timescale than voting periods, e.g. to react to L1 hard forks or to perform bugfixes and maintenance on a shorter timeframe. Must not materially change the behavior of the protocol for end users, infra providers, or chain governors. | Permissionless | Optimistic approval | N/A | 20% | One week veto period |
| Code of Conduct Violation | Code of Conduct enforcement actions (including grant policy violations) will be subject to veto | Enforcing party outlining actions | Optimistic approval | N/A | 20% | One week veto period |
| Protocol and Governor Upgrades | Scheduled changes to the  mainnet Optimism protocol (smart contracts and/or hardforks) or governance contract. | Permissionless | N/A | Veto | N/A | One week veto period |
| Treasury Appropriations | The amount of OP the Optimism Foundation may spend or distribute annually beyond the 30% of the initial total OP supply | Foundation | Active approval | 51% | No veto | Two week review period; one week voting period |
| Ratification | Ratification of governance documents. | Foundation | Active approval | 51% | No veto | Two week review period; one week voting period |
| Council Dissolution | A Council may be dissolved if it is no longer fulfilling its Charter | Permissionless | Active approval | 51% | No veto | Two week review period; one week voting period |
| Representative Removal | Council members may be removed from their position for failing to uphold the responsibilities outlined in the relevant Charter or to act with honesty and transparency, in accordance with the [Rules of Engagement](https://gov.optimism.io/t/rules-of-engagement-2-0/5728), including by refraining from engaging in self-dealing. | Permissionless | Active approval | 51% | No veto | Two week review period; one week voting period |
| Director Removal | Removal of a director of the Optimism Foundation. | Permissionless | Active approval | 76% | No veto | Two week review period; one week voting period |
| Rights Protections | OP holders must consent to any changes to the founding documents of the Optimism Foundation, if those changes would materially reduce their rights. | Foundation | Active approval | 51% | No veto | Two week review period; one week voting period |
| Sequencer ETH: Passive Management | Passive management of sequencer ETH accruing to the Collective treasury. | Foundation | Active approval | 51% | No veto | Two week review period; one week voting period |
| Elections | Electing representatives to Councils or Boards. | All qualified candidates | Approval voting | N/A | No veto | Two week review period; one week voting period |
| Inflation | Changes to the inflation rate of newly minted OP (currently capped at 2% annually) | Permissionless | Active approval | 76% | N/A | Two week review period; one week voting period; one week veto period |

*The Maintenance Upgrade Proposal Type is needed because L1 releases may not align with Optimism’s standard voting cycles. 

** Veto thresholds are expressed as a percentage of all eligible votes (votable supply * threshold.) Approval thresholds are expressed as a percentage of quorum.


## **Thresholds** 


A Token House governance proposal is **approved** if it satisfies the following minimum vote thresholds:

- **Quorum:** The minimum number of total OP votes required to be cast in connection with a proposal is 30%. Here, a quorum is measured as a % of the total active votable OP supply, as of the start of the voting period. “Votable supply” is the total amount of OP that has been delegated, and therefore can participate in voting. Votable supply is considered active if delegated voting power has been utilized within the past 6 months. An illustrative chart of the total votable OP supply can be found [here](https://dune.com/optimismfnd/optimism-op-token-house). This includes abstain votes.

- **Approval threshold:** The minimum number of OP votes required to be cast in favor of approving a proposal. The approval threshold varies by proposal type, as outlined in the table above. The approval threshold is measured as % of votes cast to approve relative to the total number of yes/no votes cast in connection with a proposal. This does not include abstain votes.

A snapshot to determine voting power for each delegate will be taken at the commencement of a given voting period, and voting will be hosted on the Optimism Governance Portal.

Elections works as described below:  

- All Elections utilize approval voting. Approval voting is a voting method in which each voter can cast their full voting power for as many candidates as they chose. The top [X] candidates, by number of votes, will be elected, so long as they meet quorum requirements. 
- In the case an elected member declines their position before the start of a term, the runner-up will be offered their place. 
- If a member wishes to resign before the end of their term, they must appoint a replacement and communicate this change on the forum at least 7 days prior to this change taking effect.
- If there is a vote to remove a member, the Lead, or a simple majority of the remaining membership, may appoint a replacement for the remainder of the term.
- Unless otherwise specified in a Charter, in the event membership falls below a pre-determined threshold, or to half of the original membership, operations will temporarily cease, or be transferred to the Foundation. In this case, the Foundation will facilitate a process with the community to assess the best way to proceed.
- Members should only serve in one position per Season. There are no term limits for members, but they may be implemented in the future if the need arises.

## **Veto Procedure**

Casting a veto is a serious decision. In cases, when an approved proposal is vetoed, it will not be enacted and instead will enter into an appeals process. The appeals process consists of a one-week discussion period after which proposals may be re-submitted to vote. In the case of Protocol Upgrades, vetoing an approved proposal may have serious consequences on engineering timelines and milestones.  

## **Implementation and Administration**

In all cases, Optimism Collective governance is intended to be carried out consistent with the terms of its [Working Constitution](https://gov.optimism.io/t/working-constitution-of-the-optimism-collective/55), the spirit of both the [Rules of Engagement](https://gov.optimism.io/t/rules-of-engagement/5/3) and the [Code of Conduct](https://gov.optimism.io/t/code-of-conduct/5751), and the pursuit of its [Optimistic Vision](https://www.optimism.io/vision). The Optimism Foundation will steward this process as described below.

**Administration**

The Optimism Foundation will facilitate the administration of the governance procedures described in this Operating Manual with the aim of ensuring that members of the Collective may participate thoughtfully in governance. Such administrative services may include:

- Moderation of governance proposals to ensure they are validly submitted and voted upon;
- Removal of proposals that reasonably appear to be fraudulent, spam-oriented, defamatory, hateful, or otherwise inappropriate or inconsistent with the values of the Collective;
- Monitoring of votes, voting power, the votable token supply, and voting periods for purposes of determining whether quorums, approval, and veto thresholds are met or accurately reflected;
- Management of mutually contradictory proposals that are submitted simultaneously or in close proximity to one another;
- Administration of network maintenance, such as emergency bug fixes or release rollbacks (with or without a governance vote); and
- Such other things as the Foundation deems appropriate in connection with the above.

**Implementation**
Valid Token Allocation Proposals related to the Governance Fund are automatically implemented via onchain execution. The Security Council will enact officially approved Upgrades. All other approved governance proposals will be routed to the Optimism Foundation for implementation.

Upon receipt of an approved proposal, the Optimism Foundation will determine whether the proposal is safe, secure, consistent with the purposes of the Foundation and the Collective, and capable of being implemented in a legally compliant manner (including completing KYC).

- If it is, the Foundation will act diligently and in a commercially reasonable manner to cause the proposal to be implemented.
- If it is not, the Foundation may remove the proposal for resubmission or cause the proposal to be implemented with certain guardrails, in its discretion, and coupled with an explanation to the Collective as to why the proposal was rejected or limited.

The Optimism Foundation will undertake this ministerial work with a view towards increasingly decentralizing its role over time.

### **Change Process**

The procedures described in this Operating Manual will go into effect as releases are published on GitHub. Major releases to the manual will be made in connection with a series of governance experiments (“Seasons”). These changes include but are not limited to the reduction or expansion of the Citizens’ House or adding and modifying Proposal Types and rules relating to voting processes. Only the removal of a proposal type requires a governance vote. Any non-clerical updates to the Operating Manual will be reflected with a new version number at the top of this document, at which point the updated version will go into effect.

## Process TLDR
- Proposals are reviewed over a three week voting cycle (some exceptions apply). For example, Protocol or Governor Upgrades do not need to occur during regular Voting Cycles. 
- For other permissionless proposal types, you may draft a proposal based on [this](https://gov.optimism.io/t/standard-proposal-template-optimism-token-house/5443) template and post it on the Forum with [Draft] in the title for feedback. Delegates and/or Citizens will provide feedback on your proposal in the forum. Use your judgment to incorporate feedback.
- Once a valid proposal has been approved by four top 100 delegates or four Citizens, tag a governance administrator to add your proposal to the nearest Voting Cycle. Proposals initiated by the Foundation do not require approvals.
- If your proposal is passed, the Optimism Foundation will facilitate its administration. The Foundation will be in touch to collect additional information from your project in order to execute the proposal or grant, including information to perform KYC.
- If your proposal fails, you can make a new proposal in the next cycle specifying how you have incorporated significant changes from your first proposal.

