# NOOFT

## Directory Structure

- `js` : JavaScript binding to interact with on-chain token vesting contract
- `program` : The BPF compatible token vesting on-chain program/smart contract

## Build Program
```
anchor build
```

## Deploy Program
```
solana program deploy <project root>/program/target/deploy/token_vesting.so
```
The program address will default to this keypair (override with --program-id):
 ```
 <project root>/program/target/deploy/token_vesting-keypair.json
 ```