# Shavowcrack_v1: Caesar Cipher Decryption Tool

Shavowcrack_v1 is a brute-force Caesar Cipher decryption tool. It attempts to decode a given ciphertext by shifting each character in the message through every possible key value until it finds a readable plaintext. This tool works with a predefined set of symbols, including uppercase and lowercase letters, numbers, spaces, and some punctuation marks.

## Table of Contents
1. [How It Works](#how-it-works)
2. [How to Use](#how-to-use)
3. [Explanation of Key Values](#explanation-of-key-values)

## How It Works

The Caesar Cipher is a type of substitution cipher where each character in the text is shifted a certain number of positions in the alphabet. Shavowcrack_v1 brute-forces the decryption by iterating through all possible shifts (or "key" values) from 0 to the total number of symbols in `SYMBOLS`. The program creates a new message with each possible key value and displays it so that the user can identify the correct decrypted message.

- **SYMBOLS**: A string containing all possible characters in the encrypted message, including uppercase and lowercase letters, numbers, and a few special symbols.
- **Key**: The number of positions each symbol in the encrypted message is shifted to reveal the original text.

## How to Use

1. **Run the Script**:
   - You need a Python environment to run this script. Use Python 3.x to avoid compatibility issues.
   
2. **Input the Ciphertext**:
   - When prompted, enter the ciphertext (encrypted message) you want to decrypt.

3. **View Possible Decryptions**:
   - The program will display possible decrypted messages for each key value, labeled as `Key #<key>: <decrypted_text>`. Look through the output to find the correct, readable message.

   Example usage:
$ python decrypt.py
What is your ciphertext? wklv lv d vhfuhw phvvdjh!
Key #0: wklv lv d vhfuhw phvvdjh!
Key #1: vjku ku c ugdtgv oguucig.
Key #2: uijt jt b tfdsft nfttbif
...
Key #10: this is a secret message!


In this example, the decrypted message with `Key #10` reads as "this is a secret message!"

## Explanation of Key Values

The Caesar Cipher shifts each character by a "key" number of positions. The key values in this program range from 0 to the length of `SYMBOLS`, attempting each possible shift. Each possible decryption corresponds to shifting the encrypted characters back by the key number of positions.

The correct key will reveal the original message in readable form. Since this is a brute-force approach, it works best for shorter messages where a readable outcome can be identified quickly.
