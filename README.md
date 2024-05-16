Data Encryption Standard (DES) Implementation in Python

Overview
This repository contains a Python implementation of the Data Encryption Standard (DES) algorithm. DES is a symmetric-key block cipher used for encrypting and decrypting data. This implementation includes the essential components of DES, such as initial and final permutations, key schedule generation, Feistel function, and S-Box substitution.

Features
Permutation tables and S-Boxes as per DES specification
Key schedule generation
Feistel function implementation
Support for encrypting plaintext messages of arbitrary length
Encryption of messages using 64-bit blocks
Files
des.py: Contains the implementation of the DES algorithm
Functions
Permutation Tables and S-Boxes
IP, FP, E, PC1, PC2, P: Permutation tables used in DES
S_BOX: S-Boxes used in the Feistel function
Utility Functions
permute(block, table): Permutes bits of the block according to the given table
xor(bits1, bits2): Performs XOR operation on two bit lists
s_box_substitution(bits): Applies S-Box substitution on the given bits
int_to_bits(value, length): Converts an integer to a list of bits of given length
bits_to_int(bits): Converts a list of bits to an integer
Feistel Function
feistel_function(right, subkey): Implements the DES Feistel function using expansion, XOR with the subkey, S-Box substitution, and permutation
Key Schedule
generate_subkeys(key): Generates 16 subkeys from the original key using permutation choices and left rotations
DES Encryption Block
des_encrypt_block(block, subkeys): Encrypts a single 64-bit block using the 16 subkeys
DES Encryption
des_encrypt(message, key): Splits the message into 64-bit blocks, encrypts each block, and concatenates the encrypted blocks
Notes
This implementation is a straightforward version of DES and does not include padding or block chaining modes. For practical use, consider implementing these features.
Ensure that the key and message lengths are handled appropriately in a real-world application.
Contributing
Feel free to open issues or submit pull requests if you have suggestions for improvements or find any bugs.

License
This project is licensed under the MIT License - see the LICENSE file for details.
