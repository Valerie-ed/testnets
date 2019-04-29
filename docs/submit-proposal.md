# Submit Proposal

- Any user can deposit some tokens to initiate a proposal. After the deposit reaches a certain value of min_deposit, the proposal enters the voting period, otherwise the deposit period will be retained. Others can submit proposals in the deposit period. Once the total deposit amount reaches min_deposit, then enter the voting period. However, if the freeze time exceeds max_deposit_period during the deposit period, the proposal will be closed.
- Proposals that entered the voting period can only be voted by validator and delegator. The vote of the un-voted delegator will be the same as the vote of validator, and the vote of the voted delegator will be retained. When you reach "voting_period", the number of votes will be counted.

## How to submit governance proposal?

You can submit a governance proposal by using the following command:

```bash
hashgardcli gov submit-proposal \
     --title=${proposal_title} \
     --type=${typ} \
     --description=${desription} \
     --from=${wallet_name}
```

Submit the blockchain governance proposal and the initial deposit of the proposal, where the proposed types includes: Text/ParameterChange/SoftwareUpgrade.

If the proposal does not get to the voting period, you will also need to activate the proposal via [mortgage deposit](deposit.md)

After the proposal goes to the voting period, you can proceed with [Proposal Voting](vote.md)

