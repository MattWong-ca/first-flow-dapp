# Common Problems
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

# Transactions
- [First](https://testnet.flowscan.org/transaction/1e581cdec6821e8785b0fad13ab61777c0c93624c9c9ef02fd31e6719109e43a) (Blocto)
- [Second](https://testnet.flowscan.org/transaction/ac18ded5b0a76d94111d361f19f40eefd5b8b73b4a06d8d362da5d7d7f823a38) (Lilico)
- [Third](https://testnet.flowscan.org/transaction/b4ac05671ffe30a5adf9f1e431c55c045d529bb06c489e7a2de24b14807d0403) (Lilico)