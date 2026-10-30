# Metric definitions

- **Payer conversion:** share of all downloads that make a first payment within 35 days when comparing with the reviewed conversion reference.
- **First annual renewal:** the first renewal of an annual subscription. It is not a blended or later-cycle retention figure.
- **Cash payback:** the first month within the model's 24-month window where the modeled cash contribution remains at or above paid CAC.
- **Payer value:** expected contribution from one payer within the selected LTV window, after modeled refunds, store fees, and service costs.
- **Meta CPI:** spend per Meta-reported install with 7-day click plus 1-day view attribution. iOS installs are partly modeled. Adapty's Q3 2026 report covers July–September 2026; its platform CPI cuts pool sampled markets and app categories. Retrieve published values and ranges through `get_meta_ads_benchmarks` when available. Use them only as explicitly selected planning references, with provenance.
- **Meta CPM, link CTR and link CPC:** spend per 1,000 impressions, link clicks per impression, and spend per link click respectively. They do not establish install conversion or payer cost. Do not combine independently reported medians to reconstruct a funnel.
- **D7 cost per trial:** spend per Adapty trial started within seven days of install. It is not cost per payer.
- **D7 cost per payer:** spend per new payer within seven days of install. It does not include later converters or establish lifetime CAC. Do not substitute it for modeled paid CAC without matching the acquisition and conversion definitions.
- **D7 gross ROAS:** gross revenue in the seven days after install divided by ad spend. It excludes the model's deductions and cash-receipt timing; 100% does not establish net profit or cash payback.
- **Published percentiles:** P25–P75 is the middle half of the source distribution, not a forecast interval. For costs, a higher percentile means a higher cost. Percentages are passed as decimal fractions; 39% ROAS is `0.39`.
- **Separate source cuts:** Adapty's platform split (p. 17) and iOS-app cohort (p. 20) report different CPM values. Retain their original scope and page locators. Cost per payer and payer yield also do not consistently reconcile in the published tables; do not recalculate one from the other.
