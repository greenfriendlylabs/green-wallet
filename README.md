# GreenWallet

A full-stack, eco-friendly cryptocurrency wallet and decentralized exchange (DEX) built for the **Terra Classic (LUNC)** blockchain. GreenWallet lets you manage assets, swap tokens, stake LUNC, participate in governance, and explore the chain - all from a single browser-based interface powered by the Keplr wallet extension.

<img alt="green_wallet" src="https://github.com/user-attachments/assets/a3621d48-3dc1-4d4b-82d0-468864a582f7" />

---

## Features at a Glance

- **Wallet** - Send and receive LUNC, USTC, and CW20 tokens
- **Swap** - AMM-based token swaps with slippage protection and liquidity management
- **Staking** - Delegate, undelegate, redelegate, and claim staking rewards
- **Governance** - Browse and vote on on-chain proposals
- **Explorer** - Search transactions, addresses, and blocks
- **Faucet** - Claim LUNC from the community faucet
- **Dashboard** - Live network stats, token price charts, and portfolio overview
- **Dark Mode** - Full dark/light theme toggle
- **Mainnet + Testnet** - Supports Columbus-5 (mainnet) and Rebel-2 (testnet)

---

## Pages

### Dashboard
The home screen gives a real-time snapshot of the Terra Classic network:
- LUNC price with 24-hour change (via CoinGecko)
- Current block height, total supply, bonded tokens
- Active validator count and active governance proposals
- 7-day LUNC price history chart
- Token distribution pie chart (bonded / circulating / community pool)
- Top validators by voting power
- Portfolio widget showing your connected wallet's asset breakdown
- Governance widget with recent proposals
- All data auto-refreshes every 30 seconds

### Wallet
Full asset management for native and CW20 tokens:
- View balances for LUNC, USTC, and any native denom
- Add and manage CW20 tokens from the official Terra Classic token registry
- Add custom CW20 tokens by contract address
- Send native tokens with memo support
- Send CW20 tokens with correct decimal handling
- Max amount button with automatic gas reservation
- Copy wallet address to clipboard
- Balances refresh every 30 seconds
- Token selections persist in local storage

### Swap
AMM-powered token swapping backed by on-chain CosmWasm contracts:

**Swap tab**
- Swap LUNC and USTC (native AMM pool)
- Swap LUNC and custom CW20 tokens (CW20 AMM pool)
- Real-time swap simulation with expected output
- Price impact indicator (low / medium / high)
- Exchange rate display
- Slippage tolerance: 0.1%, 0.5%, 1%, 2%, or custom
- Minimum received amount calculated before you sign
- One-click token flip

**Liquidity tab**
- Add liquidity (both tokens auto-calculated for correct ratio)
- Estimated LP tokens shown before confirming
- Remove liquidity with estimated token return
- View your LP balance and share of the pool
- Pool statistics panel: reserves, current price, your pool share

### Staking
Complete staking interface for LUNC:
- Browse all active validators with moniker, commission rate, voting power, and jailed status
- Search validators by name
- Delegate LUNC to any validator
- Undelegate with the standard 21-day unbonding period
- Redelegate to a different validator without waiting
- Claim staking rewards from all delegations in one transaction
- View all active delegations and pending rewards
- View unbonding queue with completion timestamps
- Staking overview: total staked, total claimable rewards, unbonding count

**Validator operator tools** (for node operators):
- Edit validator info (moniker, identity, website, security contact, details)
- Withdraw pending validator commission
- View pending commission amounts
- GreenFriendlyLabs validator highlighted in the list

### Governance
Full on-chain governance participation:
- Browse all proposals with pagination
- Filter by status: All, Voting Period, Passed, Rejected
- Proposal cards show title, status, voting period, and current vote tallies
- Click any proposal for full details in a modal
- Vote directly from the app: YES, NO, ABSTAIN, NO_WITH_VETO
- Your votes are tracked and shown with visual indicators
- Voting result percentages displayed per option

### Explorer
On-chain search tool:
- Search by transaction hash, wallet address, or block height
- Transaction view: hash, block height, timestamp, gas used, fees, message type, success/failure
- Address view: balances and paginated transaction history
- Block view: proposer info and transaction count
- Copy-to-clipboard for hashes and addresses
- Links out to the full Terra Finder explorer

### Faucet
Community faucet integration:
- View faucet balance and total claim stats
- Claim LUNC tokens (subject to rate limiting per IP address)
- Staking requirement check before claiming
- Displays faucet address for direct top-ups
- Success confirmation with claim amount

### Donate
One-click 100 LUNC donation to the GreenWallet project:
- Single button to send 100 LUNC to the project address
- Transaction status tracking (loading / success / error)
- Transaction hash shown on success

### GFT Token *(Coming Soon)*
Placeholder page for the upcoming GFT token feature - under active development.

---

## Smart Contracts

Three CosmWasm contracts handle all on-chain DEX logic:

| Contract |  Description |
|---|---|
| Native AMM Pool | LUNC / USTC constant-product AMM (x times y = k) |
| CW20 Token | ERC-20 equivalent token template |
| CW20 AMM Pool | LUNC / custom-CW20 AMM pool |

**AMM Pool features:**
- Constant product formula (x times y = k)
- Configurable swap fee (default 0.3%)
- Protocol fee collection
- LP token minting and burning for liquidity providers
- Slippage protection on all swaps
- Admin controls: pause, fee updates

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 18 + TypeScript |
| Build tool | Vite 5 |
| State management | Zustand 4 |
| Blockchain client | CosmJS 0.32 |
| Wallet | Keplr browser extension |
| HTTP client | Axios |
| Charts | Recharts |
| Icons | Lucide React |
| Smart contracts | Rust / CosmWasm |
| Linting | ESLint |

---

## Network Support

| Network | Chain ID | LCD Endpoint |
|---|---|---|
| Mainnet (Columbus-5) | columbus-5 | terra-classic-lcd.publicnode.com |
| Testnet (Rebel-2) | rebel-2 | terra-testnet-lcd.publicnode.com |

---

## Prerequisites

- Node.js 18 or higher
- [Keplr browser extension](https://www.keplr.app/)

---

## Supported Tokens

| Token | Type | Description |
|---|---|---|
| LUNC (uluna) | Native | Luna Classic - primary gas and staking token |
| USTC (uusd) | Native | Terra Classic USD stablecoin |
| GFT (gft) | CW20 | Greenfriendly Token |
| Custom | CW20 | Any CW20 token added by contract address |

---

## Donations & Support
Want to support the sustainability of **Green Wallet**?

**Donate LUNC to:**
```
terra1l9q4guus5vjxl84d5qea068vcen32l04jmc55w
```

## License
This project is open-source under the **MIT License**.

## Contributing
We welcome contributions! Feel free to fork, create pull requests, or report issues.

## Contact & Community
Join us to discuss and improve **Green Wallet**:
- [Twitter](https://twitter.com/GreenFrndLabs)
- [Website](https://www.greenfriendlylabs.com/)

---
Together, let's build a sustainable **LUNC** future! 🌿🚀

