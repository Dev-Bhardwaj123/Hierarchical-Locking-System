# Hierarchical-Locking-System
Hierarchical Locking System 🚀

🔹 Problem Statement
In many real-world applications, data is organized in a hierarchical structure (e.g., file systems, databases, organizational trees). To ensure concurrent access control, we need a locking mechanism that enforces exclusive access while maintaining hierarchy constraints.

This project implements an optimized Hierarchical Locking System using an m-ary tree, supporting the following operations:

1️⃣ lock(node, userId) → Grants exclusive access to a node if:

The node is not already locked.
No ancestor or descendant of the node is locked.
2️⃣ unlock(node, userId) → Unlocks a node if:

The same user previously locked it.
3️⃣ upgradeLock(node, userId) → Upgrades a user’s lock to an ancestor node if:

The ancestor has at least one locked descendant.
All locked descendants are locked by the same user.
🔹 Input Format
1️⃣ N → Number of nodes in the tree (1 < N < 500,000)
2️⃣ M → Maximum children per node (1 < M < 30)
3️⃣ Q → Number of queries (1 < Q < 500,000)
4️⃣ Tree Nodes: Unique node names representing the hierarchy.
5️⃣ Queries:

1 nodeName userId → Lock
2 nodeName userId → Unlock
3 nodeName userId → UpgradeLock

🔹 Example Input & Output
Input:
7  
2  
5  
Root  
A  
B  
C  
D  
E  
F  
1 C 9  
1 D 9  
3 A 9  
2 D 9  
2 A 9  

Output:
true  
true  
true  
false  
true  

