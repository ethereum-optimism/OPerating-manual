This document describes the current governance proposal process of the Optimism Collective. It will evolve, with the Collective, over time. The authoritative version is maintained [here](https://github.com/ethereum-optimism/Operating-manual) on the ethereum-optimism Github.

### **Operating Manual v0.3.8:  The Token House and Citizens' House**

The Optimism Collective is governed by two houses, the Token House and the Citizens’ House. 

In the Token House, OP holders are responsible for submitting, deliberating, and voting on various types of Optimism Collective governance proposals. They may do so by either voting their OP directly (after delegating their OP voting power to their own address), or by delegating their OP voting power to an eligible third party. Addresses with delegated OP voting power are called “delegates.” 

In the Citizens’ House, Optimism Citizens are responsible for allocating rewards to providers of public goods through a process called “retroactive public goods funding” (RetroPGF). Badgeholders that participated in RetroPGF Round 3, demarcated via entries in the AttestationStation smart contract, are now Citizens. Citizenship is currently temporary. 

All Token and Citizens’ House representatives are expected to exercise their authority responsibly and in accordance with the [Rules of Engagement](https://gov.optimism.io/t/rules-of-engagement-2-0/5728) and [Code of Conduct](https://gov.optimism.io/t/code-of-conduct/5751). 


## **Optimism Governance**
### **Governance Toolkit**

The primary tools for Token House governance are currently:

- [Token House Governance Contract:](https://optimistic.etherscan.io/address/0xcdf27f107725988f2261ce2256bdfcde8b382b10) The on-chain voting contract for Token House governance proposals. Where all Token House qualifying governance proposals are submitted for vote. 
- [Optimism Governance Portal:](https://vote.optimism.io/) A front-end interface that enables Token House members to delegate and vote their OP on-chain.
- [The Citizens’ House Snapshot Space:](https://snapshot.org/#/citizenshouse.eth) A front-end interface that enables Citizens’ House members to veto Token House proposals. 
- [The Optimism Forum:](http://gov.optimism.io/) A platform for discussion and deliberation about governance proposals.
- [Discord:](https://discord-gateway.optimism.io/) For informal governance discussion and feedback.
- [Github:](https://github.com/ethereum-optimism/ecosystem-contributions/issues) Grants (Mission Requests) are managed via issues in this public github repo 
- [Charmverse:](https://app.charmverse.io/op-grants/page-701220845245208) Home of the community-led Optimism Grants Council

These tools or their uses may change over time as governance evolves. For example, additional user interfaces dedicated to governance councils may be developed in the future. Likewise, while voting currently takes place on-chain through the Governance Contract, successful votes are currently administered and implemented by the Optimism Foundation (see below), which should not be the case indefinitely. 

### **Proposal Process**

Both Houses make decisions through governance proposals. Proposals are accepted or rejected using a voting process. Anyone can submit a proposal to governance. The proposal must be one of the valid proposal types listed below, and it must follow the voting process described here.

### **Voting Process**

All governance proposals go through a three week cycle.

Each “week” runs from Thursday at 19:00p GMT (12p PST) until Wednesday at 19:00 GMT (12p PST).

### **Mission Applications**

Mission Applications to Delegate Mission Requests will be reviewed and selected by the Grants Council and should follow the submission process outlined on each Mission Request. Mission Applications to Foundation Mission Requests will be reviewed and selected by the Foundation and should follow the submission process outlined on each Mission Request.


### **All Other Proposal Types**


#### **Weeks 1-2: Feedback and Review (`[Draft]`)**

All other proposal types should be posted to the Forum for review by anyone in the Optimism community. Proposal authors are expected to be responsive to delegate and Citizen feedback. 

Proposals should be:

- Submitted as a new discussion thread on the [Governance Forum](http://gov.optimism.io/) in the appropriate category.
- Marked with [Draft] in the title.
- Formatted and contain information consistent with the [standard proposal template](https://gov.optimism.io/t/standard-proposal-template-optimism-token-house/5443)
- Mission Requests must follow the template [here](https://gov.optimism.io/t/delegate-guide-how-to-create-a-delegate-mission-request/6898#delegate-mission-request-template-3)


Before the end of Week 2, a governance administrator will create a Voting Cycle Roundup thread in the forum to collect all proposals that meet the requirements for voting in Week 3. This Roundup will not include Mission Applications, which will be processed by the Foundation or Grants Council. 

For a non-grant proposal proposed in the Token House to proceed to Week 3, four of the top 100 delegates must give explicit approval on the discussion thread. Delegates may not approve their own proposals. Delegates may signal approval by pasting the following comment on the proposal discussion thread: *”I am an Optimism delegate [link to your [delegate commitment](https://vote.optimism.io/delegate/your_address)] with sufficient voting power and I believe this proposal is ready to move to a vote."*

For a non-grant proposal, proposed in the Citizens’ House, to proceed to Week 3, four Citizens must give explicit approval on the discussion thread. Citizens may not approve their own proposals. Citizens may signal approval by pasting the following comment on the proposal discussion thread: *”I am an Optimism Citizen [link to your [attestation](https://optimism.easscan.org/schema/view/0xfdcfdad2dbe7489e0ce56b260348b7f14e8365a8a325aef9834818c00d46b31b)] and I believe this proposal is ready to move to a vote."*

If a delegate or a Citizen approves a proposal to move to a vote, it is not an endorsement of that proposal.  It simply signifies that they believe the proposal is ready to move to a vote.

After a non-grant proposal has received the required approvals, the proposal author should update the proposal title from [Draft] to [Final] and add a link to their proposal in the Voting Cycle Roundup thread by the last day of Week 2 at 19:00 GMT (12:00p PST). Authors should also include a summary of incorporated feedback as a comment on their proposal thread so future reviewers can understand the proposal’s progress. If feedback was gathered outside of the Forum (e.g. on Discord), proposal authors should include relevant links.

If a proposal author does not get explicit approval or wants more time for feedback, they should continue to seek feedback from the community and submit an updated proposal in the next voting cycle.


#### **Week 3: Voting**

In the third week, all Citizens and delegates (including OP token holders who have self-delegated) are invited to vote on proposals. The Token House votes via the Optimism Governance Portal. Non-grant proposals will be included in voting only if they were added to the Voting Cycle Roundup thread before the deadline and have the required approvals. Without explicit approval, proposals will not move to a vote.

A Token House governance proposal is **approved** if it satisfies the following minimum vote thresholds:

- **Quorum:** The minimum number of total OP votes, including abstain votes, required to be cast in connection with a proposal. Here, a quorum is measured as _a % of the total votable OP supply, as of the start of the voting period._ “Votable supply” is the total amount of OP that has been delegated, and therefore can participate in voting. An illustrative chart of the total votable OP supply can be found [here](https://dune.com/optimismfnd/optimism-op-token-house). 
- **Approval threshold:** The minimum number of OP votes required to be cast in favor of approving a proposal. The approval threshold for each proposal is measured _as % of votes cast to approve relative to the total number of yes/no votes cast in connection with a proposal._ This does not include abstain votes. 
-- **Veto threshold**: The minimum number of OP votes required to be cast against a proposal, measured as _a % of the total votable OP supply, as of the start of the voting period.

A snapshot to determine voting power for each delegate will be taken at the commencement of a given voting period, and voting will be hosted on the Optimism Governance Portal.

A Citizens’ House governance proposal is **approved** if it satisfies the following minimum vote thresholds:

- **Quorum:** The minimum number of Citizen votes, including abstain votes, required to be cast in connection with a proposal. Here, a quorum is measured as _a % of the total number of Citizens at the start of the voting period.
- **Approval threshold:** The minimum number of Citizen votes required to be cast in favor of approving a proposal. The approval threshold for each proposal is measured as _a % of the total number of Citizens at the start of the voting period. This does not include abstain votes. 
- **Veto threshold:** The minimum number of Citizen votes required to be cast against a proposal, measured as _a % of the total number of Citizens, as of the start of the voting period.


Depending on the Proposal Type, exact quorum and approval threshold requirements may vary. For more information, refer to the proposal types below.

If a non-grant proposal is submitted for a vote and does not pass, the proposal will not be executed. If a proposal author wishes to iterate on a proposal that has been rejected, they should:

1. Create a new proposal thread on the Forum.
2. Include a link to the first proposal that did not pass.
3. Clearly identify what has changed in the new proposal.

### **Veto Procedure**
The next step in developing the Collective’s bicameral governance system is empowering the Citizens’ House with select veto rights. In Season 5, the Citizens’ House will be able to veto protocol upgrades that have been approved by the Token House. The Citizens’ House will have a one week period, directly following the Token House voting period, to veto any approved protocol upgrade. Citizens may veto by casting a veto vote via the  [Citizens’ House Snapshot Space.](https://snapshot.org/#/citizenshouse.eth) Veto thresholds are specified for proposal types as outlined below. Please note veto thresholds may be adjusted iteratively. 

Casting a veto is a serious decision. If a proposal approved in the Token House is vetoed by the Citizens' House, the proposal will not be enacted. In the case of Protocol Upgrades, vetoing may have serious consequences on engineering timelines and milestones. Proposals that may be vetoed by the Citizens' House have already been evaluated and approved by the Token House, which has been entrusted with primary responsibility over that proposal type. A Citizens' House veto may be appropriate if a proposal is believed to be malicious or to have been passed by a compromised Token House (either captured or acting out of self-interest rather than the Collective interest.)

### **Valid Proposal Types**

All v0.3 governance proposals must fall within one of the following categories:
- Governance Fund 
- Protocol Upgrade
- Inflation Adjustment
- Director Removal
- Treasury Appropriations
- Code of Conduct Violations
- Collective Council or Advisory Board Member Removal 
- Council Dissolution
- Rights Protections
- Elections 
- Ratification  
- Reflection Period 


The different requirements for submission and approval of each Proposal Type are summarized below.  If a specific template is not specified below, proposals should follow this [standard proposal template.](https://gov.optimism.io/t/standard-proposal-template-optimism-token-house/5443) Additional proposal types may be added in future Seasons. 

All Mission Applications are processed by either an elected Grants Council or the Foundation. Mission Applications should follow the process outlined on each individual Mission Request.

|Proposal Type|Proposing House|Description|Submission Requirements|Vote Duration|Quorum|Approval Threshold|Veto Threshold|Veto Rights|
|--------------------------------|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|------------------------------------------------------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
|Governance Fund      |Token House| The Governance Fund may be used to support development of the Collective and/or growth of the ecosystem.|Forum + On-Chain Voting                                                                                                                                                                                                                                                                                                                 |Two-week review period plus one week voting window|30%|51%|N/A|N/A| 
|Protocol Upgrade                |Token House| Scheduled changes to the on-chain smart contracts comprising the mainnet Optimism protocol. Please reference the [Framework for Protocol Upgrades](https://github.com/ethereum-optimism/OPerating-manual/blob/main/Framework%20for%20Protocol%20Upgrades.md) to understand when governance approval is required.	                                                                                                                                                                                                             |Forum + On-Chain Voting                                                                                                                                                                                                                                                                                                                                                          |Two-week review period plus one week voting window                  | 30%                                                   | 76%|30%|Citizens' House|                                                                                |
|Inflation Adjustment            |Token House|Changes to the inflation rate of newly minted OP (currently capped at 2% annually)                                                                                                                                                                                                                     |Forum + On-Chain Voting. Proposals should follow [this template](https://gov.optimism.io/t/inflation-adjustment-proposal-template/5923).                                                                                                                                                                                                                                                                                                                                                         |Two-week review period plus one week voting window                          |30%                                                   |76%|TBD|Citizens' House|                                                                                 |
|Director Removal                |Token House| Removal of a director of the Optimism Foundation                                                                                                                                                                                                                                                       |Forum + On-Chain Voting                                                                                                                                                                                                                                                                                                                                                         |Two-week review period plus one week voting window                     |30%                                                   |76%|N/A|N/A|                                                                                |
|Treasury  Appropriations        |Token House| The amount of OP the Optimism Foundation may spend or distribute annually, beginning in Year 2 of its existence (the Year 1 budget is 30% of the initial total OP supply)                                                                                                                              |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                  |Two-week review period plus one week voting window                    |30%                                                   |51%|N/A|N/A|                                                                                |
|Rights Protections              |Token House|OP holders must consent to any changes to the founding documents of the Optimism Foundation, if those changes would materially reduce their rights                                                                                                                                                     |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                  |Two-week review period plus one week voting window                      |30%                                                   |51%|N/A|N/A|                                                                                |
|Code of Conduct Violation              |Token House| Token House Code of Conduct violations will be processed by the Code of Conduct Council, subject to veto by the Token House.                                                                                                                                                  |Proposals to be initiated by the Token House Code of Conduct Council outlining any enforcement actions.                                                                                                                                                                                                                                                                                                                             |Two-week review period plus one week voting window                     |N/A                                                  |N/A|12%|Token House|   
|Collective Council or Advisory Board Member Removal| Token House| Collective Council or Advisory Board members may be removed from their position for failing to uphold the responsibilities outlined in the relevant Charter or to act with honesty, integrity, and transparency.| Forum + On-Chain Voting.| Two-week review period plus one week voting window|	30%|	51%|	N/A	|N/A|
|Council Dissolution              | Token House|A persistent Council may be dissolved if it is no longer fulfilling its Charter                                                                                                                                                    |Forum + On-Chain Voting                                                                                                                                                                                                                                                                                                                                  |Two-week review period plus one week voting window                     |30%                                                   |51|N/A|N/A| 
|Ratification          | Token House|Ratification of governance documents                                                                                                                                                   |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                  |Two-week review period plus one week voting window                     |30%                                                   |51|N/A|N/A| 
|Reflection Period Proposals (including elections)           | Token House|Experiments with new governance structures, programs, and/or processes                                                                                                                                                 |Proposals to be initiated by the Foundation                                                                                                                                                                                                                                                                                                                                |Two-week review period plus one week voting window                     |30%                                                   |51|N/A|N/A| 

The Proposing House column will be updated to include Citizens’ House, for relevant proposal types, when those proposal types become valid in the Citizens’ House. Veto thresholds may be adjusted iteratively. 


### **RetroPGF Rounds**
Citizens’ House governance includes RetroPGF, which involves voting and disbursements occurring over a series of “rounds.” In each RetroPGF round, the Citizens’ House votes to retroactively reward public goods projects that have provided substantial impact. 

RetroPGF rounds are run according to the following process:

- Scoping:  The overall amount of rewards to be allocated and scope of impact are defined at the outset of the round.  
- Application creation:  Projects are invited to create an Application in the [RetroPGF Application Manager.]((https://app.optimism.io/retropgf-signup)) 
- Application Review: Applications are reviewed for adherence to the application rules
- Voting:  Votes are collected from the citizens with the requisite [AttestationStation](https://community.optimism.io/docs/identity/schemas/) entries and tallied. 
- Disbursement:  Based on the simple weighted average of the Citizens’ House vote, the overall reward amount for the round is divided among the winning projects. 
- Compliance: The Foundation will collect information from projects in order to distribute the grant in a legally compliant manner (including completing KYC).

Additional information on the process for RetroPGF Round 3 is available [here.](https://community.optimism.io/docs/governance/retropgf-3) 


## **Implementation and Administration**

In all cases, Optimism Collective governance is intended to be carried out consistent with the terms of its [Working Constitution](https://gov.optimism.io/t/working-constitution-of-the-optimism-collective/55), the spirit of both the [Rules of Engagement](https://gov.optimism.io/t/rules-of-engagement/5/3) and the [Code of Conduct](https://gov.optimism.io/t/code-of-conduct/5751), and the pursuit of its [Optimistic Vision](https://www.optimism.io/vision). The Optimism Foundation will steward this process as described below.

**Administration**

The Optimism Foundation will facilitate the administration of the governance procedures described in this Operating Manual with the aim of ensuring that members of the Collective may participate thoughtfully in governance. Such administrative services may include:

- Moderation of governance proposals to ensure they are validly submitted and voted upon;
- Removal of proposals that reasonably appear to be fraudulent, spam-oriented, defamatory, hateful, or otherwise inappropriate or inconsistent with the values of the Collective;
- Monitoring of votes, voting power, the votable token supply, and voting periods for purposes of determining whether quorums and approval thresholds are met or accurately reflected;
- Management of mutually contradictory proposals that are submitted simultaneously or in close proximity to one another;
- Administration of network maintenance, such as emergency bug fixes or release rollbacks (with or without a governance vote); and
- Such other things as the Foundation deems appropriate in connection with the above.

**Implementation**

Approved governance proposals will be routed to the Optimism Foundation for implementation.

Upon receipt of an approved proposal, the Optimism Foundation will determine whether the proposal is safe, secure, consistent with the purposes of the Foundation and the Collective, and capable of being implemented in a legally compliant manner (including completing KYC).

- If it is, the Foundation will act diligently and in a commercially reasonable manner to cause the proposal to be implemented.
- If it is not, the Foundation may remove the proposal for resubmission or cause the proposal to be implemented with certain guardrails, at its discretion, and coupled with an explanation to the Collective as to why the proposal was rejected or limited.

The Optimism Foundation will undertake this ministerial work with a view towards increasingly decentralizing its role over time.

### **Amendments**

The procedures described in this Operating Manual will go into effect as releases are published on GitHub. Major releases to the manual will be made in connection with a series of governance experiments (“Seasons”). These changes include but are not limited to the expansion of the Citizens’ House, and adding, removing, and modifying Proposal Types and rules relating to voting processes. Any non-clerical updates to the Operating Manual will be reflected with a new version number at the top of this document, at which point the updated version will go into effect.

## Process TLDR
- Proposals are reviewed over a three week voting cycle.
- If you’re submitting a Mission Application, you’ll need to submit your application as outlined on each individual Mission Request.
- For all other proposal types, you may draft a proposal based on this template and post it on the Forum with [Draft] in the title for feedback. Delegates and/or Citizens will provide feedback on your proposal in the forum. Use your judgment to incorporate feedback.
- Once your non-grant proposal has been approved by four top 100 delegates or four Citizens add a link to your proposal to the Voting Cycle Roundup thread by the last day of Week 2 and update the title from [Draft] to [Final]. These proposals will move on to Week 3 voting.
- Protocol Upgrades approved by the Token House, must also pass the Citizens’ House Veto Procedure, as outlined in the Veto Procedure section above, before they are considered officially approved. 
- The Security Council will enact officially approved Protocol Upgrades. The Optimism Foundation will facilitate the administration of all other approved proposals, including by distributing any approved OP grants. The Foundation will be in touch to collect additional information from your project in order to execute the proposal or grant, including information to perform KYC. 
- If your proposal is passed, the Optimism Foundation will facilitate its administration, including by distributing any approved OP grants. The Foundation will be in touch to collect additional information from your project in order to execute the proposal or grant, including information to perform KYC.
- If your proposal fails, you can make a new proposal in the next cycle specifying how you have incorporated significant changes from your first proposal.


#### The Citizens’ House also manages the allocation of RetroPGF:
- Citizenship is currently temporary, with the RetroPGF Round 3 Citizens recorded via entries in the AttestationStation. 
- RetroPGF rounds occur in intervals and according to a predefined process, which currently includes phases for scoping, application creation, application review, voting, and disbursements. The Foundation will collect information from projects in order to distribute the grant, including information to perform KYC.

