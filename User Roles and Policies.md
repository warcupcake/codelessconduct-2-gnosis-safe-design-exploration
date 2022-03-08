# Gnosis Safe: User Roles and Policies

Currently, Gnosis Safe Users are equal in rights to the Gnosis Safe in terms of initiating, confirming, and executing transactions. 
At the same time, during the M of N transaction confirmations, there are no particular order in which Users have to confirm the signing, with the last confirmation having the choice of executing the transaction.

The lack of User Roles in participating in the creation and execution of the transaction makes for a loose governance framework for the Gnosis Safe which may not be ideal for enterprises users who usually prefer clear roles and responsibilities.

# Problem: Off-Chain Roles Unrepresented On-Chain

While equal rights and power for a decentralized organization may seem simple enough to govern, traditional or larger organizations may not feel as comfortable with no roles or guidelines in place to govern large transactions.
Not to mention - for regulated enterprises and businesses, checks and balances including clear job descriptions and roles in executing transactions are usually required to be in place for the business to be licensed or allowed to conduct business.

Not having this differentiation of roles in transacting on the blockchain may result in Users having to develop their own governance framework in order to comply with business and licensing requirements.

###### Example:

A firm managing their clients' assets on chain requires at least 3 people to fully execute a transaction. 1 person to initiate, 1 to confirm, and 1 to confirm AND execute. The current Gnosis Safe workflow allows for this however it does so without a built in tool to enforce these designated roles.

**The illustrate how these roles are neccesary, take the following scenario:** The 3 people required to complete transaction may be required to represent 3 different business functions.
The initiator is from a client-facing team that takes in the clients' transaction requirements, ie. where to send funds or what swaps to make. The initiator is able to be stationed at an office and has access to the Gnosis Safe platfom via a laptop computer. 
The approver of the confirmation in the middle is from the management team who is constantly movign from one meeting to another with only a smartphone to confirm transactions.
Lastly, the last confirmation and executor of the transaction is from the accounting or finance team who require to make decisions on gas fees and record the relevant expenses.

# Solution: User Roles

An effective way to handle roles and assigned tasks is to create a configurable role and task matrix. Inspired by the roles and rights of regulated custodians, configurable user matrices can allow for Users to be able to apply and enforce their own business requirements under pre-defined constraints that is specific for Gnosis Safe.

The idea here is to allow Users to be able to generate roles and allow each role specific tasks during a transaction. The main tasks that would require assignment to a User Role includes:

- Transaction Initiation
- Transaction Approval/Confirmation
- Transaction Execution

With these 3 tasks, many combinations of roles can be created to tailor to each Gnosis Safe needs.

For the given example above, the user role and task matrix would look like the following:

<img width="1150" alt="Screen Shot 2565-03-07 at 23 38 59" src="https://user-images.githubusercontent.com/97900684/157077664-c851addc-397a-46cd-8b12-c91b88edca95.png">

By separating user roles through clear task assignments, users are allowed to create combinations of workflows and policies revolving around the tasks and custom roles.

**Take for example a few scenarios:**

1. Users want a dedicated transaction initiator and executor to be the same person. Let's call this role a Transaction Manager.

<img width="1104" alt="Screen Shot 2565-03-07 at 23 48 52" src="https://user-images.githubusercontent.com/97900684/157079447-05f20fe4-f3f7-4aa6-9e87-6668b7190ed6.png">

2. Users want anyone to be able to initiate with only 1 executor who manages gas fees. Let's call this role Gas Manager.

<img width="1130" alt="Screen Shot 2565-03-07 at 23 50 33" src="https://user-images.githubusercontent.com/97900684/157079775-ac842f26-7b2d-4a89-82e8-5afa0f7ebf7a.png">

In implementing these roles and assigned tasks, the initial M of N approval accouts should be signed.

## Transaction Policies

By introducing User Roles and their assigned tasks to Gnosis Safe, Users are able to formulate their own transaction policies to govern their transaction process.

Transaction policies are an important aspect in delegating tasks and order of execution to ensure good practice. With the key tasks in processing transactions defined above, user roles can be created to form transaction policies. With User Roles, groups of Users can be formed to perform certain tasks.

###### Example:

Imagine a DAO that executes transactions based on quorum or governance of the DAO's community. To efficiently execute these transactions, Users who manage the community may be given the Initiator role to start transaction processes. However, the approval of that transaction may be given to a different group of Users who perform final checks on the transaction before the transaction is broadcasted onto the blockchain. 

This approval group may be a set of Users whose sole purpose is to approve transactions without access to initiate or execute the transaction. This reduces the risks of multi-sig owners going rogue and approval transactions for their own benefit without the approval of the enterprise, DAO, or community.

Lastly, along side the proposed **Gas Management** mechanism, another User Role or Group can be created to solely manage the gas expenses for the community.

In this example, the roles are pre-defined and follow a secure policy that allows the transactions from the Gnosis Safe to be predictable and organized.

## Conlusion

By defining the key actions and tasks required to process a transaction on Gnosis Safe, it is possible to delegate these tasks to specific Users or addresses to allow Users to create and govern their own enterprises in a way that is suitable for them and each User's appropriate responsibility. This added complexity onto the Gnosis Safe transaction process will allow for a more secure and confident experience for Users that require them, as well as given Users who need clear delegation of tasks the ability to do so on-chain.

No doubt in the coming months and years, enterprises, businesses, and larger communities will require more than just a multi-sig, but also a secure and structured way to govern the signing process as well.

