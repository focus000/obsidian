202211222232

Status: #idea

Tags: [[blockchain]]

# Blockchain Full Node Size Too Big

## Conclusion

No need worry about the size growth

## Explain

- the growth of full node size is $O(n)$ 
	- bitcoin size after a century:
		- block-avg-size \* blocks-per-hour \* a-century = 4Mib \* 6blocks/hr \* 1Century = 20TB
	- Ethereum size after a century:
		- 10Mb \* 300blocks/hr \* 1Century = 25TB
- there is enough time to replace blockchain before the size growth unacceptable
- technology is developing, we don't no how cheap of the ssd after 100 years 

---
# References

[100TB SSD](https://www.techradar.com/news/at-100tb-the-worlds-biggest-ssd-gets-an-eye-watering-price-tag)
[ETH full node size 650GB](https://geth.ethereum.org/docs/interface/hardware)
[ETH size graph](https://ycharts.com/indicators/ethereum_chain_full_sync_data_size) note that eth client has bug, need prune nodes, so the size may not accuracy
[BTC full node size 439GB](https://ycharts.com/indicators/bitcoin_blockchain_size)

