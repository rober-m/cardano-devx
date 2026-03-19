# ContractsLibrary Library

## Dependencies

No dependencies

## Description

OpenZeppelin-like library. 

We'll design and implement a **library of standardized, reusable smart contracts — both on-chain and off-chain — with an initial focus on building blocks and DeFi primitives.** 

Inspired by OpenZeppelin's role in the EVM ecosystem, this library will provide battle-tested, ready-to-use contract implementations that developers can use as building blocks, inspiration, or a ready-to-go implementation for their applications. 

The deliverable includes creating the library's infrastructure and website and shipping _at least_ 5 ready-to-audit smart contracts (both on-chain and off-chain). For example, Vesting, Programmable Tokens, DEX (Decentralized Exchanges), Swap, Lending, and other contracts.

> [!NOTE]
> It's important to note the difference between this library and libraries like Anastasia Labs's [design-patterns](https://github.com/Anastasia-Labs/design-patterns) and [Vodka](https://github.com/sidan-lab/vodka). While libraries like `vodka` contain small on-chain utility functions and the `design-patterns` library contains fully-fledged on-chain generic patterns, our library's level of abstraction will be at the use case level and provide both on-chain and off-chain. We could say that we'll stand on the shoulders of libraries like those.

## Related Resources

[cardano-template-and-ecosystem-monitoring](https://github.com/cardano-foundation/cardano-template-and-ecosystem-monitoring) tracks real-world Cardano use cases and implementations, and can serve as a source of insights for identifying which contract patterns are most needed in practice. Similarly, [Mesh SDK's contract package](https://github.com/MeshJS/mesh/tree/main/packages/mesh-contract) and the [Cardano Developer Portal's example contracts](https://developers.cardano.org/docs/build/smart-contracts/example-contracts/) provide/reference existing implementations that can inform the design of this library.

## Outcome

By providing canonical implementations of common smart contract use cases, this library will significantly reduce the time and risk required to build on Cardano.
