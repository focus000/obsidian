202212020025

Status: #idea

Tags: [[blockchain]]

# consensus

For [[Decentralize|decentralized]], we need multiple client run [[blockchain]], there is a problem to make all clients get the same status. consensus is a way to solve this problem. 

## PoW

device change nonce in block header to calculate hash, if the hash in target set, we accept this block, and notice other miner. we need  block generation rate is stable, too fast will let blockchain has many temporary fork, and make blockchain unstable ( why? ),
while too long will reduce transparent speed. Hence the algorithm will adjust the difficulty depend on the last block genesis time.

pros:
- let idle power transfer to profit

cons:
- waste power

## PoS

Since PoW calculate hash is nonsense, we proposed to avoid waste power. PoW is make profit transfer to crypto currency by calculate hash, while PoS is staking coins. If staker or miner be evil, coins will go down

---
# References