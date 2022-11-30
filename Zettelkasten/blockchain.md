202211302346

Status: #idea

Tags:

# blockchain

Blockchain is a link-table replace pointer to hash pointer.
```cpp
// link table
<typename T>
struct node {
	T data;
	node *pre;
};

//block
<typename T>
struct block {
	T data;
	std::string hash_of_pre_node;
}
```
block stored in k-v database like [[leveldb]], witch key is hash of block.

Since there is hash pointer, we can't break the order of blocks or change block raw data, like we can't break the time, indeed we can use this feature to record unchangeable history. If we do need change the past, we would make a fork, like a forked timeline.

Because linked table search is $O(n)$ complexly, we could make a tree use hash pointer to speed up search and also made data unchangeable, this is merkle tree
![[Pasted image 20221201011338.png|merkle tree]]

---
# References