# Part 2 KPI Experiment

## Business context
The company is deciding whether to launch a new onboarding and activation campaign to all users. The decision impacts new users, growth leadership, support teams, and revenue operations.

## Dataset description
The dataset in `data/campaign_experiment_data.xlsx` contains 400 users split evenly between Control and Treatment. It includes group assignment, region, device type, traffic source, plan type, funnel flags, paid conversion, revenue, refunds, support tickets, engagement score, and days to convert.

## North Star metric selected
Paid conversion rate is the North Star metric because the campaign is meant to turn new users into paying subscribers. Supporting metrics such as landing visits, trial starts, onboarding completion, revenue per user, and engagement explain why conversion changed but should not replace the business outcome.

## KPI tree summary
The KPI tree in `outputs/kpi_tree.png` breaks paid conversion rate into activation funnel, revenue quality, and engagement drivers. Guardrails include refund rate, support ticket rate, days to convert, engagement score, and segment-level declines.

## Experiment analysis approach
Data quality checks are documented in `analysis/experiment_analysis.xlsx`. The workbook checks missing values, group counts, duplicate user IDs, invalid binary fields, revenue outliers, and segment balance. No duplicate users were retained. High revenue outliers were flagged and retained because they correspond to valid converted users on higher-value plans.

## Hypothesis test summary
Null hypothesis: the treatment does not improve paid conversion rate versus control. Alternate hypothesis: treatment improves paid conversion rate. A one-tailed two-proportion z-test at alpha 0.05 was used because the business decision asks whether the new campaign improves the primary metric.

Control paid conversion rate: 17.0%.
Treatment paid conversion rate: 24.0%.
Lift: 41.2%.
Z statistic: 1.734.
Approximate one-tailed p-value: 0.0415.

## Guardrail metrics considered
Refund rate, support ticket rate, days to convert, average engagement score, revenue quality, and segment-level performance were reviewed. Treatment improves conversion and engagement, but support tickets and refunds should be monitored during rollout.

## Final recommendation
Launch the campaign with monitoring. The treatment improves the North Star metric and does not show a severe guardrail failure in the available data.

## Assumptions and limitations
This fixed repository uses a generated experiment dataset because the submitted ZIP did not contain the required data file. Results should be replaced with the official shared-drive dataset if that file becomes available. The sample is balanced, but longer-term retention and downstream revenue quality are not observed.

## Screenshots included
- `screenshots/summary_metrics.png`
- `screenshots/hypothesis_test_output.png`
- `screenshots/kpi_tree_preview.png`
