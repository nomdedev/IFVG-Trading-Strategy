# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a single TradingView Pine Script v6 indicator that combines multiple technical analysis components:

- **Main Script**: `tradingview_script_corrected.pine` - A unified indicator combining Squeeze/ADX/RSI/TTM Waves/CMF/EMAs/IFVG functionality

## Architecture

### Core Components

The Pine Script implements a multi-signal trading indicator with these key systems:

1. **Squeeze Oscillator**: Compares Bollinger Bands with Keltner Channels to detect compression/expansion phases
2. **ADX (Average Directional Index)**: Measures trend strength and direction using DI+/DI- 
3. **TTM Waves**: Three MACD-like waves for multi-timeframe momentum analysis
4. **CMF (Chaikin Money Flow)**: Volume-weighted momentum indicator
5. **RSI**: Standard momentum oscillator with 30/70 crossover signals
6. **EMAs**: Up to 3 configurable exponential moving averages for trend filtering
7. **IFVG (Fair Value Gaps)**: Identifies price gaps that act as support/resistance zones

### Signal Generation System

- **Scoring System**: Combines all indicators using configurable weights
- **Filter System**: Advanced filtering with ADX, z-score, EMA alignment, IFVG proximity, and volume spikes
- **Weighted Filters**: Statistical approach using historical performance to weight filter importance
- **Signal Types**: Strong/weak buy/sell signals with deduplication logic

### Key Data Structures

- `ifvg_boxes[]`: Array storing IFVG zone boxes for visualization
- `ifvg_highs[]`/`ifvg_lows[]`: Arrays storing IFVG boundary values for proximity calculations
- `returns[]`: Rolling window of log returns for Monte Carlo simulations
- Filter counting arrays for statistical weight calculation

### Configuration

The script includes extensive input parameters organized by functionality:
- Display controls (`show_SQZ`, `show_ADX`, `showWaves`, etc.)
- Technical parameters (lengths, multipliers, thresholds)
- Filter settings (enable flags, thresholds, minimum requirements)
- Evaluation/backtesting settings
- Visualization options

## Development Notes

### File Structure
- Single file architecture - all functionality contained in one Pine Script
- No build system or external dependencies
- Direct deployment to TradingView platform

### Key Functions
- `signal_passes_filters()`: Evaluates how many filters a signal passes
- `is_near_ifvg()`: Checks proximity to Fair Value Gap zones  
- `z_normalize()`: Standardizes indicator values for comparison
- `percentile_from_array()`: Calculates percentiles for Monte Carlo bands
- `sum_n()`: Optimized rolling sum using cumulative sums

### Performance Considerations
- Uses vectorized operations where possible to avoid Pine Script execution limits
- Implements efficient rolling window management for historical data
- Statistical calculations are performed only on last bar when possible

## Testing

This Pine Script is designed for TradingView platform testing:
- Use TradingView's Strategy Tester for backtesting
- Enable evaluation mode (`eval_enable = true`) for performance metrics
- Adjust timeframes and assets to validate signal effectiveness
- Monitor execution time and memory usage on different chart types