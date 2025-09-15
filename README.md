# Soroswap API Example

A TypeScript example demonstrating how to use the Soroswap SDK to interact with the Soroswap DEX on Stellar network.

## Overview

This project showcases how to:
- Quote token swaps using the Soroswap API
- Build swap transactions
- Sign and submit transactions to the Stellar network

## Prerequisites

- Node.js (v18 or higher)
- npm or pnpm
- A Stellar account with:
  - Testnet XLM for fees
  - Trustlines established for the tokens you want to trade
- Soroswap API key

## Installation

1. Clone this repository
2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   ```bash
   cp .env.example .env
   ```

4. Edit the `.env` file with your actual values:
   - `SOROSWAP_API_KEY`: Your API key from api.soroswap.finance
   - `USER_SECRET`: Your Stellar account secret key
   - `SOROSWAP_API_URL`: API endpoint (optional, defaults to production)

## Usage

### Development
```bash
npm run dev
```

### Build and Run
```bash
npm run build
npm run start:build
```

## Configuration

The example is configured to:
- Trade on Stellar Testnet
- Swap 1 XLM for USDC
- Use 0.8% slippage tolerance
- Route through Soroswap protocol

### Token Addresses (Testnet)
- **XLM**: `CDLZFC3SYJYDZT7K67VZ75HPJVIEUVNIXF47ZG2FB2RMQQVU2HHGCYSC`
- **USDC**: `CDWEFYYHMGEZEFC5TBUDXM3IJJ7K7W5BDGE765UIYQEV4JFWDOLSTOEK`

## Code Structure

- `src/index.ts`: Main example implementation
- `.env.example`: Environment variables template
- `package.json`: Project dependencies and scripts

## API Rate Limiting

The example includes rate limiting delays to respect API limits. Each API call is followed by a 1-second delay.

## Error Handling

The code includes basic error handling that will log any issues encountered during the swap process.

## Dependencies

- **@soroswap/sdk**: Official Soroswap SDK
- **@stellar/stellar-sdk**: Stellar SDK for transaction handling
- **dotenv**: Environment variable management
- **TypeScript**: Type safety and development experience

## Getting API Access

1. Visit [api.soroswap.finance](https://api.soroswap.finance)
2. Register for an API key
3. Add the key to your `.env` file

## Security Notes

- Never commit your `.env` file with real credentials
- Use testnet for development and testing
- Ensure your account has sufficient XLM for transaction fees
- Verify token addresses before trading

## License

ISC