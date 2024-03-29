
### Transcation flow in quorum: 

![image](Images/quorum.jpeg?raw=true "Title")

   - A user or application initiates a transaction by creating and signing a transaction request.
   - The transaction request includes details such as the sender's address, recipient's address, amount, and any other relevant data.
   - The transaction request is broadcasted to a subset of nodes in the Quorum network, known as the Quorum Chain.
   - The Quorum Chain is responsible for reaching consensus on the validity of transactions.
   - If the transaction involves private data, it is sent to the Private Transaction Manager (pTM).
   - The pTM ensures that private data is only visible to authorized participants.
   - The receiving nodes in the Quorum Chain verify the validity of the transaction based on the consensus algorithm (such as Istanbul BFT) and the smart contract rules.
   - The Quorum Chain uses a consensus algorithm to agree on the order and validity of transactions.
   - Istanbul Byzantine Fault Tolerance (IBFT) is a commonly used consensus mechanism in Quorum.
   - Once a consensus is reached, the transaction is grouped with other validated transactions into a block.
   - The block is then added to the blockchain.
   - If the transaction involves private data, the Private State Manager updates the private state with the relevant information.
   - The final state of the blockchain is updated with the new block, and the transaction is considered finalized.
   - The user or client who initiated the transaction receives a confirmation once it is successfully added to the blockchain.

### how to use GETH to invoke JSON RPC API?
![image](Images/geth-attach.PNG?raw=true "Title")

we can use geth attach command to connect nodes 

### Inspecting nodes/peers information
![image](Images/node-info.PNG?raw=true "Title")

### Inspecting chain, block and transaction information
Block info:
![image](Images/blockinfo.PNG?raw=true "Title")
Transcation info:
![image](Images/txdetails.PNG?raw=true "Title")

### Creating wallets / accounts and transferring Ether between accounts 
New wallet creation:
![image](Images/account-create.PNG?raw=true "Title")

Amount transfer: 
![image](Images/amount-transfer.PNG?raw=true "Title")

