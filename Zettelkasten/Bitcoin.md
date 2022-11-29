202211201634

Status: #idea

Tags: [[Web3]]

# Bitcoin

## What is Bitcoin

A [[Decentralize|decentralized]] electronic cash system

## What problems bitcoin want to solved

make transactions without trusted centralized financial institution
 
## Why this problem matter

- we may not trust third party
	- third parties may not represent ours profit
- the third party may sometimes inefficient
	- e.g. international transaction
- we cant take a transaction online for now
	- take transaction though bank is an additional feature, it is not traditional cash provided 

## How is bitcoin solved

### Centralized transaction model

![[transaction-with-bank.excalidraw|700*400]]

in centralized transaction model, we need believe bank will correct update ledger, and it will save money for you. bank will update ledger in private, and we can maintain a light ledger in local, to verify the correctness immediately. the core problem is can we bring back our money in any time? In real world, it is not for sure. (p.s. save money to bank is a investigation, investigation always have risk, but bitcoins is a sort of cash, typically bitcoins is a first electronic cash, bank on blockchain as well as [[DeFi]] also has risk), if transaction happens between different banks, it may transact very slow, and it will cost many human resources.

### Design a electronic cash

- How to ensure that each user reaches a [[consensus]] on the consistency of the ledger?
	- everyone trusts the bookkeeper, if not, others can participate in the bookkeeping
	- hence we need a distributed  consensus make the hole systems consistency
	- bitcoin use [[PoW]] consensus algorithm
	- we call bookkeeper as miner, publish a valid ledger called mining
- Since bookkeeping is [[Decentralize|no central]], we have to use p2p to sync ledger, bookkeeping and make transaction
- ledger need keep consistency, but every time has a lot of transactions. So we pack a piece of ledger once in a while, and link each of them by a time order to make sure some time in the past,  the  consistency of the ledger is guaranteed.
	- we use [[blockchain]] to implement this data structure. every single packed ledger is a block
- How do we trust a new block?
	- there is two part of it:
		1. new block must be verified by previous block and the system rules, otherwise, it cause [[fork]]
		2. we assume most computation power of miner is good, than the longest verified chain is good chain. if hacker get most of computation power, he can take [[51% Attack]], but note that, this 51% is not a accuracy value, it is just under the probability meaning
- How do we make a transaction?
	- user broadcast address1 transfer some value to address2
	- miner verify:
		1. user is the owner of addr1
			- user know the private key of addr1, so we need user give a sign by addr1 private key, and others can use public key verify it, hence we need user provide signature, address of unspent transaction; and the sig need pair with pubkey in the address of unspent transaction.
		2. user has enough bitcoin to afford
			- miner verify it from UTXO
		3. user not double spent
			- miner verify it from UTXO


---
# References