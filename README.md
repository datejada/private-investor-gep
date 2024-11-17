# Private Investor GEP

Private investor generation expansion planning example.

## Overview

This project demonstrates a generation expansion planning model for a private investor using Pyomo, a Python-based open-source optimization modeling language. The model optimizes the investment and operation of a photovoltaic (PV) system to meet household electricity demand in Spain.

## Project Structure

- **inputs/**: Contains input data files for the model.
  - `dayahead_price_forecast.csv`: Day-ahead electricity price forecast.
  - `electricity_demand_profile_household_spain.csv`: Household electricity demand profile in Spain.
  - `solar_pv_spain_uncorrected.csv`: Uncorrected solar PV generation profile in Spain.
- **private-investor-gep.ipynb**: Jupyter Notebook implementing the generation expansion planning model.
- **LICENSE**: License file for the project.
- **README.md**: This file.

## Installation

To run this project, you need to have Python installed. You can install the required packages using pip:

```sh
pip install pyomo highspy pandas matplotlib seaborn
```

## Usage
1. Clone the repository:
```sh
git clone https://github.com/yourusername/private-investor-gep.git
cd private-investor-gep
```
2. Open the Jupyter Notebook:
```sh
jupyter notebook private-investor-gep.ipynb
```
3. Run the cells in the notebook to execute the model and visualize the results.

## Model Description
The model includes the following components:

- Decision Variables:
    - `v_production`: Electricity production from the PV system.
    - `v_purchasing`: Electricity purchased from the grid.
    - `v_selling`: Electricity sold to the grid.
    - `v_investment`: Investment in the PV system.

- Expressions:
    - `e_demand`: Electricity demand.
    - `e_savings`: Savings from electricity production.
    - `e_taxes`: Taxes on electricity sales.
    - `e_investment_cost`: Investment cost.
    - `e_fix_om_cost`: Fixed operation and maintenance cost.

- Objective Function: Maximizes the net savings by considering savings from production, taxes, investment cost, and fixed operation and maintenance cost.

- Constraints:
    - Maximum production constraint.
    - Balance constraint ensuring supply meets demand.

- Results: The results of the model are stored in a DataFrame and visualized as a heatmap showing the production over time.

## License
This project is licensed under the MIT License. See the LICENSE file for details.