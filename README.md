# Local Avalanche Subnet and Smart Contract Deployment

This guide walks you through the process of establishing a local Avalanche Subnet using `avalanche-cli` and deploying two smart contracts, namely `token.sol` and `vault.sol`, through Remix and MetaMask.

## Prerequisites
- **Golang Installation:** Ensure Golang is installed to build `avalanche-cli`.
- **Node.js Installation:** Install Node.js to facilitate running the local Avalanche node.
- **Avalanche CLI Setup:** Follow the instructions in the [Avalanche CLI Installation Guide](https://docs.avax.network/tooling/cli-guides/install-avalanche-cli) for `avalanche-cli` installation.
- **MetaMask Configuration:** Install and configure MetaMask to connect to the local Avalanche node.
- **Remix Workspace:** Open Remix and create a new workspace.

## Setting up the Local Subnet

### Configuring the Subnet:

1. Execute the `avalanche subnet create` command and follow the prompts to create a Subnet configuration.
2. Choose a name for your Subnet (e.g., mySubnet).
3. Select `SubnetEVM` as the VM.
4. Assign a positive integer for the ChainID (e.g., 151511).
5. Define any additional Subnet options as necessary.

### Deploying the Subnet:

1. Use the `avalanche subnet export` command to export the Subnet configuration file.
2. Deploy the Subnet locally with the `avalanche subnet deploy --local` command.

## Deploying Smart Contracts

### Compiling Contracts:

1. Import the `token.sol` and `vault.sol` files into Remix.
2. Compile both contracts.

### Connecting to the Local Node:

1. In Remix, access the "ENVIRONMENT" dropdown within the "Deploy" tab.
2. Select "Injected Web3" and ensure MetaMask is connected to the local Avalanche node.

### Deploying Contracts:

For each contract:
1. Choose the contract in the "Deployer" section.
2. Enter the constructor arguments (if any).
3. Click "Deploy."
4. Confirm the transaction in MetaMask.

### Interacting with Contracts:

Utilize the Remix interface to interact with the deployed contracts, enabling you to call functions, read contract data, and monitor events.
