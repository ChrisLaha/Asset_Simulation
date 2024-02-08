# Asset_Simulation
This project leverages Python to simulate and analyze different portfolio allocations among stocks, bonds, and T-bills to identify the strategy that generates the highest returns over a 40-year period. The simulation incorporates historical return data and accounts for annual inflation, providing insights into the long-term performance of diversified portfolios versus a 100% stock allocation strategy.

Overview
The goal of this project is to estimate the probability distribution of a fund's balance after 40 years, given an initial balance and consistent annual investments. The simulation explores how different allocations among T-bills, bonds, and stocks affect the portfolio's final value, considering the uncertainty in annual returns and inflation. The project also evaluates the impact of a 100% stock allocation to understand the trade-offs between risk and return.

Methodology
The simulation model uses historical data on returns and inflation from 1946 to 2007 to specify the probability distribution of returns for T-bills, bonds, and stocks. A damping factor controls the relevance of older data, giving more weight to recent years. The final value of the portfolio is discounted to present value using random inflation rates drawn from the historical data.

Key Model Components
Deterministic Model Inputs:

N: Number of investment years (e.g., 40)
Y: Annual investment amount (e.g., $1000)
x: Fraction of annual investment allocated to T-bills, T-bonds, and stocks
pt: Percent change in T-bills, T-bonds, and stocks in year t
it: Inflation rate in year t
damp: Damping factor to adjust the weight of historical data
Outputs:

Pt: Portfolio multiplier in year t
Vt: Value of the investment at the end of year t
Dt: Discount factor through the end of year t
Z: Present value of the portfolio after N years
Stochastic Elements
The model treats returns for T-bills, T-bonds, stocks, and inflation as random values drawn from a discrete distribution based on historical data. A damping factor adjusts the probability weights for each year, prioritizing more recent data.

Implementation
The simulation was implemented in Python, utilizing libraries such as NumPy, Pandas, and Matplotlib for data manipulation and visualization. The simShell function encapsulates the simulation logic, generating samples of random outputs based on the specified allocation strategies and calculating the present value of the portfolio for each scenario.

Results
The project includes a comparison of different allocation strategies to determine which mix of T-bills, T-bonds, and stocks offers the highest expected returns after 40 years, discounted to present value. It also assesses the viability of a 100% stock allocation by examining its potential for higher returns against the backdrop of increased risk (volatility).

Running the Simulation
To run the simulation, ensure you have the required historical data file (asset_data.csv) in the same directory as the script. The main Python script (simulation_model.py) can be executed in any Python environment that supports NumPy, Pandas, and Matplotlib.

Conclusion
This project demonstrates the power of simulation in financial planning and portfolio management, offering valuable insights into long-term investment strategies. By comparing diversified portfolios with a 100% stock allocation, investors can make informed decisions based on their risk tolerance and return expectations.

Future Work
Future enhancements could include expanding the simulation to incorporate more asset classes, implementing more sophisticated risk management techniques, and exploring the impact of different economic scenarios on portfolio performance.
