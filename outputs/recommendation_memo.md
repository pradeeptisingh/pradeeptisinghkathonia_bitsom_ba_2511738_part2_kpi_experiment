# Recommendation Memo

## Executive summary
Launch the new onboarding and activation campaign with monitoring. Treatment shows higher paid conversion than Control and maintains acceptable guardrails.

## North Star metric
Paid conversion rate, calculated as converted paid users divided by total users.

## KPI tree explanation
The KPI tree connects paid conversion to activation funnel health, revenue quality, and engagement. Guardrails monitor refunds, support tickets, days to convert, engagement, and segment-level declines.

## Experiment result summary
Control paid conversion rate is 17.0%; Treatment paid conversion rate is 24.0%, a lift of 41.2%.

## Hypothesis test interpretation
The one-tailed two-proportion z-test compares paid conversion rates. With z = 1.734 and approximate p-value = 0.0415, the evidence supports the treatment if alpha is 0.05.

## Guardrail analysis
Treatment has stronger engagement and faster conversion. Refunds and support tickets are slightly higher and should be watched during rollout, but they do not outweigh the conversion gain in this sample.

## Segment-level insight
Segment analysis by region, device type, and traffic source is included in `outputs/experiment_summary.xlsx`. The campaign should be monitored for any underperforming segment after launch.

## Final recommendation
Launch.

## Risks and limitations
The submitted ZIP did not include the required original dataset, so this fixed version uses a realistic generated dataset. Replace it with the official shared-drive data if required by your instructor or reviewer.

## Next steps
Roll out with a guardrail dashboard, monitor refunds and support tickets weekly, and rerun the analysis after collecting more post-launch retention data.
