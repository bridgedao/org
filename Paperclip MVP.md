# Paperclip MVP
Participants in the Paperclip system are:  
*Node* - IBAN account holder  
	executes transactions on behalf of the Coordinator for a fee
*Coordinator* - DAO (or any other more or less centralized organization that instantiates the system)
	facilitates all the transactions, manages deposited collateral and fee payouts  
*User* - user of services  
	transacts with other users or DAO, pays the fee  
*Services* - banks, etc.  
	provide platform for fiat transactions for a fee  
*Arbitrator* - dispute resolution service  
	solves any disputes for a fee - possible collaboration with Kleros or Aragon decentralized court  
*Oracle* - source for off chain transactions verifications   
	provides confirmation of fiat transactions for a fee

Paperclip enables a Coordinator to facilitate fiat transactions on behalf of Users by commissioning and paying Nodes to execute these transactions using their own bank accounts (Services). This enables any entity to use services without having to use their standard interface. Explicitly, a business doesn’t need a bank account or any other relationship with a bank to transact with electronic fiat money. This service at its base is legislation agnostic, but rules and actions can be implemented which would enable AML and KYC compliance if necessary.

Any IBAN account holder can become a node by putting in a collateral which is stored on-chain and controlled by Coordinator. At any given time, a node cannot hold more fiat currency (of other users) than what she has at stake. 

When a user wants to use the network for a transaction, the Coordinator will give her the details for payments with a reference number, the amount and the node’s IBAN. When money is deposited, the participating node gets the instruction for further payment. Instruction is given in a form of ticket which expires in 5 min. To fulfil the order, a node needs to confirm it and manually make the payment in next 5 minutes. 
A node earns money in these ways:
* transaction fee (similar to bitcoin fees)
* holding fee (determined by the Authority according to goals)
The system automatically generates all the tax and legal documentation for the Nodes.

This solution doesn’t even have to use PSD2 open banking APIs.

## User stories
With enough adoption, this would result in a DAO with hundreds of delegated personal IBAN accounts in dozens of different banks being controlled by the DAO. This allows for the following scenarios:

### Example 1: DAO receives fiat
User named Joe wants to make a payment to DAO in EUR. Joe makes a request on the DAO website or mobile app to pay in EUR. DAO calls Paperclip app to arrange the payment. In the same app, Joe selects the amount, bank of sender, max fee and any other detail. Paperclip observes all available nodes and picks the most convenient one to receive the payment. Joe is given instructions to send money to IBAN account of that node with a specific reference code. Once a payment is detected on that IBAN with that reference code, Paperclip sends the confirmation to the DAO, node and Joe.

*KYC/AML concerns:* Joe might be required by the bank of sender to identify himself. He should be able to do. It could be problematic for exchanges use this service if they don’t perform KYC on their customers. The money that gets into Paperclip system should be from the original sender.
 
### Example 2: DAO sends fiat
Another user, Joanna wants to receive a payment from DAO in EUR. Joanna makes a request on DAO website of mobile app to receive payment in EUR. DAO calls Paperclip app to arrange the payment. The call includes the amount, bank of receiver, max fee and any other detail. Paperclip checks if DAO has enough balance in the system to make that payment. If DAO has enough balance (let’s say it kept euros it received from Joe and that it is enough), Paperclip observes all available nodes and picks the most convenient one to make the payment. The node is given instructions to send money to Joanna’s IBAN account with a specific reference code. Once a payment is detected on that IBAN with that reference code, Paperclip sends the confirmation to the DAO, node and Joanna.

*KYC/AML concerns:* There are reasonable concerns here if DAO sells cryptocurrency on an exchange to receive EUR. Paperclip doesn’t enable money laundering activities and this is the reason why origin of the money should be traceable.

*Issue:* What if DAO operates with a large quantity of cryptocurrency which doesn’t have provable origin?

### Example 3: DAO holds fiat
Once DAO has received a fiat payment in the Paperclip system, it’s total balance is visible through Paperclip app. The money doesn’t lay on a certain IBAN or in a certain bank. Rather, it is the credited against the whole Paperclip supply. This makes it impossible for an external actor to block DAO from operating with fiat without shutting down the whole Paperclip system.

Through the above examples, we clearly demonstrate the power of a distributed network of IBANs managed through smart contracts with the help of some Oracles (external data input) to facilitate a global exchange of assets and value, bypassing current limitations while remaining well within the legal framework of most if not all countries.

## Additional thoughts
Ideas for improving robustness:
* diminishing returns for nodes would incentivise many nodes with small transaction volume
* balancing out the accounts regularly (also for better liquidity)

### Advantages:
Paperclip can be implemented now. It can be the first version of DAObank base layer with second iteration using PSD2 opportunities. It uses economic incentives for participants and avoids any kind of registration or authorisation by protocol providers (banks, government). It cannot be stopped easily. It cannot be traced easily. It is scalable. 

### Limitations:
There is a lower threshold for transaction fee. It is the cost of bank transaction and cost of time node spends on executing the transaction. This will make it hard to execute small transactions. Nodes might have to spend time raising transaction limits and things like that which banks put in place. Participation is limited to those who have enough money to put in deposit (stake). 
