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
block stored in k-v database like [[leveldb]], witch key is hash of block, and 

---
# References