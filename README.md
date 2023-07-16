# 🦅 BirdBlock Flow NFTs
Live demo: https://birdblock-nft.vercel.app/

My first dapp built on Flow - a NFT minting site that lets you easily mint bird NFTs. Log in with just an email through Blocto or sign up for a Lilico wallet to begin minting. Once your wallet is connected, mint an NFT and view your collection at the bottom of the screen!

I used Cadence (resource-oriented programming) for the Flow contracts/scripts/transactions, and React for the frontend. The GIFs are stored on IPFS through NFT.Storage and the site is deployed on Vercel.

# 📷 Screenshots
### Landing page
<img width="1440" alt="Screenshot 2023-07-16 at 8 56 46 AM" src="https://github.com/MattWong-ca/first-flow-dapp/assets/66754344/82c4630b-a9ff-452d-b582-977deb8d2914">

### Mint screen
<img width="1440" alt="Screenshot 2023-07-16 at 8 56 20 AM" src="https://github.com/MattWong-ca/first-flow-dapp/assets/66754344/00a1e32e-9773-47e8-acfb-14141039be6f">

### Console when minting
<img width="440" alt="console-log-birdblock" src="https://github.com/MattWong-ca/first-flow-dapp/assets/66754344/65913f74-5096-4114-a381-97982b582bf7">

# 🔗 Links
- [Deployed contracts](https://flow-view-source.com/testnet/account/0x990bf8fe740942e2)
- [First txn](https://testnet.flowscan.org/transaction/1e581cdec6821e8785b0fad13ab61777c0c93624c9c9ef02fd31e6719109e43a) (Blocto)
- [Second txn](https://testnet.flowscan.org/transaction/ac18ded5b0a76d94111d361f19f40eefd5b8b73b4a06d8d362da5d7d7f823a38) (Lilico)
- [Third txn](https://testnet.flowscan.org/transaction/b4ac05671ffe30a5adf9f1e431c55c045d529bb06c489e7a2de24b14807d0403) (Lilico)

# 🚧 Friction Log
- Location of `flow.json` file. Not sure if it should be in root (first-flow-dapp) or FlowNFTs, but placing it in root seems to be working
- When running `flow emulator`, it would default connect to `Alice` account, needed to switch it manually to `Emulator-account`
- Got many errors when opening the repo up for first time. Needed to go to NonFungibleToken.cdc and deploy there first, then BottomShot.cdc, and finally mintNFT.cdc (since they're dependent on each other)
- Common fix for errors is to restart VS Code and flow emulator
- Lilico was originally giving `invalid for chain flow-testnet` --> wallet was on mainnet, needed to go to developer mode and switch to testnet
- Sometimes got `transaction execute failed: [Error Code: 1101] cadence runtime error: Execution failed:
error: panic: Could not get receiver reference to the NFT Collection` but retried couple of minutes later and it worked. Not sure why.
- NFTs aren't showing in wallet or in Flowscan under transfers, not sure why
- First successful attempt was actually with Blocto, but it stopped working, rest of successful attempts were with Lilico
- With Blocto: `DEPRECATION NOTICE Received FCL::CHALLENGE::RESPONSE, please use FCL:VIEW:RESPONSE for this and future versions of FCL`. When I try to log in and click confirm, nothing happens afterwards.
- Not Flow related: I kept getting "The git repository has too many active changes, only a subset of Git features will be enabled", turns out forgot to add a .gitignore
- Need to create a destory button to delete NFTs
- It keeps printing out only the fourth NFT, not incrementing correctly
- Vercel wasn't working because I needed to switch framework from Other --> React, and add `frontend` as root directory

### Note
- Everyone has the ability to mint and we're passing in the NFT metadata from the frontend
- Better way: use [NFTMinter resource](https://github.com/onflow/flow-nft/blob/master/contracts/ExampleNFT.cdc) and store IPFS hash on contract + increment file number using Cadence so people can't mint all sorts of NFTs
