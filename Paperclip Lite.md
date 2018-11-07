# Paperclip Lite
*_Trustless fiat interface for popular common business services and expenses of smart contracts._*  

## Description
It enables smart contracts to sell their services and pay their business expenses using traditional banking system without need for interacting with one, trusted, “real-world entity” or a financial institution. Paperclip Lite is not a legal entity, it is an Ethereum dapp which controls a distributed network of incentivized proxies called nodes. Nodes, physical and legal persons, are able and willing to facilitate fiat transactions using their own IBANs in an exchange for a fee.  

All transactions are IBAN to IBAN only.  

### Transaction flow:  
1. Smart contract sends a request to Paperclip for an IBAN to which it’s customer can make a payment. The request includes IBAN of customer, invoice for the service and payment amount.
2. Paperclip finds most suitable node in the network and gives it’s IBAN to the smart contract.
3. Smart contract then gives this IBAN to their customer for them to make the payment from their IBAN.
4. When customer makes the payment, she sends a confirmation to the smart contract which forwards it to Paperclip.
5. When a node gets the funds from the customer, it sends a confirmation to Paperclip.
6. When Paperclip gets both confirmations, it increases the balance of smart contract for the amount received and pays the fee to the node.
7. When smart contract decides to spend this balance. It sends an instruction to Paperclip with IBAN account of the contractor, invoice for the service and amount to be paid.
8. Paperclip first checks the balance and looks for any active limitations. If everything is ok, it finds the most suitable node and gives it an instruction to make the payment.
9. When node makes the payment, it sends confirmation to Paperclip. When contractor receives the payment, it sends the confirmation to smart contract which forwards it to Paperclip.
10. When Paperclip gets both confirmations, it decreases the balance of smart contract for the amount sent and pays the fee to the node.

## Services and expenses
Paperclip will only accept and facilitate transactions for a given types of services and expenses. Supported services are particularly hand picked to decrease the risks of damage and liability to the parties involved.

### Types of services supported:
1. Subscriptions (example: UJO music streaming, Aragon payroll and accounting service or DAOs)
2. Licenses
3. Gas costs (example: Gnosis Safe account creation, Aragon DAO creation)
4. Consumable assets of small value (example: Kickback event tickets)

### Types of expenses supported:
1. Salaries
2. External services (spendable or with short expiry date)
3. Software licenses (AWS, Mailchimp, Google, etc.)
4. Utilities (electricity, water, internet, phone bills…)
5. Rent
6. Legal
7. Travel (tickets, per diems, insurance, accommodation)
8. Marketing (advertising on Google, Facebook)


### Paperclip does not:
1. receive, sell or keep cryptocurrency, besides the locking/unlocking the collateral of the nodes;
2. facilitate currency exchange of any kind;
3. facilitate purchases of valuable assets, illegal, risky, non-common or unknown services;
4. accept any kind of payment which is not IBAN to IBAN, strictly no cash or crypto payments;
5. facilitate transactions to unknown, risky or illegal suppliers;
6. provide services to unknown smart contracts;
7. facilitate donations, transfers, liquidations or remittances;
8. hold funds of physical or legal persons;
9. conduct any actions which might be deemed as money service business actions

## Participant protection
Paperclip Lite is optimized for protection of all participants: creators, smart contracts, customers, suppliers, nodes and banks.

Foremost, Paperclip does not support services which have a high risk of customer disputes. Additionally to narrowing down the supported services and expenses to those of least risk and most common ones, we are able to employ a number of other protection mechanisms.

### Reversible transactions
Smart contracts funds are available for spending only after the consumer, node and smart contract have agreed the service was successfully and fully provided and/or the date for appeal has passed according to Terms of use.

However, we will decrease the need for this by providing service only to those smart contracts which provably successfully deliver their service.

### Damage liability
Every smart contract could have insurance for cases of damages arising from the usage of services sold. 

However, we will only support services which cannot cause any significant damage to the customer or node. This way the value of potential damage is limited to the amount paid for them. This amount will be covered by smart contract insurance or collateral.

Invoices and transaction details are kept for eventual inquiry of authorities, and for dispute resolution.

### Fraud prevention
Nodes stake DAI as collateral. This collateral is in the control of Paperclip DAO and can be taken away in the case of fraudulent behaviour. Maximum transaction bandwidth of a node is limited by the value of their stake.
To further disincentivize fraud, nodes start with smaller bandwidth and increase it by successfully executing transactions. This creates a reputation system similar to Ebay and Amazon sellers.  In case of dispute, transactions of a node are halted and a dispute resolution services are used (real world court, Aragon court of Kleros).
If transactions are halted, node doesn’t collect any fees. This creates strong incentives for nodes to cooperate and, avoid and resolve disputes.

## Participant incentives
### Smart contracts
#### 1. Can save time and money.
By matching outstanding receivables and debts, costs of exchanges and gas fees are avoided. Also, no need to work with shady exchanges.

#### 2. Can increase their total addressable market.
Currently addressable market is everyone who is interested in their service and is familiar/uses cryptocurrency. Paperclip Lite enables them to offer their services to everyone who is interested in their service.

#### 3. Can get KYC/AML compliant funds
Since all the funds are already in the banking system KYC/AML compliance checks have already been performed for all the funds by the banks of the customers. No cash or crypto payments take place. Transactions are used exclusively to facilitate service purchases.
Don’t need to trust anyone (except Paperclip Lite code)
Dapp founders can set up a legal corporation and partner up with one bank to conduct these transactions, instead of using Paperclip API. The issue with this is that it is not trustless and it’s much more work.

#### 4. Can achieve a better UX
Users are already familiar with using their credit cards to make online purchases. Additionally, using meta transactions, we are able to enable users to use dapps without the need of having any cryptocurrency or token beforehand. They can just pay it with fiat. 

### Nodes
Earn fees for their work. They collect fees after they successfully execute a transaction and when they keep the funds in their account for certain amount of time.

### Suppliers
Can offer their services to smart contracts without accepting cryptocurrency.

### Customers
Can quickly and easily purchase services from smart contracts with fiat.

### Banks
Earn fees from transactions done using their network. Get a cut from the growing new dapp economy. Paperclip provides a way for banks to offer their services to dapps, DAOs and smart contracts without disrupting own position of platform for money transfers. Paperclip Lite doesn’t deal with the adoption of cryptocurrency, it is solely focused on fostering the adoption of smart contract services.

## Examples
### Example 1: Smart contract selling a service for fiat
Service: Aragon Network account creation
Seller: Aragon Network smart contract
Customer: Physical person

Customer wants to create an account on Aragon Network and prefers to pay this with fiat. Customer selects the service and proceeds to checkout where he is given the option of paying with their credit card. The payment will go from his IBAN account to the IBAN account of Paperclip Lite node. When the payment goes through, Aragon smart contract is notified so it can proceed with providing the service to the customer. The funds stay within Paperclip Lite network in the same currency and Aragon now has a spendable balance.

### Example 2: Smart contract paying a utility bill with fiat
Service: Electricity
Seller: Local utilities company
Customer: Aragon Network smart contract

Aragon Network smart contract has a balance on Paperclip Lite network. Seller prefers being paid in fiat currency. Smart contract decides to pay the service with his balance on Paperclip Lite network. Smart contract sends a message to Paperclip Lite with the invoice describing the service and supplier. Paperclip Lite then sends an instruction to the node to make the payment. When the node makes the payment, it sends the message to Paperclip Lite and this is then passed on to smart contract. 

## Possible improvements 
### Payment bounties
If the transaction is too big, Paperclip Lite can create a bounty on behalf of the smart contract. This bounty enables anyone to pay a bill for the smart contract. When they provide the proof of the payment, they get repaid by smart contract through Paperclip network with addition of the award.

### Smart contract collaterals
To ensure smart contracts follow the rules and for the protection of nodes and customers, smart contracts can be requested to put in a collateral. This can be even extended to other participants if neccessary (customers and suppliers).

### Clearing up the accounts
In case a large amount of currency is meant to be kept for longer period in Paperclip network, these funds can be used to purchase Government bonds with the least price volatility. Special, over-collateralized nodes can do this.

### Balancing out the accounts
When there is a mismatch between nodes that receive funds from customers (inflows) and nodes used to pay for expenses (outflows), inner transactions are executed to create a balance. This is also used to decrease the exposure to one bank, and to motivate the use of less used banks and nodes (incentivizing decentralization).

### Node innovation
Different nodes can specialize for different purposes. These specializations can be based on the geographical differences, differences in the speed, number and size of transactions, and other. Our nodes could be banks, MSBs, physical persons, sole proprietors, LTDs. But also, they could be Ethereum miners.


