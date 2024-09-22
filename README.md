# TheCyberThesis CTF - The Blockchain Breach Challenge

Welcome to the **The Blockchain Breach Challenge** created for **TheCyberThesis CTF**. This repository contains the source code for the challenge website, designed to test participants' understanding of blockchain data structures and cryptographic hash collisions.

## Challenge Overview

In this challenge, participants are tasked with analyzing a blockchain dataset consisting of 50 blocks. Each block contains:

- A **previous hash**
- **Timestamp**
- **Transactions**
- The **block's hash**
- A **salt** used to generate the block's hash

The goal is to identify and exploit **MD5 hash collisions** in the blocks with identical salts and ultimately reveal the CTF flag.

### Challenge Files

- `blockchain.json` - Contains the blockchain data with 50 blocks.
- `salts.json` - Lists the salts used to hash each block.
- `index.html` - The main interface where users upload the blockchain and salts files to analyze the data.

Participants are required to:

1. Identify blocks that share the same salt.
2. Concatenate their hashes and compute a new MD5 hash.
3. Use this new MD5 hash to unlock the flag.

## Writeup

To see how the challenge works, check out my blogsite [here](https://your-live-demo-url.com/).

---

## Installation and Setup

### Prerequisites

To run this project locally, you’ll need:

- A working web browser (Chrome, Firefox, etc.)
- Python (for script-based challenge solutions)

### Clone the Repository

```bash
git clone https://github.com/Alishba-Malik/The-Blockchain-Breach
cd The-Blockchain-Breach
npm run build 
npm run dev
```

---

## Challenge Solution Overview

Participants are provided with:

1. **`blockchain.json`** - A file with 50 blocks, each containing a hash and a salt.
2. **`salts.json`** - A list of all salts used to generate block hashes.

### Steps to Solve:

1. Identify the blocks that use the same salt.
2. Concatenate the hashes of the blocks with the same salt.
3. Generate an MD5 hash from the concatenated string.
4. Input this MD5 hash into the solution form to get the flag.

---