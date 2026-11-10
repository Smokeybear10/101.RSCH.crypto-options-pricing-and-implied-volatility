# Pricing Engine — Initial Pitch

## Project Overview

This project is a real-time C++ pricing engine for listed crypto options.

The system takes live market data from crypto exchanges, updates the current market state, reprices the relevant option chain, and displays the results in a Qt6 dashboard. The goal is not to build a simple Black-Scholes calculator. The goal is to build the full pipeline from live market data to updated option prices on screen.

This makes the project a strong mix of quantitative finance, systems programming, performance engineering, and live visualization.

## Core Idea

A trader looking at crypto options needs to understand how prices, Greeks, and implied volatility are changing in real time. This engine would help by continuously updating model prices and highlighting contracts that may be mispriced relative to the market.

The first version would focus on building a clean, working demo:

- Stream or replay crypto market data.
- Maintain an updated market state.
- Reprice an option chain when the underlying price changes.
- Display prices, Greeks, and implied volatility in a live dashboard.
- Highlight possible volatility mispricings.

## Why This Is Interesting

The project is interesting because it combines multiple difficult areas into one practical system.

The pricing side involves option pricing models, Monte Carlo simulation, American option support, and Greeks. The systems side involves live market data, efficient updates, and low-latency processing. The interface side makes the project visible and usable by showing the results in a real-time dashboard.

A pricing model by itself is useful, but a pricing model connected to live data and a working interface is much more impressive and practical.

## What Makes It Strong

The strongest part of this project is that it is not just theoretical. It has a clear end-to-end path:

> live exchange data → market state → pricing engine → dashboard → mispricing signal

That makes it useful as both a trading research tool and a technical portfolio project. A good demo would let someone watch the market move, see the option chain update, and immediately understand where the engine thinks volatility may be mispriced.

## Stretch Goals

After the core version works, the project could be extended with:

- CUDA acceleration for faster Monte Carlo pricing.
- CPU SIMD support for a faster fallback path.
- Benchmarking for tick-to-render latency.
- More advanced volatility-smile calibration.
- A ranked volatility mispricing scanner.

## Open Questions

The main early decision is the target platform. CUDA requires NVIDIA hardware, so the project would likely need a Linux machine with a GPU, either locally or in the cloud.

Another important question is how to define "fast." Instead of making broad performance claims upfront, the project should measure latency and throughput on specific hardware once the system is working.

Finally, the first version should stay focused. The priority should be a clean live demo before adding every advanced pricing feature.

## One-Sentence Summary

A real-time C++ crypto options pricing engine that turns live exchange data into updated prices, Greeks, implied volatility, and mispricing signals inside a usable trading dashboard.
