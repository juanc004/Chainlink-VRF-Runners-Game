# Chainlink Bootcamp: Gaming with Chainlink VRF on Avalanche Fuji

Learn how to create fair and transparent blockchain-based games using Chainlink's Verifiable Random Function (VRF). This guide will walk you through deploying a dynamic NFT smart contract on the Avalanche Fuji testnet, utilizing Chainlink VRF to introduce randomness into game outcomes.

## Setup

Before you begin, ensure you have the following:

- **Wallet**: Install and configure [MetaMask](https://metamask.io/) for the Avalanche Fuji network.
- **IDE**: Access [Remix IDE](https://remix.ethereum.org/) online.
- **Network**: Connect MetaMask to the Custom (43113) network, which corresponds to Fuji.

## Deployment Steps

### Step 1: Smart Contract Preparation

1. **Access Remix IDE**: Navigate to [Remix](https://remix.ethereum.org/) and ensure you're logged in.
2. **Create `Runners.sol`**: In the "FILE EXPLORER" panel of Remix, click the "Create New File" icon and name your file `Runners.sol`.

> **Important**: Before deploying your contract, ensure you have established a VRF Subscription. You will receive a 4-digit subscription ID, which is required to be entered into your contract's constructor upon deployment.

### Step 2: VRF Subscription

- **Create a Chainlink VRF Subscription**:
  - Visit the [Chainlink VRF page](https://vrf.chain.link/) and connect your MetaMask wallet.
  - Choose the Fuji network and create a new subscription.
  - **Fund your subscription** with 3 LINK tokens and record your subscription ID for later use.

### Step 3: Contract Deployment

- **Deploy `Runners.sol`**:
  - Back in Remix, compile `Runners.sol` and prepare for deployment.
  - Ensure MetaMask is connected and set to the Fuji network.
  - Deploy your contract by entering your VRF subscription ID as a parameter.
- **Verify Deployment**:
  - After deployment, use the `tokenIdCounter` function to confirm the creation of your first NFT, which should return `1`.

### Step 4: OpenSea Collection

- **Check Your NFT on OpenSea**:
  - Copy your deployed contract's address from Remix.
  - Visit [OpenSea's testnet environment](https://testnets.opensea.io/) and paste your contract address to view your newly minted NFT collection.

### Step 5: Add VRF Consumer

- **Link Your Contract to VRF**:
  - Return to your Chainlink VRF subscription dashboard.
  - Add your `Runners.sol` contract address as a new consumer. This allows your contract to request randomness from Chainlink VRF.

### Step 6: Execute "run" Function

- **Interact with Your NFT**:
  - In Remix, interact with your deployed `Runners.sol` contract.
  - Call the `run` function with `0` as the token ID to simulate randomness in your game.

### Step 7: OpenSea Metadata Refresh

- **Update Your NFT Metadata**:
  - After executing the `run` function, refresh your NFT's metadata on OpenSea to see the updated attributes resulting from the Chainlink VRF call.

### Step 8: Mint New Players

- **Expand Your Collection**:
  - Use the `safeMint` function in your contract to mint new NFTs, selecting a character by its index (0 to 3).
  - View your new NFTs on OpenSea and refresh their metadata as needed.

### Step 9: Continuing Rounds

- **Keep the Game Going**:
  - Continue to call the `run` function for each NFT player, observing how Chainlink VRF influences your game's outcomes.
  - Compare the progress of each NFT player on OpenSea by refreshing their metadata.

## References & Resources

For comprehensive documentation, community support, and additional resources, explore the following:

- [Chainlink VRF Documentation](https://docs.chain.link/docs/vrf/v2/)
- [Avalanche Fuji Testnet Information](https://docs.chain.link/vrf/v2/subscription/supported-networks#avalanche-fuji-testnet)
- [Security Considerations for Chainlink VRF](https://docs.chain.link/vrf/v2/security)
- [Best Practices when using Chainlink VRF](https://docs.chain.link/vrf/v2/best-practices)
- [Chainlink Case Studies](https://chain.link/case-studies/nba)

### Support & Community

- **Discord**: Join [Chainlink's Discord](https://chain.link/discord) for bootcamp support and community interaction.
- **Hackathon**: Get involved in "Block Magic", our next hackathon. [Sign up here](https://chn.lk/3xjhPDy).
- **Learning Resources**: Access all session recordings on [Luma](https://lu.ma/ChainlinkBootcamp2024) and download the slides [here](https://docs.google.com/presentation/d/e/2PACX-1vSnf4bZHTmpZW8s_PKwkS2wT0ZbHmMygg1JKGlvElaS9G0v9wA5kUr_8sJbkGEJZ5cM6y6a3U0a_5t1/pub?start=false&loop=false&delayms=3000).
- **LINK Faucets**: For LINK tokens and additional support, visit [Chainlink Faucets](https://faucets.chain.link).
