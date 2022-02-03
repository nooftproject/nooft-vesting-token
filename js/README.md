# Simple JS binding

## Quickstart

Run `yarn` in the `js` directory to install the node modules.

## Prerequisite
1. Place wallet keypair to `js` folder
2. Define variables in `js/variables.json` file
```
"rpc": "https://api.devnet.solana.com", # replace it with `https://api.mainnet-beta.solana.com` on mainnet
"wallet_path": "../keypair.json",
"wallet_address": "",                   # owner's wallet address
"token_address": "",                    # token mint address
"token_account": "",                    # token account address  
"decimals": 9,
"token_vesting_program_id": "",         # token vesting program id 
"distination_owner": "",                # receiver's wallet address for vesting
"distination_token_account": "",        # receiver;s token account address for vesting
"associated_wallet_address": "",        # receiver's wallet address
"locked_seed": ""                       # locked contract's seed. it will be needed to unlock 
```

3. Define unlocking schedule in `js/src/lock.ts`
```
const DATES = [
  new Date(2022, 2),
  new Date(2022, 3),
  new Date(2022, 4),
];
const AMOUNT_PER_SCHEDULE = [
  100,
  200,
  500
];
```

## Build
```
yarn build
```

## Locking
```
yarn lock
```
## Unlocking
```
yarn unlock
```