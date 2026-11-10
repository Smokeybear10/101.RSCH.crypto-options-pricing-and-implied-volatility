# Options Pricing Research

A proposal for a C++ engine that updates crypto option prices, Greeks, and implied volatility from streamed or replayed market data.

## Start Here

Read the [initial pitch](PITCH.md). It describes the intended market-data pipeline, pricing engine, and Qt6 interface.

This repository is at the proposal stage. It has no implementation, datasets, saved experiments, or measured results yet.

## Planned Scope

The proposed first version maintains market state, reprices an option chain as the underlying changes, and displays model outputs. Monte Carlo pricing, American option support, and Greeks are discussed in the pitch. CUDA acceleration, SIMD, and volatility-smile calibration are possible later extensions.

## Evaluation Still Needed

The pitch leaves the target platform and performance goals open. Pricing correctness, latency, and throughput need measured checks on specified data and hardware before making performance claims. A difference between a model price and a market quote would also need evaluation before being treated as a trading signal.

There are no reproduction commands at this stage. The pitch records intended work rather than completed findings.
