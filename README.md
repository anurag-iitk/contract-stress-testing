

# Smart Contract Stress Testing

## Overview

This project demonstrates stress testing of a blockchain network using [Pandora's Box](https://github.com/blockchain-etl/pandoras-box), an Ethereum stress-testing tool. The testing is integrated with a Hardhat environment, ensuring the blockchain's performance and stability under heavy load.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/anurag-iitk/contract-stress-testing.git
   cd contract-stress-testing
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Install Pandora's Box globally:

   ```bash
   npm install -g pandoras-box
   ```

## Running the Project

Start the Hardhat network:

```bash
npx hardhat node
```

## Stress Testing with Pandora's Box

Once your Hardhat network is running, you can perform stress testing using the following command:

```bash
pandoras-box -url http://127.0.0.1:8545 -m "powder major vast spare apart convince daring lunar mountain expose tennis oil" -s 100 -t 500 -b 100 -o ./myOutput.json
```

### Command Explanation:
- `-url`: Specifies the URL of the Ethereum network (in this case, the local Hardhat node).
- `-m`: The mnemonic seed phrase for generating test accounts.
- `-s`: Number of test accounts.
- `-t`: Number of transactions to be sent.
- `-b`: Number of blocks to be mined during the test.
- `-o`: Output file to store the results.

## Output

The stress test results will be saved in a JSON file (e.g., `myOutput.json`). You can analyze the output to assess network performance, transaction throughput, and overall stability under stress.
