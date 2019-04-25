# Vote

After the proposal is officially activated, you can vote on this proposal

 You can determine if you have entered the voting period by looking at the details of the proposal:

  ```bash
Hashgardcli gov proposal ${proposal_id} --trust-node
  ```

 In the result, ``` proposal_status ``` is the status of this proposal.

 If you are in the voting state, you can vote by doing the following:

  ```shell
Hashgardcli gov vote ${proposal_id} ${option} \
    --chain-id=hashgard \
    --from hashgard
  ```

Need to specify the voting id ```${proposal_id}```, and the voting option ```${option}```, options include: 

  - Yes
  - No
  - NoWithVeto
  - Abstain
