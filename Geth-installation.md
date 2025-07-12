file:
  name: geth-installation.md
  content: |
    # 🚀 Running My Own Ethereum Node Locally (Sepolia Testnet)

    As part of my Web3 studies at [Web3Bridge](https://web3bridge.com), I learned to set up a local Ethereum node using an **execution client**.

    This helped me understand what happens *under the hood* when building on Ethereum.

    ---

    ## 🧰 What I used

    - 🖥 **macOS** machine
    - ⚙ **Execution client:** Geth (Go Ethereum)
    - 🌱 **Testnet:** Sepolia

    ---

    ## ⚙️ Installation steps

    ### ✅ Install Geth using Homebrew
    ```bash
    brew install ethereum
    ```

    ### 🔍 Verify installation
    ```bash
    geth version
    ```

    ---

    ## 🌱 Connect to Sepolia testnet

    Sepolia is a developer-friendly Ethereum test network.

    To sync my local node with Sepolia:
    ```bash
    geth --sepolia
    ```

    What this command does:
    - Starts the Geth execution client
    - Connects to Sepolia peers
    - Begins syncing the Sepolia blockchain data locally
    - Exposes a **JSON-RPC API** (default: `127.0.0.1:8545`)

    ---

    ## 🧪 Why this matters

    By running my own node, I can:
    - Validate transactions and blocks locally
    - Send and test transactions through JSON-RPC
    - Deploy and interact with smart contracts
    - Avoid relying on third-party providers like Infura or Alchemy

    This makes learning Ethereum feel *real* rather than just abstract.

    ---

    ## 🛠 Next steps

    - Send test transactions to my node
    - Deploy a smart contract to Sepolia
    - Experiment with reading blockchain state
    - Explore how consensus clients & validator clients fit in

    ---

    ## 📸 Screenshot
    ![Sepolia node syncing](../images/sepolia.png)

    ---

    ## 🏷️ Tags

    `#Ethereum` `#Web3` `#Blockchain` `#Geth` `#Sepolia` `#LearningInPublic` `#Node`

    ---

    > ✍ Written as part of my learning journey.  
    > Feedback & suggestions welcome!

git:
  commands:
    - git checkout -b docs/add-geth-sepolia-node-post
    - git add docs/learned-geth-sepolia.md
    - git commit -m "docs: add post about running local Geth node on Sepolia"
    - git push origin docs/add-geth-sepolia-node-post

pr:
  title: "docs: add post about running local Geth node on Sepolia"
  description: |
    This adds a new markdown file documenting my experience setting up a local Ethereum node 
    using the Geth execution client and connecting to the Sepolia testnet.

    Includes:
    - Installation steps on macOS using Homebrew
    - Running `geth --sepolia`
    - Explanation of JSON-RPC and why running a local node matters
    - Next steps and learning goals
