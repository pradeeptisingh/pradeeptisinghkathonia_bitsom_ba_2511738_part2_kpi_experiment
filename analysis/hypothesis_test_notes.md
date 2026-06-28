# Hypothesis Test Notes

## Hypotheses
Null hypothesis: the treatment paid conversion rate is less than or equal to the control paid conversion rate.

Alternate hypothesis: the treatment paid conversion rate is greater than the control paid conversion rate.

## Test design
The test is one-tailed because the business decision is whether the new campaign improves the selected North Star metric. The significance level is 0.05.

## Metric being tested
Paid conversion rate, calculated as converted paid users divided by total users.

## Reason for choosing the metric
Paid conversion rate directly connects onboarding success to subscription growth. Other metrics are supporting diagnostics or guardrails.

## Inputs and output
Control paid conversion rate: 17.0%.

Treatment paid conversion rate: 24.0%.

Z statistic: 1.734.

Approximate one-tailed p-value: 0.0415.

## Decision rule
If p-value is less than 0.05, reject the null hypothesis. Otherwise, fail to reject the null.

## Business interpretation
The treatment shows evidence of a meaningful improvement in paid conversion. The recommendation is to launch while monitoring guardrails.
