# Mortgage-Credit-Risk-Stress-Testing-in-Python
A Python project analysing Freddie Mac mortgage data and comparing credit losses under baseline and stress scenarios using historical event rates and Monte Carlo simulation.

## Data
- 50,000 US mortgages from Freddie Mac's 2025 sample.
- Monthly performance records from January 2025 to June 2026.
- Analysis uses a selected subset with sufficient follow-up.1. **Portfolio size:** The stress portfolio contains 4,050 mortgage loans,
   with total exposure of approximately USD 1.407 billion.

  ## Method
1. Clean and validate the loan data.
2. Estimate a common PD using historical credit-event rates.
3. Apply illustrative PD and collateral stress assumptions.
4. Simulate portfolio losses using independent Monte Carlo draws.

   ## Key Findings
1. **Expected Loss (EL):** Expected loss represents the average credit loss
   implied by the assumed probability of default, loss given default and
   exposure. It increases from USD 609,259 under baseline to USD 5,122,514
   under severe stress, approximately 8.4 times the baseline level.

2. **Tail losses:** Under severe stress, the 99% Value at Risk (VaR) is
   USD 7,195,730, the estimated 99th percentile of simulated portfolio losses.
   The 99% Expected Shortfall (ES) is USD 7,461,465, representing the average
   loss across the worst 1% of simulations.

3. **Loan-to-Value (LTV) analysis:** Original LTV measures the initial loan
   amount relative to the property's value at origination. The >90% LTV
   band includes loans whose initial amount exceeded 90% of the property's
   value. This group contributes the largest total expected loss under
   severe stress. Its contribution reflects both the group's exposure
   and its assumed loss severity, rather than LTV alone.

   ## Limitations
PD is shared across loans. LGD and stress shocks are assumed.
Defaults are simulated independently and exposure is held constant.
