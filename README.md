# Minimal DAO Governance

A professional-grade, standard-compliant Governance system for decentralized organizations. This repository implements the core "Governor" logic used by major protocols like Uniswap and Compound, optimized into a single-directory flat structure.

## Core Components
* **Governance Token:** An ERC20 token with snapshots and delegation capabilities.
* **Governor Contract:** Handles proposal submission, voting, and counting logic.
* **Timelock Controller:** Acts as the DAO treasury and executor, adding a mandatory delay between vote success and execution for security.

## Governance Lifecycle
1. **Propose:** A token holder submits a proposal.
2. **Vote:** Holders cast votes (For, Against, or Abstain) during the voting period.
3. **Queue:** If passed, the proposal enters the Timelock.
4. **Execute:** After the delay, the proposal actions are performed on-chain.

## Quick Start
1. `npm install`
2. Deploy `GovernanceToken.sol` and `Timelock.sol`.
3. Deploy `GovernorContract.sol` using the addresses from step 2.
