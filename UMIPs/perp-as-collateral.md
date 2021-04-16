Perpetual Protocol

## Headers
| UMIP-tbd   |                                                                                                                                          |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| UMIP Title | Add PERP as approved collateral currency          |
| Authors    | John Shutt (john@umaproject.org), Deepanshu Hooda (deepanshuhooda2000@gmail.com) |
| Status     | Draft                                                                                                                                    |
| Created    | April 16, 2021                                                                                                                           |
| [Discourse Link](TBD)    |       
# Summary (2-5 sentences)
This UMIP will add PERP as approved collateral currency. This will involve adding PERP to the whitelist and adding flat final fees to charge per-request.
# Motivation
Perpetual Protocol builds on an Uniswap-inspired automated market maker (AMM) design (constant product curve).
By adding PERP as collateral, it will be possible to create derivative contracts such as KPI options. This is an opportunity to incentive growth of the PERP platform alongside the usage of KPI options.

# Proposed Collateral Currency


## PERP (Perpetual Protocol)

### Technical Specification
To accomplish this upgrade, two changes need to be made:

 * The Perpetual Protocol address, [0xbc396689893d065f41bc2c6ecbee5e0085233447][PERP], needs to be added to the collateral currency whitelist introduced in UMIP-8.
 * A final fee of 53 PERP  needs to be added in the Store contract. 

 [PERP ]: https://etherscan.io/token/0xbc396689893d065f41bc2c6ecbee5e0085233447

# Rationale
53 PERP was chosen for the fee because this sits around $400, which we have seen other collateral tokens use in the past.

# Security considerations

The only security implication is for contract deployers and users who are considering using EMP contracts with this token as the collateral currency. 
They should recognize that, relative to most fiat currencies, these assets are much more volatile. This volatility should be taken into account when parameterizing or using these EMP contracts.


