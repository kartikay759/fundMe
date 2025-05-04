# fundMe
FundMe is a decentralized crowdfunding smart contract built using Solidity on the Ethereum blockchain. This application allows users to contribute ETH to the contract, with real-time USD price validation using Chainlink Price Feeds. The contract enforces a minimum funding amount (e.g., $5 USD) and allows only the contract owner to withdraw the collected funds. Key components include:
🔧 Technical Highlights

    Solidity Smart Contracts:

        Uses PriceConverter library to fetch live ETH/USD rates via Chainlink AggregatorV3Interface.

        Implements fund(), withdraw(), and fallback functions to handle direct ETH transfers.

        Uses modifiers (onlyOwner) and custom error handling (NotOwner) for gas efficiency and security.

    Chainlink Integration:

        Real-time price conversion ensures the funder contributes a minimum USD-equivalent ETH.

        Demonstrates understanding of oracles and external data in smart contracts.

    Best Solidity Practices:

        Use of immutable and constant variables for gas optimization.

        Clean use of call() for secure ETH transfers.

        Fallback and receive() functions for robustness.

    Security & Optimization:

        Proper access control using modifiers.

        Resets mappings and funders list post-withdrawal to prevent state pollution.

        No redundant state writes, avoiding unnecessary gas costs.
