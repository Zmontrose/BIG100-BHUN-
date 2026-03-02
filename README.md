🛠 Deployment Notes

When deploying, pass this as constructor argument:

1100000000000000000000000000000000000000000000000000

Example (Hardhat):

await deploy("BIG100", [
  "1100000000000000000000000000000000000000000000000000"
]);
🔒 Security Assessment

✔ No overflow risk (Solidity 0.8+)

✔ Mint restricted to owner

✔ No reentrancy vector

✔ Standard OpenZeppelin implementation

⚠ Unlimited minting (owner can inflate supply)
