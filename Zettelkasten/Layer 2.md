202212042212

Status: #idea

Tags: [[blockchain]]

# Layer 2

Layer 2 is a solution to speed up L1, or called L1 scaling. We pertain not go down safety of blockchain or as L1.

## Rollup

Pack transactions and Merkel tree root update to block, usually update in contract content tree, not execute transactions on chain. And rollup contract will update [[blockchain]] state. Although transactions store on chain, but light node no need download it, unless need verify the transaction.

### Optimism

optimistic rollup, there is a sequencer pack transactions and update chain state, assume most sequencers is trusted. Any sequencer need validate some coins when it upload transactions and state, and there are some challengers verify the packed transactions, if they find any transaction is invalid, the challenger can dispute the transaction and get reward from sequencer validated. Of course, challenger also need validate some coins to avoid chain ddos, and it will burn some coins from validated to avoid the one published the invalid transaction to bring back the coins. We need a dispute period duration let challengers have enough time check transactions, usually need 1 or 2 week.

pros:
- simple to implement

cons:
- dispute period duration is too long.
- safety depend on enough challengers.
- because we may need verify packed transactions on chain, the size of pack limited by max gas fee

### Arbitrum

different with optimism: multi turn ask cha 

### zkRollup

### Polygon

---
# References

https://research.paradigm.xyz/rollups

https://www.bilibili.com/video/BV1kP4y197vL/?share_source=copy_web&vd_source=69807ae335823f65b2ae2d890a863b2a