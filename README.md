# American-Option-pricing-using-Binomial-Tree-and-Monte-Carlo-Simulation

This project estimates the price of an American call option on NVIDIA (NVDA) stock by combining a binomial tree model with Monte Carlo simulations. Real historical data is incorporated to adjust for volatility, capturing early exercise opportunities unique to American options.

## Project Overview

1. **Data Processing**: Historical price data at 10-minute intervals is used to compute log returns and daily volatility. This helps create a volatility measure that more accurately reflects market fluctuations.
2. **Risk-Free Rate and Stock Data**: Treasury rates and NVIDIA stock data are pulled using `yfinance` for accurate pricing inputs.
3. **Volatility Adjustments**: A combined volatility measure is calculated, integrating both historical and custom adjustments to account for different market conditions.
4. **Option Pricing**: A binomial tree model simulates potential stock price paths, allowing for early option exercise. Monte Carlo simulations enhance this model by incorporating more scenarios to estimate the American option price accurately.
5. **Visualization**: The project plots real vs. estimated option prices, along with moneyness over time, to analyze accuracy and trends.

## Why Monte Carlo Simulation?

Monte Carlo simulation refines the binomial tree model by sampling a wide range of possible outcomes. This approach is particularly effective for American options, where the option holder has the flexibility to exercise early. By capturing this flexibility across various volatility conditions, Monte Carlo simulations provide more accurate price estimates.

## Dependencies

- `yfinance`
- `numpy`
- `matplotlib`
- `pandas`

## Usage

1. Clone the repository and ensure you have the necessary libraries installed.
2. Place the `10min stock data.xlsx` file in the project directory.
3. Run the script to generate option price estimates and visualizations.

## License

This project is open source under the MIT License.

