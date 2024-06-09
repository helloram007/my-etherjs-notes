What is a Node: Single instance in the blockchain network.
Consensu: mechanism used to agree on the state on blockchain

1) ChainSelection (Nakamoto Consensus) EIP 1559 Miners Gas paid by whoever initiates the transactions
2) Sybil resistence
	a) PoW ( Miners )
	b) PoS ( Validators )
	
	Sybil attack: 
	51% attack longest chain rule
	
	PoS : nodes put up collateral as a sybil resistance mechanism, if they misbehave, then they will removed or loose all the collateral.
		miners are called validators.
		
Layer 1: base layer blockchain solution.
Layer 2: any application on Layer1
Rollups derive their security from Base Layer
Side Chains derive their security from their own protocols.

L2 Types:
 Optimistic and Zero Knowledge Chains.
 
 Hybrid Decentralised : Oracles connecting Blockchains connecting with data from external sources.
 
 Web 1 : The Permisionless open sourced web with static content.
 Web 2 : The Permissioned Web with Dynamic content where companies run your agreements on their servers
 Web 3 : The Permissioned Web with Dynamic content. Where decentralized censorship resistant networks run your
       agreement and code. it generally is accompanied by the idea of user owned ecosystems, where the protocols
       you interact with you also own a portion of , instead of solely being the product.
       
       Smart Contract = "Unbreakable promises by agreement"
       Smart Contract = "Trust Minimized Verifiable agreements"
 
 What is the value of Smart Contracts?
 
 What is a Smart Contract: an Agreement, contract or set of instructions that is deployed on a decentralized blockchain.
 	1) Cannot be altered(Immutable)
 	2) Automatically executes
 	3) Everyone sees the terms of the agreement
 
 Transaction Fee = Gas Price * Usage of Gas for txn.
 
 What is a Hash: A unique fixed length string, meant to identify a piece of data.
                 They are created by placing said data into a "hash function". 

private key: Only known to the key holder, it's used to "sign" transactions.
Publilc Key: is derived from your private key.Anyone can "see" it, and use it to verify that a 
             transaction came from you.
Signing a Transaction:
A"one way" process. Someone with a private key signs a transaction by their private key being hashed with their transaction data.
Anyone can then verify this new transaction hash with your public key.

Secret Key >>> Private Key <<creates>> Public Key <<Creates>> Address


