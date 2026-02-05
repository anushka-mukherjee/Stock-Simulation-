# Stock Simulation Game

A real-time stock market trading simulation game built in OCaml. This project simulates a real-life stock market on a smaller scale, allowing users to invest in stocks, index funds, and certificates of deposit (CDs). Compete against an AI bot to see who can make the smartest investments and achieve the highest net worth over 20 years.

> **Note:** This was the final project for CS 3110 at Cornell University, developed in collaboration with Josue Garcia and Joey Morquecho.

## Overview

The Stock Simulation Game provides an interactive trading experience where players start with a set amount of cash and compete against a bot over a 20-year period. The game uses historical stock market data from Yahoo Finance to simulate realistic market conditions. The goal is to make smart investment decisions and "beat the market" by outperforming the bot, which only invests in index funds.

## Features

### Trading Options
- **Individual Stocks**: Buy and sell shares of various companies (e.g., AAPL, MSFT, GE, XOM, COKE, JNJ)
- **Index Funds**: Trade S&P 500 and Real Estate index funds
- **Certificates of Deposit (CDs)**: Invest in CDs with terms of 6 months, 1 year, or 3 years

### Game Mechanics
- **Real-time Simulation**: 1 second = 1 month in game time
- **Duration**: 20 years (240 months) of simulated trading
- **Historical Data**: Uses authentic 1995 stock price data from Yahoo Finance
- **Multi-currency Support**: USD, CAD, EUR, GBP, CHF, NZD, AUD, JPY

### Portfolio Management
- Track your cash balance and total net worth
- View portfolio allocation percentages
- Monitor stock prices and percentage changes in real-time
- Color-coded profit/loss indicators (green for gains, red for losses)

### Competition
- Compete against an AI bot that invests in index funds
- Winner is determined by net worth at the end of 20 years
- Real-time comparison of your performance vs. the bot

## Prerequisites

- OCaml (with opam package manager)
- Make

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd Stock-Simulation--master
```

2. Install dependencies:
```bash
make install
```

This will install the required packages:
- `OUnit2` (for testing)
- `ANSITerminal` (for colored terminal output)

## Building

To build the project:
```bash
make build
```

## Running the Game

To start the simulation:
```bash
make play
```

## Testing

To run the test suite:
```bash
make test
```

## Game Commands

### Viewing Information
- `s` - View all available stocks and their current prices
- `i` - View index funds
- `cd` - View certificate of deposit rates and terms
- `view_index` - View index fund details
- `cash` - Display your current cash balance
- `networth` - Display your total net worth
- `portfolio` - View your portfolio breakdown
- `portfolio_percent` - View portfolio allocation percentages
- `checkstock [stock #]` - View details of a specific stock
- `view_cd` - View your purchased CDs
- `bot` - View the bot's current net worth
- `help` - Display all available commands

### Trading Commands
- `buy_s [stock #] [# of shares]` - Buy shares of an individual stock
- `sell_s [stock #] [# of shares]` - Sell shares of an individual stock
- `buy_index [index_fund_#] [# of shares]` - Buy shares of an index fund
- `sell_index [index_fund_#] [# of shares]` - Sell shares of an index fund
- `buy_cd [term] [amount]` - Purchase a CD
  - Term options: `1` (6 months), `2` (12 months), `3` (36 months)
- `sell_cd [cd #]` - Sell a certificate of deposit

### Game Control
- `start` - Begin the simulation
- `quit` - Exit the game

## How to Play

1. **Start the game**: Run `make play` and type `start` when prompted
2. **Choose currency**: Select your preferred currency (USD, CAD, EUR, etc.)
3. **Monitor the market**: Use `s` and `i` to view available investments
4. **Make trades**: Buy and sell stocks, index funds, and CDs based on market conditions
5. **Track performance**: Monitor your net worth and compare it to the bot using `networth` and `bot`
6. **Win the game**: Achieve a higher net worth than the bot after 20 years!

## Project Structure

```
Stock-Simulation--master/
├── data/              # Historical stock price data files
├── *.ml               # OCaml source files
├── *.mli              # OCaml interface files
├── Makefile           # Build configuration
├── INSTALL.txt        # Installation instructions
└── README.md          # This file
```

## Technologies Used

- **OCaml** - Functional programming language
- **ANSITerminal** - Terminal output formatting and colors
- **OUnit2** - Unit testing framework
- **ocamlbuild** - Build system

## Data Sources

Stock price data is sourced from Yahoo Finance, specifically historical data from 1995. The data files are located in the `data/` directory.


