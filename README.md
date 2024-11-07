Merkle Tree Program

Overview

This C++ program reads student data from a text file, generates SHA-256 hashes for each student, and constructs a Merkle tree from the hashed data. It then outputs the Merkle root hash and displays the entire tree in a visually structured format.

Features

Reads student data (ID, name, GPA) from a text file.

Generates SHA-256 hashes for each student entry.

Constructs a Merkle tree from the hashes.

Displays the Merkle root hash.

Prints the entire Merkle tree structure in a readable format.

Prerequisites

To compile and run this program, you will need:

C++ Compiler (e.g., g++, clang++, Visual Studio)

OpenSSL Library for SHA-256 hashing

Installation

Install the OpenSSL library on your system.

Clone or download the program source code.

Ensure your C++ development environment is set up to link against the OpenSSL library.

Sample output
![image](https://github.com/user-attachments/assets/5dcec363-0918-4527-8f93-1b966ef461d4)

Code Structure

Student struct: Represents a student with ID, name, and GPA.

NodeMerkel struct: Represents a node in the Merkle tree, with pointers to left and right child nodes and a hash value.

sha256 function: Computes the SHA-256 hash of a given string.

readStudentsFromFile function: Reads student data from a text file and returns a vector of Student objects.

leafNode and parentNode functions: Create leaf and parent nodes for the Merkle tree.

insertNode function: Constructs the Merkle tree from a vector of leaf nodes.

printTree function: Displays the Merkle tree in a readable format.

Dependencies

OpenSSL Library

C++ Standard Library
