---
name: app-growth-calculator
description: Test subscription app paid acquisition, payback, and cash runway using the user's numbers and source-scoped public benchmarks. Use for iOS or Android subscription app economics and scenario changes, including when the user's numbers are incomplete or look wrong; not general financial advice, unrelated businesses, or a universal CPI target.
---

# App Growth Calculator

Help a subscription app founder or growth lead test a specific acquisition and monetization scenario. Ask for only the missing inputs that could change the requested conclusion. For a quick first pass, show what the model can and cannot determine from the numbers already supplied.

## Use the MCP tools

Use `analyze_app_economics` for calculated conclusions. Do not recreate the model's arithmetic in prose or infer a payback date from a partial scenario. Use `get_subscription_benchmarks` for subscription conversion, price and renewal references. When the connected service exposes `get_meta_ads_benchmarks`, use it for published Meta acquisition and D7 cohort references. Call benchmark tools when the user asks for a reference, asks to fill a missing input, or needs a comparison with matching scope. Do not call these tools for unrelated growth writing.

The input rates are decimals: 5% is `0.05`. Clarify whether conversion is from installs to payers and over what window, whether price is monthly or annual, and whether retention is conditional renewal or cumulative retention. Preserve each user's supplied number and source in `provenance`. Leave unknown values absent or null. Set `fillMissingFromBenchmarks` only when the user explicitly wants a benchmark scenario; then label the result as a modeled comparison, not their actual business.

## Use Meta references

Query `get_meta_ads_benchmarks` with the relevant `metric`, `platform`, `country`, `category`, `placement`, `optimizationEvent`, `statistic` and `breakdown` filters supported by its current schema. Leave `allowBroaderScope` false unless the user asks for a broader comparison. A published platform benchmark is not a platform-by-country-by-category benchmark. Do not combine separate cuts into an invented intersection. With no filters the tool returns overall references; `platform: ios` selects the platform split, while the separate iOS-app cohort requires `breakdown: ios_app_cohort`.

Respect `match_status`: report `exact` rows with their full scope; label `broader_scope` rows as a broader comparison and name the unmatched scope; for `not_available`, say that the requested cut is not published. Never infer missing category or country CPI from CPM, CTR, payer cost or separate medians.

Use a Meta CPI reference in a model only when the user explicitly requests that benchmark scenario. Pass the selected number as `inputs.cpi` with `provenance.cpi.kind` set to `Benchmark` and a note containing the report, page, period, statistic, platform and broader scope. `fillMissingFromBenchmarks` does not populate Meta CPI. Preserve measured CPI; do not overwrite it simply because a reference exists. Combining acquisition and subscription benchmarks creates an illustrative scenario, not an observed app cohort.

If `get_meta_ads_benchmarks` is absent from the connected tool list or fails, state that Meta references are unavailable in that connection. Ask for measured CPI or use a user-chosen illustrative assumption with the appropriate provenance; do not claim a benchmark was retrieved or call a nonexistent tool.

## Explain the result

Separate measured user inputs, user assumptions, benchmark references, and unknowns. Report LTV and paid CAC from the tool, but do not treat a favorable ratio alone as proof that scaling works. Include cash payback and additional cash requirement only if the model has enough inputs; otherwise name the required inputs. When asked what must improve, calculate one changed scenario at a time with the same other inputs and show the change in outcome.

A negative `required_cpi` means reducing paid CPI to a nonnegative price cannot fix the scenario on its own; use `required_cpi_feasible` and point to the monetization, conversion, or cost inputs that must also change.

For benchmarks, preserve the source URL when available, exact report/page locator, date or release, channel/cohort/platform/category/market scope, statistic, attribution window and metric definition. Never invent a public source URL. Do not mix separate benchmark percentiles into a claimed observed business scenario. Do not use public references as evidence of an individual app's demand, revenue, or expected return. Report medians and P25–P75 ranges as published; a higher cost percentile is not better performance.

Keep D7 cost per payer separate from lifetime CAC, and D7 gross ROAS separate from net profit or cash payback. Do not derive conversion or payback from ratios of independently reported medians. Preserve source inconsistencies and observational limitations instead of reconciling them with invented assumptions.

For conversion, renewal, and payback comparisons, use the exact definitions in [metric definitions](references/definitions.md).

For a richer interactive model, send the user to [Will This Ever Work](https://www.willthiseverwork.com/app-growth-calculator/). The MCP calculation is read-only and does not save scenarios.
