# Gift List Merkle Tree Project

This project demonstrates the use of a Merkle tree to verify if a data item is part of a set without storing the entire set. It is a practical exercise in understanding Merkle trees and their application in data verification.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) installed on your machine
- [npm](https://www.npmjs.com/) (Node Package Manager)

### Installation

1. Clone the repository:
    ```bash
   git clone <repository-url>
    ```

2. Naviage to project repository
    ```bash
    cd MarkleTree-GiftList
    ```

3. Install the dependencies
    ```bash
    npm install
    ```

### Project Structure
The repository is organized into three main directories:

#### Client
- Description: Acts as the prover in the Merkle tree verification process.
- Usage: Run the client script to send an HTTP request to the server.
- Command:
    ```bash
    node client/index
    ```

#### Server
- Description: Functions as the verifier to check if a name is in the MERKLE_ROOT.
- Usage: Start the server to listen for client requests.
- Command: 
    ```bash
    node server/index
    ``` 
- Port: The server listens on port 1225.

### Utils
- niceList.json: Contains names of individuals eligible for a gift.
- example.js: Demonstrates generating a Merkle root, creating a proof, and verifying a name against the root.
- MerkleTree.js: A modified version of the Merkle Tree module for easier integration.
- verifyProof.js: Used to verify if a name is part of the Merkle root.

### How It Works
- Merkle Tree Creation: The MerkleTree class is used to create a tree from the niceList.json.
- Proof Generation: A proof is generated for a specific name to verify its presence in the tree.
- Verification: The server verifies the proof against the MERKLE_ROOT.

### License
- This project is licensed under the MIT License.