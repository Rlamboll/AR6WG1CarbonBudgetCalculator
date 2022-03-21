# Carbon Budget Calculator
Calculates remaining carbon budget given atmospheric simulation inputs. 
The workhorse script is `src/run_budget_calculator.py`
Expects to find data from MAGICC or FaIR simulations in the `InputData` folder in the 
standard format output for a pyam dataframe. Specification of how to read this data 
and options for running the code are all found at the beginning of 
`src/run_budget_calculator.py`. 

The calculation is based on the framework in 
*Estimating and tracking the remaining carbon budget for stringent climate targets*, 
Rogelj et al. 2019. This revolves around five terms: the warming to date (input 
directly), the non-CO2 warming (calculated from scenarios analysed previously by MAGICC 
or FaIR), the zero-emissions commitment (ZEC, input directly), the  transient climate 
response to cumulative emissions of CO2 (TCRE, parameters are input for a distribution
which may be either lognormal or normal)
and unrepresented Earth feedbacks (a linear function of temperature change).   
