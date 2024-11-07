# Merkle Tree Program

## Overview
This C++ program reads student data from a text file, generates SHA-256 hashes for each student, and constructs a Merkle tree from the hashed data. It then outputs the Merkle root hash and displays the entire tree in a visually structured format.

## Features
- Reads student data (ID, name, GPA) from a text file.
- Generates SHA-256 hashes for each student entry.
- Constructs a Merkle tree from the hashes.
- Displays the Merkle root hash.
- Prints the entire Merkle tree structure in a readable format.

## Prerequisites
To compile and run this program, you will need:
- **C++ Compiler** (e.g., g++, clang++, Visual Studio)
- **OpenSSL Library** for SHA-256 hashing

## Installation
1. Install the OpenSSL library on your system.
2. Clone or download the program source code.
3. Ensure your C++ development environment is set up to link against the OpenSSL library.

## Compilation Instructions
Use the following command to compile the program (adjust paths to your environment):
```bash
g++ -o merkle_tree_program merkle_tree_program.cpp -lssl -lcrypto
```
For Visual Studio users:
- Add OpenSSL headers and libraries to your project.
- Link against `libssl.lib` and `libcrypto.lib`.

## Usage
1. Create a text file named `students.txt` with the following format:
   ```
   1 John, 3.8
   2 Alice, 3.6
   3 Bob, 3.9
   4 Charlie, 4.0
   ```
   Each line should represent a student with their ID, name, and GPA separated by a space and a comma.

2. Run the compiled program:
   ```bash
   ./merkle_tree_program
   ```

## Sample Output
![image](https://github.com/user-attachments/assets/ed2149b6-8104-4f4b-90b6-5c9028c7b393)

## Code Structure
- **`Student` struct**: Represents a student with ID, name, and GPA.
- **`NodeMerkel` struct**: Represents a node in the Merkle tree, with pointers to left and right child nodes and a hash value.
- **`sha256` function**: Computes the SHA-256 hash of a given string.
- **`readStudentsFromFile` function**: Reads student data from a text file and returns a vector of `Student` objects.
- **`leafNode` and `parentNode` functions**: Create leaf and parent nodes for the Merkle tree.
- **`insertNode` function**: Constructs the Merkle tree from a vector of leaf nodes.
- **`printTree` function**: Displays the Merkle tree in a readable format.

## Dependencies
- OpenSSL Library
- C++ Standard Library

## License
This program is open-source and free to use. Please credit the original author if modifying or redistributing.

## Troubleshooting
- **Linking Errors**: Ensure your compiler is linking against the OpenSSL library (`-lssl -lcrypto` for g++ or `libssl.lib` and `libcrypto.lib` for Visual Studio).
- **File Reading Issues**: Ensure `students.txt` is in the correct format and located in the same directory as the executable or adjust the file path accordingly.

## Contact
For any questions or support, please contact me at chitoiu.andrei2@yahoo.com.

