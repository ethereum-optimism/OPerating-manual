This document describes the current governance proposal process of the Optimism Collective. It will evolve, with the Collective, over time. The authoritative version is maintained [here](https://github.com/ethereum-optimism/Operating-manual) on the ethereum-optimism Github.

### **Operating Manual v0.3.3:  The Token House and Citizens' House**

The Optimism Collective is governed by two houses, the Token House and the Citizens’ House. 

In the Token House, OP holders are responsible for submitting, deliberating, and voting on various types of Optimism Collective governance proposals. They may do so by either voting their OP directly (after delegating their OP voting power to their own address), or by delegating their OP voting power to an eligible third party. Addresses with delegated OP voting power are called “delegates.” 

In the Citizens’ House, Optimism citizens are responsible for allocating rewards to providers of public goods through a process called “retroactive public goods funding” (RetroPGF). Citizenship is currently temporary, with the citizenry for RPGF Round 2 demarcated via entries in the AttestationStation smart contract. Over time, the scope and role of the Citizens’ House is expected to expand significantly. 

All Token and Citizens’ House representatives are expected to exercise their authority responsibly and in accordance with community standards. 


## **Token House Governance**
### **Governance Toolkit**

The primary tools for Token House governance are currently:

- [Token House Governance Contract:](https://optimistic.etherscan.io/address/0xcdf27f107725988f2261ce2256bdfcde8b382b10) The on-chain voting contract for Token House governance proposals. Where all Token House qualifying governance proposals are submitted for vote. 
- [Optimism Governance Portal:](https://vote.optimism.io/) A front-end interface that enables Token House members to delegate and vote their OP on-chain.
- [The Optimism Forum:](http://gov.optimism.io/) A platform for discussion and deliberation about governance proposals.
- [Discord:](https://discord-gateway.optimism.io/) For informal governance discussion and feedback.

These tools or their uses may change over time as governance evolves. For example, additional user interfaces dedicated to governance councils may be developed in the future. Likewise, while voting currently takes place on-chain through the Governance Contract, successful votes are currently administered and implemented by the Optimism Foundation (see below), which should not be the case indefinitely. 

### **Proposal Process**

The Token House makes decisions through governance proposals. Proposals are accepted or rejected using a voting process. Anyone can submit a proposal to governance. The proposal must be one of the valid proposal types listed below, and it must follow the voting process described here.

### **Voting Process**

All Token House proposals go through a five week cycle.

Each “week” runs from Thursday at 19:00p GMT (12p PST) until Wednesday at 19:00 GMT (12p PST).

### **Governance Fund Proposal Types**

Governance Fund Proposals (Season 3 grant applications) will be reviewed by the Grants Council and should follow the submission process outlined in the [Grants Council: Internal Operating Procedures](https://gov.optimism.io/t/grants-council-internal-operating-procedures/4832).

If a submitted grant proposal is determined not ready for review by the Grants Council, proposers should work with non-Council delegates to resubmit their proposal via the Council’s application process. 

### **All Other Proposal Types**


#### **Weeks 1-3: Feedback and Review (`[Draft]`)**

All other proposal types (besides grant proposals) should be posted to the Forum for review by anyone in the Optimism community. Proposal authors are expected to be responsive to delegate feedback. 

Proposals should be:

- Submitted as a new discussion thread on the [Governance Forum](http://gov.optimism.io/) in the appropriate category.
- Marked with [Draft] in the title.
- Formatted and contain information consistent with the [standard proposal template](https://gov.optimism.io/t/standard-proposal-template-optimism-token-house/5443)


At the start of Week 1, a governance administrator will create a Voting Cycle Roundup thread in the forum to collect all proposals that meet the requirements for voting in Week 4. This Roundup will not include grant proposals, which will be processed and voted on by the Grants Council. 

For a non-grant proposal to proceed to Week 4, four delegates, each with >0.5% of the current votable token supply, must give explicit approval on the discussion thread. Delegates may not approve their own proposals. Delegates may signal approval by pasting the following comment on the proposal discussion thread: *”I am an Optimism delegate [link to your [delegate commitment](https://vote.optimism.io/delegate/your_address)] with sufficient voting power and I believe this proposal is ready to move to a vote."*

If a delegate approves a proposal to move to a vote, it is not an endorsement of that proposal.  It simply signifies that the delegate believes the proposal is ready to move to a vote.

After a non-grant proposal has received four delegate approvals, the proposal author should update the proposal title from [Draft] to [Final] and add a link to their proposal in the Voting Cycle Roundup thread by the last day of Week 3 at 19:00 GMT (12:00p PST). Authors should also include a summary of incorporated feedback as a comment on their proposal thread so future reviewers can understand the proposal’s progress. If feedback was gathered outside of the Forum (e.g. on Discord), proposal authors should include relevant links.

If a proposal author does not get explicit delegate approval or wants more time for feedback, they should continue to seek feedback from the community and submit an updated proposal in the next voting cycle.


#### **Week 4-5: Voting**

In the fourth and fifth weeks, all delegates (including OP token holders who have self-delegated) are invited to vote on proposals via the Optimism Governance Portal. Non-grant proposals will be included in on-chain voting only if they were (a) added to the Voting Cycle Roundup thread before the deadline, and (b) have the required approval comments from four delegates with >0.5% voting power. Without explicit delegate approval, proposals will not move to an on-chain vote.

A Token House governance proposal is **approved** if it satisfies the following minimum vote thresholds:

- **Quorum:** The minimum number of total OP votes, including abstain votes, required to be cast in connection with a proposal. Here, a quorum is measured as _a % of the total votable OP supply, as of the start of the voting period._ “Votable supply” is the total amount of OP that has been delegated, and therefore can participate in voting. An illustrative chart of the total votable OP supply can be found [here](https://dune.com/optimismfnd/optimism-op-token-house). 
- **Approval threshold:** The minimum number of OP votes required to be cast in favor of approving a proposal. The approval threshold for each proposal is measured _as % of votes cast to approve relative to the total number of yes/no votes cast in connection with a proposal._ This does not include abstain votes. 

A snapshot to determine voting power for each delegate will be taken at the commencement of a given voting period, and voting will be hosted on the Optimism Governance Portal.

Depending on the Proposal Type, exact quorum and approval threshold requirements may vary. For more information, refer to the proposal types below.

If a non-grant proposal is submitted for a vote and does not pass, the proposal will not be executed. If a proposal author wishes to iterate on a proposal that has been rejected, they should:

1. Create a new proposal thread on the Forum.
2. Include a link to the first proposal that did not pass.
3. Clearly identify what has changed in the new proposal.

### **Valid Proposal Types**

All v0.3 governance proposals must fall within one of the following categories:
- Governance Fund 
- Protocol Upgrade
- Inflation Adjustment
- Director Removal
- Treasury Appropriations
- Rights Protections

The different requirements for submission and approval of each Proposal Type are summarized below.  All proposals other than Governance Fund proposals should follow this [standard proposal template.](https://gov.optimism.io/t/standard-proposal-template-optimism-token-house/5443) Additional proposal types, such as those related to the Grants Council, may be added in future Seasons. 

|Proposal Type|Description|Submission Requirements|Vote Duration|Quorum|Approval Threshold|
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------|-----------------------------------------------------------------------------------|
|Governance Fund      |OP grants to proactively incentivize future growth of projects and communities in the Optimism ecosystem. |Proposals should follow [this template](https://gov.optimism.io/t/governance-fund-phase-1-how-to-create-a-proposal/216) and the process outlined in [Grants Council: Internal Procedures](https://gov.optimism.io/t/grants-council-internal-operating-procedures/4832).                                                                                                                                                                                                                                                                                                                 |Three-week review cycle plus two week Grants Council vote window             | N/A                                                |See [Grants Council: Internal Procedures](https://gov.optimism.io/t/grants-council-internal-operating-procedures/4832).                                                                                |
|Protocol Upgrade                |Scheduled changes to the on-chain smart contracts comprising the mainnet Optimism protocol                                                                                                                                                                                                             |Forum + On-Chain Voting                                                                                                                                                                                                                                                                                                                                                          |Three-week review cycle plus two week vote window                     | 30%                                                   | 76%                                                                               |
|Inflation Adjustment            |Changes to the inflation rate of newly minted OP (currently capped at 2% annually)                                                                                                                                                                                                                     |Forum + On-Chain Voting                                                                                                                                                                                                                                                                                                                                                         |Three-week review cycle plus two week vote window                       |30%                                                   |76%                                                                               |
|Director Removal                |Removal of a director of the Optimism Foundation                                                                                                                                                                                                                                                       |Forum + On-Chain Voting                                                                                                                                                                                                                                                                                                                                                         |Three-week review cycle plus two week vote window                      |30%                                                   |76%                                                                               |
|Treasury  Appropriations        |The amount of OP the Optimism Foundation may spend or distribute annually, beginning in Year 2 of its existence (the Year 1 budget is 30% of the initial total OP supply)                                                                                                                              |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                  |Three-week review cycle plus two week vote window                     |30%                                                   |51%                                                                               |
|Rights Protections              |OP holders must consent to any changes to the founding documents of the Optimism Foundation, if those changes would materially reduce their rights                                                                                                                                                     |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                  |Three-week review cycle plus two week vote window                     |30%                                                   |51%                                                                               |
|Delegate Suspension              | The Token House may vote to suspend a delegate for severe violations of the [delegate code of conduct](https://gov.optimism.io/t/delegate-code-of-conduct/3943)                                                                                                                                                     |Proposals to be initiated by the Foundation in response to reported violations                                                                                                                                                                                                                                                                                                                                 |Three-week review cycle plus two week vote window                     |30%                                                   |51%                                                                               |


## **Citizens' House Governance**

### **RetroPGF Rounds**
Citizens’ House governance begins with RetroPGF, with voting and disbursements occuring over a series of “rounds.” In each RetroPGF round, the Citizens’ House votes to retroactively reward public goods projects that have provided substantial impact. 

RetroPGF rounds are run according to the following process:

- Scoping:  The overall amount of rewards to be allocated and scope of impact are defined at the outset of the round.  
- Profile creation:  Projects are notified and invited to create a profile in the [RetroPGF Application Manager.](https://app.optimism.io/retropgf-manager) 
- Voting:  Votes are collected from the citizens with the requisite [AttestationStation](https://community.optimism.io/docs/governance/attestation-station/#general-faq) entries and tallied. 
- Disbursement:  Based on the simple weighted average of the Citizens’ House vote, the overall reward amount for the round is divided among the winning projects. 

Additional information on the process for RetroPGF Round 2 is available [here.](https://community.optimism.io/docs/governance/retropgf-2/#) 


## **Implementation and Administration**

In all cases, Optimism Collective governance is intended to be carried out consistent with the terms of its [Working Constitution](https://gov.optimism.io/t/working-constitution-of-the-optimism-collective/55), the spirit of both the [Rules of Engagement](https://gov.optimism.io/t/rules-of-engagement/5/3) and the [Delegate Code of Conduct](https://gov.optimism.io/t/delegate-code-of-conduct/3943), and the pursuit of its [Optimistic Vision](https://www.optimism.io/vision). The Optimism Foundation will steward this process as described below.

**Administration**

The Optimism Foundation will facilitate the administration of the governance procedures described in this Operating Manual with the aim of ensuring that members of the Collective may participate thoughtfully in governance. Such administrative services may include:

- Moderation of governance proposals to ensure they are validly submitted and voted upon;
- Removal of proposals that reasonably appear to be fraudulent, spam-oriented, defamatory, hateful, or otherwise inappropriate or inconsistent with the values of the Collective;
- Monitoring of votes, voting power, the votable token supply, and voting periods for purposes of determining whether quorums and approval thresholds are met or accurately reflected;
- Management of mutually contradictory proposals that are submitted simultaneously or in close proximity to one another;
- Administration of network maintenance, such as emergency bug fixes or release rollbacks (with or without a governance vote); and
- Such other things as the Foundation deems appropriate in connection with the above.

**Implementation**

Approved Token House governance proposals will be routed to the Optimism Foundation for implementation.

Upon receipt of an approved proposal, the Optimism Foundation will determine whether the proposal is safe, secure, consistent with the purposes of the Foundation and the Collective, and capable of being implemented in a legally compliant manner (including completing KYC).

- If it is, the Foundation will act diligently and in a commercially reasonable manner to cause the proposal to be implemented.
- If it is not, the Foundation may remove the proposal for resubmission or cause the proposal to be implemented with certain guardrails, in its discretion, and coupled with an explanation to the Collective as to why the proposal was rejected or limited.

The Optimism Foundation will undertake this ministerial work with a view towards increasingly decentralizing its role over time.

### **Amendments**

The procedures described in this Operating Manual will go into effect as releases are published on GitHub. Major releases to the manual will be made in connection with a series of governance experiments (“Seasons”). These changes include but are not limited to the expansion of the Citizens’ House, and adding, removing, and modifying Proposal Types and rules relating to voting processes. Any non-clerical updates to the Operating Manual will be reflected with a new version number at the top of this document, at which point the updated version will go into effect.

## Process TLDR
Optimism governance has two houses:  a Token House and a Citizens’ House.

#### Token House Governance operates as follows:
- Proposals are reviewed over a five week voting cycle.
- If you’re submitting a Governance Fund grant proposal, you’ll need to submit your proposal to the Grants Council. Please follow the process outlined in [Grants Council: Internal Procedures.](https://gov.optimism.io/t/grants-council-internal-operating-procedures/4832)
- For all other Token House proposal types, you may draft a proposal based on this template and post it on the Forum with [Draft] in the title for feedback. Delegates will provide feedback on your proposal in the forum. Use your judgment to incorporate feedback.
- Once your non-grant proposal has been approved by four delegates, each with >0.25% of voting supply, add a link to your proposal to the Voting Cycle Roundup thread by the last day of Week 3 and update the title from [Draft] to [Final]. These proposals will move on to Week 4 voting.
- If your proposal is passed by the Token House or Grants Council, the Optimism Foundation will facilitate its administration, including by distributing any approved OP grants. The Foundation will be in touch to collect additional information from your project in order to execute the proposal or grant, including information to perform KYC.
- If your proposal fails, you can make a new proposal in the next cycle specifying how you have incorporated significant changes from your first proposal.

#### Citizens’ House Governance operates as follows: 
- Citizenship is currently temporary, with the RetroPGF Round 2 citizenry recorded via entries in the AttestationStation. 
- RetroPGF rounds occur in intervals and according to a predefined process, which currently includes phases for scoping, nominations, profile creation, voting, and disbursements. 
