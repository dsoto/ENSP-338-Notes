## Learning Objectives
- You will understand the basic concepts of the time value of money
- You will be able to calculate how financial instruments like loans and
  credit cards work

## Feedback on the reading

## Review
- Ideal circuit elements
- Kirchoff's Laws
- Equivalent resistors


## Concepts
- Ideal bank
- Comparsion principle

<!-- we connect the equivalence principle to the resistors -->

## Connection to energy efficiency
- Many energy projects are made attractive to consumers by providing
  financing so that people don't have to pay the entire cost at once.



## Informal poll
Would you rather have

- $1K now or $500 in a year?
- $1K now or $1K in a year?
- $1K now or $2K in a year?
- $1K now or $5K in a year?
- $1K now or $10K in a year?

<!--
questions for class
- why do you have these preferences
- how do we quantify these preferences?
-->

## Equivalence principle
- Given a choice between money now and money later, most demand a larger
  value if money is provided at a later date

<!--
this is as much art as science
-->

## Loans
- With a loan we essentially rent money and pay a percentage of the
  amount we still owe the lender

## Discount rate based on equivalence principle
- Banks have preferences that set their loan rates
- People have preferences that dictate their discount rate


## Discount Rate and Net Present Value
$$\textrm{Present Value (USD)} =
\frac
{\textrm{Future Amount (USD)}}
{(1 + \textrm{Discount Rate})^{\textrm{number of years}} }$$

$$P = \frac {F} {(1 + i)^{n} }$$


## Learning Objectives
- You will be able to use common financial methods (NPV, IRR, CRF) to compare energy
- Capital Recovery Function (CRF)
- Net Present Value (NPV)
<!-- (we can calculate the value now of future electricity bills) -->
- Internal Rate of Return (IRR)
<!--  (we can calculate the equivalent interest rate of an investment) -->

## Guiding Questions
- How do we compare two options with different costs over time?

## Two cash flows
![](../figures/two-option-cash-flow.pdf)

<!--
these could be
- energy appliances
- effort invested
- climate change decisions
-->

## Discount Rate and Net Present Value

$$FV = PV (1 + i)^{n}$$

$$PV = \frac {FV} {(1 + i)^{n} }$$

$$\textrm{Present Value (USD)} =
\frac
{\textrm{Future Amount (USD)}}
{(1 + \textrm{Rate})^{\textrm{number of years}} }$$

<!-- what was the point of yesterday's spreadsheet demo? -->

## Activity
- What is the present value of a $1000 payment 5 years from now with an
  interest rate of 10%?


## Strategy

<!-- 1000 / (1 + 0.10)^5 = $620.92 -->

## Activity
- What is the future value of $1000 payment today in 10 years at 7%
  interest?

## Strategy

<!-- 1000 * (1 + 0.07)^10 = 1967.15 -->

<!-- does anyone remember from the reading what NPV is -->

# Net Present Value (NPV)


## Net Present Value
- Provides a shorthand to calculate the present value of a stream of
payments.
- Provides a method of comparison for two different cash flows
- Cash flows can be compared for equivalence

<!-- do I have some cash flow plots or diagrams? -->

## Cash flow
- We think of discrete events in time where cash is paid or recieved

## Two options
![](../figures/two-option-cash-flow.pdf)

## Present Value

Single payment
$$ PV = \frac{C}{(1+i)^n} $$

Stream of payments
$$ PV = C_0 +
        \frac{C_1}{1+i} +
        \frac{C_2}{(1+i)^2} +
        \dots +
        \frac{C_N}{(1+i)^N}$$

Compact notation
$$ PV = \sum_{n=0}^{N} \frac{C_n}{(1+i)^n}$$

## Two options
![](../figures/two-option-cash-flow.pdf)


# Internal Rate of Return (IRR)

## Internal Rate of Return
- Tells us at what interest rate a cash flow has a net present value of
  zero
- We will look at this on a spreadsheet

# Capital Recovery Function

## Capital Recovery Function
Tells you how much the loan payment is for a given balance, number of
payments, and interest rate.

## Capital Recovery Factor

$$CRF = \frac {i(1+i)^n}{(1+i)^n-1}$$

## Additional Metrics for Energy Projects
- Cost of conserved energy
- Cost of avoided carbon

<!--

## Exercise
- What is the annual payment for a $10K loan with an interest rate of 5%
  paid over a period of 7 years?
- Solve on spreadsheet
- Solve using formula

## Solution
![](../figures/capital_recovery_factor.jpg)

-->

<!--
calculate a car loan
does it match what you expect?
-->

## Spreadsheet functions
- NPV(rate, payments) net present value
- IRR(payments, guess) internal rate of return
- PMT(rate, number of payments, principal)


## Learning Objectives
- Use conserved cost of energy as an investment metric

## Activity Objective
- Be able to use NPV, IRR, and CCE on calculator and computer

## Review
- How did we determine the cost of a loan?
- What were our methods?



## Capital Recovery Factor (CRF)
- Allows for the calculation of the annual or monthly payment to repay a
  loan

$$CRF = \frac {i(1+i)^n}{(1+i)^n-1}$$

## Monthly payments

If payments are monthly, we divide the annual percentage rate (APR) by
12 and multiply the number of years ($n$) by 12.

$$CRF = \frac {i(1+i/12)^{12n}}{(1+i/12)^{12n}-1}$$


## Exercise
- What is the annual payment for a $10K loan with an interest rate of 5%
  paid over a period of 7 years?

## Solution
![](../figures/capital_recovery_factor.jpg)

## Exercise
- What is the CRF for a 10 year loan at 0% interest?

## Solution
- 0.10 or 10%

## Cost of conserved energy
- Allows you to calculate the value of an investment as a per kWh cost
- This allows easy comparison with the current or plausible future cost
  of electricity



## CCE (Meier 1984)

$$ CCE = \frac{\textrm{Investment}}{\textrm{Annual Energy Savings}}
\cdot
\frac{d}{1-(1+d)^{-n}}
$$

## Interpreting the CCE
$$ CCE = \frac{\textrm{Investment}}{\textrm{Annual Energy Savings}}
\cdot
\frac{i}{1-(1+i)^{-n}}
\cdot
\frac{(1+i)^n}{(1+i)^n}
$$

$$ CCE = \frac{\textrm{Investment}}{\textrm{Annual Energy Savings}}
\cdot
\frac{i(1+i)^n}{(1+i)^n - 1}
$$

$$ CCE = \frac{\textrm{Investment}\cdot\textrm{CRF}}{\textrm{Annual Energy Savings}}
$$



## Cost of avoided carbon
- Allows you to calculate the value of an investment as the cost per
  amount of carbon not emitted
- Allows comparison with the current market price of carbon




<!--
## Activity
- Calculate cost of a loan (replicate class examples)
    - on spreadsheet
    - on a REPL
    - on paper
- Start spreadsheet calculation and cost flows
- Calculate conserved cost of electricity
- Calculate IRR of retrofit

## Monthly loan
- use PMT function and compare to manual CRF

-->


