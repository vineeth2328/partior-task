
Feature	Hyperledger Fabric	Hyperledger Indy					
Purpose	General-purpose blockchain platform	Decentralized Identity (DID) Management					
Throughput	- Moderate (1,000 - 3,000 TPS with optimizations)	- Lower (designed for identity management, not high-volume transactions)					
Scalability	- Higher scalability potential through sharding and channel architecture	- Lower scalability potential due to focus on DID interaction security					
Complexity	- More complex due to modular architecture, permissioned network setup, and pluggable consensus mechanisms	- Less complex, with a focused purpose and built-in DID management features					
Maintainability	- Requires more expertise due to broader feature set, potential for customization, and diverse deployment options	- Generally easier to maintain due to narrower scope and focused functionality					
Performance	- Suitable for a wider range of applications with varying performance requirements	- Not suitable for high-performance transactional applications requiring high throughput					
Security	- Supports confidential transactions and private channels for secure data sharing	- Focuses on secure DID issuance, revocation, and verifiable credentials					
Privacy	- Supports private and consortium networks for permissioned access	- Can be used for anonymous interactions within specific use cases					
Regulation	- Can be compliant with various regulations through permissioned networks and access control	- Designed for privacy-preserving identity management which can align with specific regulatory requirements					
Maturity	- More mature and established platform with a larger ecosystem and extensive documentation	- Less mature platform with a smaller community and evolving feature set					
Interoperability	- Can integrate with other Hyperledger projects and external systems	- Supports interoperable DIDs for identity exchange across different platforms					
Cost	- Open-source platform with no licensing fees, but deployment and ongoing maintenance costs can vary	- Open-source platform with no licensing fees, but integration with existing infrastructure can impact cost					
Learning Curve	- Steeper learning curve due to the complexity and diverse features	- Lower learning curve due to focused functionality and clear documentation on DIDs					
Use Cases	- Supply chain management, trade finance, asset tracking, voting systems, healthcare data management	- Decentralized identity management, self-sovereign identity, verifiable credentials, access control, data privacy					
Community & Support	- Larger community with more active forums, tutorials, and contributions	- Smaller community but growing rapidly with dedicated support resources					
Deployment Options	- Supports various deployment options (on-premises, cloud, hybrid)	- Primarily cloud-based deployments, but on-premises options are emerging					
Customization	- Highly customizable through pluggable modules and chaincode development	- Limited customization options due to focused purpose on DIDs					
Permissioning	- Permissioned networks with flexible access control mechanisms	- Can be used in permissioned or permissionless environments for DID interaction					
Consensus Mechanisms	- Supports various consensus mechanisms for different network requirements (e.g., PBFT, Kafka)	- Primarily leverages Indy's built-in Plenum consensus for DID operations					
Data Storage	- Supports different state database options (e.g., LevelDB, CouchDB)	- Leverages Indy's distributed ledger for storing DID data and credentials					


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

