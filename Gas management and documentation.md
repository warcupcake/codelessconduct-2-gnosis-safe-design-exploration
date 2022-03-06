# Gnosis Safe: Gas Management and Documentation

Currently, as part of the User Experience on Gnosis safe, the cost of transaction is gas can be managed only at execution of the contract at the last user of the M of N approval.
In performing a transaction or smart contract contract interaction, the process is currently as follows:
  
  1. A user initiates the transaction/contract interaction.
  2. The M of N confirmation approval triggers for the rest of the users.
  3. The last confirmation triggers the transction/contract interaction "Execution".

The last confirmation of the M of N has a choice to "execute" at confirmation, or opt-out of the "execution" and leave the gas payment and of the transaction to another user.

###### Workflow Visualization:

<img width="1270" alt="Screen Shot 2565-03-06 at 11 58 08" src="https://user-images.githubusercontent.com/97900684/156909862-a8193a93-752b-4e4f-a4e9-0abd59e4c68d.png">

# Problem: Off-chain Delegation of Execution and Gas Payment

From the perspective of an enterprise, business, or collective, the lack of on-chain delegation of gas payment poses a degree of risk from human error and unclear responsibility delegation.

###### Example:

A small centralized asset management firm manages their clients' funds through gnosis safe and has 3 directors who are Users of a Gnosis Safe. 
- Due to their company policy evolving around their clients confidence, the M of N is set to 3 of 3.
- Their investment strategy involves arbitraging during highly volatile markets and therefore usually pays overestimates their gas estimation to ensure transaction confirmations during high gas fees.


The question comes to mind of who of the 3 directors shall pay the gas fees? If the answer is "whoever executes last" then that strategy has a few unpredictable dependencies especially during highly volatile markets. This includes:
- Each director having a sufficient amount of ETH in their wallets.
- In topping-up - the availability of centralized exchanges or fiat on-ramps.
- In execution - The director's gas configurations in execution. 

Of course, the solution to this example can be addressed off-chain if the Users are well communicated, educated, and governed, but as improvement to welcome enterprises and businesses onto Gnosis safe, the platform should allow for clear delegation of responsibility through a dedicated **Gas Vault, Dashboard, and Policies**.

# Solution: Dedicated Gas-Vault and Dashboard

Firstly, there might be a question of "why not use the eth in the Gnosis Safe?". The answer here is simply that the balance of the gnosis safe should represent the available capital in assets, tokens, and NFTs. For businesses (and their customers) it wouldn't be efficient or convenient to communicate and manage the value of their assets with "Plus or minus a few 100$ of gas."

To address the unpredictability of the current execution workflow, a simple option for a gas vault is proposed. The gas vault can be a generated addressed facilitated by Gnosis Safe or an address of the User's choice. A simple seggregated address to store and spend gas will allow the users to manage their gas spendings and also relieve them of the burden of paying for gas with their own funds.

Some properties of the gas vault that should be be included or translated from the normal Gnosis Safe includes:

- Whitelisted withdrawal addresses for emptying ETH
- M of N confirmation for withdrawals and whitelisting
- Configurable execution gas price - preconfigured at initiation, last confirmation, or auto-calculated at execution.
- Option to generate the vault at creation of the Gnosis safe or later added/generated from the main dashboard.

###### UX Flow of Gas Vault Generation:

<img width="1191" alt="Screen Shot 2565-03-06 at 19 24 57" src="https://user-images.githubusercontent.com/97900684/156923028-4b3331a4-7fc1-423c-b7a5-6b164c46aa2a.png">


