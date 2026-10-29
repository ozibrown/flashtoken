# QToken (Q / SDT)

QToken is a fixed-supply TRC-20-compatible token contract for the TRON network. It is an independent token and is **not USDT**, is not issued by or affiliated with Tether, and does not represent a claim on US dollars or any other asset.

## Token details

| Property | Value |
| --- | --- |
| Token name | Q |
| Symbol | SDT |
| Decimals | 6 |
| Fixed total supply | 1,000,000 SDT |
| Contract | `QToken` |
| License | MIT |

The full supply is assigned to the deploying address in the constructor. The contract has no mint, burn, owner, tax, blacklist, pause, or hidden transfer restriction. No additional tokens can be created through this contract after deployment.

## Contract

Source: [`contracts/QToken.sol`](contracts/QToken.sol)

The contract provides the standard token operations and public data commonly used by wallets and decentralized exchanges:

- `transfer` — send tokens to another address.
- `approve` and `transferFrom` — authorize a contract to transfer tokens.
- `balanceOf`, `allowance`, `totalSupply`, `name`, `symbol`, and `decimals` — read token data.

## Mainnet address

The address shown on the TRONSCAN page supplied by the project owner is:

`TWjsSRwfwSVxpEnkSuAC6kMNZ8CeL155Ga`

Always verify the address and the published contract source directly on TRONSCAN before interacting. Token symbols are not unique; confirm the full contract address rather than relying on `Q`, `SDT`, or a logo.

## Explorer status

As of October 29, 2026, a supplied TRONSCAN screenshot showed this contract with an **Unsafe** reputation label and a warning that multiple users had reported the account as phishing. This README does not claim that the warning has been removed or resolved. Check the current explorer status and review the contract yourself before sending assets, approving a spender, or providing liquidity.

## Price, liquidity, and risks

The contract does not set a market price, guarantee value, create liquidity, or provide a redemption right. A DEX pool must be separately created and funded with this token and another asset. The first pool's reserve ratio determines its initial quoted price; that price is not a guarantee of fair value or of future buyers. Liquidity providers can lose value through price changes, slippage, and impermanent loss.

There is no independent security audit included with this project. Do not treat wallet display, token balance, or a DEX quote as proof that the tokens have a particular cash value or can be withdrawn on a centralized exchange.

## Development and deployment

The contract uses Solidity `^0.8.20`. It can be compiled in a TRON-compatible Solidity environment such as TronIDE. The constructor takes no arguments. Deployment requires a TRON wallet and network resources; mainnet deployment and transactions use real TRX and are irreversible.

This repository does not include private keys, wallet connection code, deployment automation, a logo, an audit, or a DEX liquidity position.
