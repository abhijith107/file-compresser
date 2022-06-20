# file-compresser
CPP program for file compression using Huffman Coding Algorithm

# Discription

Huffman Coding is a technique of compressing data to reduce its size without losing any of the details. It was first developed by David Huffman.

Huffman Coding is generally useful to compress the data in which there are frequently occurring characters.
Each character occupies 8 bits. There are a total of 15 characters in the above string. Thus, a total of 8 * 15 = 120 bits are required to send this string.

Using the Huffman Coding technique, we can compress the string to a smaller size.

Huffman coding first creates a tree using the frequencies of the character and then generates code for each character.

Once the data is encoded, it has to be decoded. Decoding is done using the same tree.

Huffman Coding prevents any ambiguity in the decoding process using the concept of prefix code ie. a code associated with a character should not be present in the prefix of any other code. The tree created above helps in maintaining the property.

# Algorithm
-> Calculate the frequency of each character in the string.
-> Sort the characters in increasing order of the frequency. These are stored in a priority queue.
-> Make each unique character as a leaf node.
-> Create an empty node z. Assign the minimum frequency to the left child of z and assign the second minimum frequency to the right child of z. Set the value of the z as the sum of the above two minimum frequencies.
-> Remove these two minimum frequencies from Q and add the sum into the list of frequencies 
-> Insert node z into the tree.
-> Repeat steps 3 to 5 for all the characters.
-> For each non-leaf node, assign 0 to the left edge and 1 to the right edge.

