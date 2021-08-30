IGP#3 - DSL September 2021 Upgrade

### Summary of Code Changes:
- Modifies the ‘votingDelay’ parameter and sets it to 2 days (~13140 blocks).
- Modifies the ‘votingPeriod’ from 2.63 days (~17280 blocks) to 3 days (~19710 blocks).
- Adds support for ERC-721 and ERC1155 SafeTransfers
- Adds ‘Beta Mode’ to the base implementation

### Description
This is an update to the DeFi Smart Layer that includes several changes and updates:

#### Modifying Voting Parameters:
Currently when on-chain proposals are submitted, the voting period begins immediately and users need to delegate and assign voting power before the vote goes on chain. Adding a 2 day voting delay will allow INST tokenholders to delegate and assign voting power after a proposal is submitted on chain and will help increase voter participation. The Voting Period is currently set to slightly above 2.5 days, this will modify the voting period to 3 days.

#### Adding Support for ERC-721 and ERC-1155:
This update will update the base implementation for both ERC-721 and ERC-1155 by adding functions ERC721Received(), ERC1155Received(), and ERC1155BatchReceived(). This will enable better handling and usage of these standards across all DeFi Smart Accounts.
Code Change: https://github.com/Instadapp/dsa-contracts/pull/48

#### Beta Mode:
This update adds Beta Mode to the base implementation. This will allow DSA owners to enable ‘Beta Mode’ which will grant that account access to upcoming and experimental features which are not enabled by default when creating an account.
Code Change: https://github.com/Instadapp/dsa-contracts/pull/42

Main PR with all the updates combine:- https://github.com/Instadapp/dsa-contracts/pull/50
