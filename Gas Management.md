# Gnosis Safe: Gas Management

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

Of course, the solution to this example can be addressed off-chain if the Users are well communicated, educated, and governed, but as improvement to welcome enterprises and businesses onto Gnosis safe, the platform should allow for clear delegation of responsibility through a dedicated **Gas Vault and Dashboard**.

# Solution: Seggregated Gas-Vault and Dashboard

## 1. Gas Vault

Firstly, there might be a question of "why not use the eth in the Gnosis Safe?". The answer here is simply that the balance of the gnosis safe should represent the available capital in assets, tokens, and NFTs. For businesses (and their customers) it wouldn't be efficient or convenient to communicate and manage the value of their assets with "Plus or minus a few 100$ of gas."

To address the unpredictability of the current execution workflow, a simple option for a gas vault is proposed. The gas vault can be a generated addressed facilitated by Gnosis Safe or an address of the User's choice. A simple seggregated address to store and spend gas will allow the users to manage their gas spendings and also relieve them of the burden of paying for gas with their own funds.

### 1.1 Gas Vault Generation

In setting up the Gas Vault, Users should have the option to generate the vault at creation of the Gnosis safe or later added/generated from the main dashboard. A high level UX flow in opening a Gas Vault for the Gnosis Safe is presented below:

###### UX Flow of Gas Vault Generation:

<img width="1191" alt="Screen Shot 2565-03-06 at 19 24 57" src="https://user-images.githubusercontent.com/97900684/156923028-4b3331a4-7fc1-423c-b7a5-6b164c46aa2a.png">

Once generated, all gas for transactions from the Gnosis Safe should be paid with the ETH in the gas vault. Therefore, the Users who are confirming transactions are freed of the burden to handle funds and potentially allow them to have a single and consistent approval workflow experience.

With a seggregated vault for managing gas, the Users are able to direct their deposits for ETH as well as monitor and configure the usage of gas. Imagine a business with strict accounting and reconciliation measures; a single source of fund (the gas vault) for on-chain transaction costs will be much easier to manage for an accounting or financing team. With a seggregated gas vault address, the Users and their business can also directly monitor and top-up their gas balances according to their business requirements. This also allows better visibility and traceability of business expenses for gas fees.

### 1.2 Gas Vault Properties

Some properties of the gas vault that should be be included or translated from the normal Gnosis Safe includes:

- Whitelisted withdrawal addresses for emptying ETH
- M of N confirmation for withdrawals and whitelisting
- Configurable execution gas fees - pre-configured, on last confirmation, or auto-calculated at execution

The configuration of these properties should be accessible through the **Dashboard** mentioned earlier, which will be further described.

### 1.3 Gas Settings and Transaction Execution

Now that there is a seggregated Gas Vault, the question still remains: How then, do we manage the configuration of gas fees and limits?

There are mainly 2 ways to practically configure gas fees, each with their own pros and cons depending on what the Users will want to prioritize: **Convenience or Control**
  
- **Convenience: Gas fees and limits are automated depending on the current gas prices**

Allowing Gnosis Safe to automate the gas fees akin to the style of MetaMask is a great way to streamline the transaction approval process by the Users and provide them with a consistent user experience in making transactions. Other than the initiator, everyone signing in the M of N approval will have the same predictable experience in signing transactions without having to worry about making decisions according to the current gas prices.

However, the risk here is the lack of visibility in gas costs that will incur onto the Gas Vault.

Configuring this is should be done prior to transactions on the **Dashboard**. In terms of User Interface, there should be a toggle and simple choices of Slow, Standard, and Fast selections. After the confirugation is finalized, the M of N confirmations should be signed to enable the automation.

With the gas fees and limits automated according to the current gas prices, the transaction execution is streamlined for the Users to initiate and approver transactions without encumbrance of decisions around gas.

- **Control: Gas fees and limits are configured by the last confirmation of the M of N approvals.**

Reasonably, automating gas fees can be a risk for highly volatile market conditions, and therefore the Users may still want to maintain the customization of gas for execution.

For this, the most reasonable place to customize is at the last confirmation of the M of N prior to the transaction being sent out onto the blockchain. With this, in terms of user experience, the initiation, confirmation, and execution of the transaction remains very much the same to the current process offered by Gnosis Safe, with the exception of the gas fee being paid from the Gas Vault, and not the User who performs the last confirmation.

This re-introduced the unpredictability of the User who performs the last confirmation. Will they be able to make the right choices in predicting and configuring the gas fee for the transaction? Depending on who in the M of N is last, the results here is still dependent on their individual familiarity with Ethereum gas prices and fee settings.

Ideally, a designated gas manager should be the last to confirm this transaction and make the decision based on the current gas prices. Currently, this is not able to be governed with Gnosis Safe and relies on off-chain dependencies. This is explored further in the **Transaction Policies** page of this hackathon submission.

## 2. Dashboard

Other than a seggregated Gas Vault that allows for the Gnosis Safe to be better at delegating gas payments, Gnosis Safe should also allow for easy access and management of the gas vault through a dashboard that includes the Gas Vault's balances, previous transactions, and gas settings. The gas settings section of the dashboard was already mentioned prior in **1.3**. 

This dashboard should be available and accessible as an additional page on the main menu bar on the left.

The dashboard should also notify the Users of the historical gas data, to consolidate the essential data required to make decisions in topping up ETH, and gas settings for transactions.

Finally, customized alerts or push notifications through the mobile-app can be a quality-of-life add-ons that will allow Users to have better awareness of their readiness in executing transactions.

# Conclusion:

The addition of the Gas Vault and Dashboard's can introduce an option to streamline the approval and transaction process of the Gnosis Safe while also giving Users tools to fairly manage expenses from incurring gas fees on the ethereum blockchain. For businesses and enterprises, clarity and visibility of expenses are an important aspect of management that no doubt will have to be addressed if Gnosis Safe is to position itself to onboard more enterprise users.
