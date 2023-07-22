# BTree-Index   #Academic Project


In this project milestone, we are tasked with implementing a B+ Tree Index for insertion and lookup operations. We will follow the C++ implementation and utilize the BTreeNode classes for automatic splitting when necessary during insertion. By utilizing the classes and methods provided by the professor in helper code, I added logic for the B-tree Index in Btree.cpp


This code implements a B+ Tree Index data structure and provides functionalities for creating, opening, closing, and dropping the index, as well as inserting and looking up rows based on specified key values. The B+ Tree Index is implemented using BTreeIndex, BTreeNode (BTreeLeaf and BTreeInterior), and BTreeStat classes.

## Key points in the implementation:

- BTreeIndex constructor: It creates a B+ Tree index with the specified parameters (relation, index name, key columns, and uniqueness). It also builds the key profile to determine the data types of each key component.

- create(): This method creates the B+ Tree index file and initializes the root node. It populates the index with existing data from the table by performing insertions.

- open(): This method opens an existing B+ Tree index file and initializes the root node for lookup, insert, delete, and update operations.

- lookup(): It finds all the rows in the index whose columns match the given key_dict.

- insert(): It inserts a row with the specified handle into the index.

- del(): This method is not fully implemented yet, and it throws an exception for now.

- tkey(): This function encodes the key values from a ValueDict into a KeyValue format based on the key profile.

- build_key_profile(): It determines the data types of each key component and constructs the key profile.

- test_btree(): A test function that creates a B+ Tree index, inserts rows into the table, performs lookups based on the index, and tests certain functionalities. However, it is partially commented out in the code, and the delete and range functions are not yet fully implemented.

- The code is designed to handle indexing efficiently, ensuring fast lookups and insertions in a sorted manner using the B+ Tree data structure.
