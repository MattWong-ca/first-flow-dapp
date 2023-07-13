# Common Problems
- Location of `flow.json` file. Not sure if it should be in root (first-flow-dapp) or FlowNFTs, but placing it in root seems to be working
- When running `flow emulator`, it would default connect to `Alice` account, needed to switch it manually to `Emulator-account`
- Got many errors when opening the repo up for first time. Needed to go to NonFungibleToken.cdc and deploy there first, then BottomShot.cdc, and finally mintNFT.cdc (since they're dependent on each other)
- Common fix for errors is to restart VS Code and flow emulator
- Not Flow related: I kept getting "The git repository has too many active changes, only a subset of Git features will be enabled", turns out forgot to add a .gitignore