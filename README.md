# Furlong Backtest

An event-driven quantitative research and execution simulator for studying how market conditions, transaction costs, and execution assumptions influence trading-strategy performance.

## Overview

A strategy that appears profitable under idealized assumptions may perform differently once fees, spread, latency, partial fills, and inventory constraints are considered.

Furlong Backtest aims to provide a reproducible environment for evaluating these effects.

## Core Features

* **Event-Driven Simulation:** Process market events and simulated orders chronologically.
* **Execution Modeling:** Account for bid-ask spread, fees, slippage, and partial fills.
* **Latency Modeling:** Simulate configurable delays between decisions and execution.
* **Queue Assumptions:** Model queue position and fill probability with explicitly documented assumptions.
* **Risk Controls:** Implement position limits and inventory constraints.
* **Performance Analytics:** Calculate P&L, drawdown, turnover, and transaction costs.
* **Experiment Reproducibility:** Support fixed random seeds and recorded configurations.

## Technical Stack

* C++20 simulation core
* Python for analysis and visualization
* CMake
* GoogleTest
* CSV or Parquet datasets, where appropriate

## Research Questions

* How sensitive is strategy performance to execution latency?
* How do transaction costs affect net returns?
* How do queue-position assumptions change simulated fill rates?
* How much does performance deteriorate under adverse market conditions?
* Does a strategy remain robust across different time periods?

## Evaluation Methodology

* Compare idealized and cost-aware execution.
* Separate research data from out-of-sample evaluation data.
* Include simple baselines.
* Report assumptions, uncertainty, and limitations.
* Avoid look-ahead bias and unrealistic fill assumptions.

## Metrics

* Gross and net P&L
* Maximum drawdown
* Turnover and transaction costs
* Fill ratio and partial-fill rate
* Inventory exposure
* Execution latency sensitivity

## Project Status

Under development. Strategy results will be published only after implementation, validation, and reproducible testing.

## Disclaimer

This project is intended for education and quantitative research. Simulated performance is not evidence of future profitability.
