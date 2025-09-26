# DIDLab Activity 2

📄 See the full report here: [Report.md](Report.md)




---

# CampusCredit Hardhat Starter

Local-first Hardhat project for deploying an ERC-20 (CampusCredit), running transactions, and analyzing receipts & events.

## Quick Start

```bash
npm install
npx hardhat compile
# Terminal A
npx hardhat node
# Terminal B
npx hardhat run scripts/deploy.js --network localhost
npx hardhat run scripts/interact.js --network localhost
npx hardhat run scripts/analyze.js --network localhost
```

See `contracts/`, `scripts/`, and `test/` for examples.
