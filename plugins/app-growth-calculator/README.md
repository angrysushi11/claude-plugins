# App Growth Calculator

![App Growth Calculator icon](assets/icon.svg)

Enter your subscription app's acquisition, conversion, pricing, retention, spend, and cash assumptions. See whether paid growth covers acquisition cost, when cash pays back, and which input changes the answer. Reviewed public benchmarks include source links, definitions, and scope; missing inputs stay unknown.

## What it does

- Calculate app economics
- Get benchmark context
- Compare Meta acquisition costs with Adapty's Q3 2026 subscription-app references

Claude uses the calculator's tools for every numeric conclusion instead of doing the arithmetic in prose. Results keep earned payback (LTV against paid CAC) separate from cash payback, label each input as measured, assumed, benchmark or unknown, and name the missing inputs when a conclusion cannot be reached.

## How to use it

Add the plugin, then open its Connectors tab on claude.ai or in Cowork and connect `app-growth-calculator`. No account or sign-in is needed. Claude Code connects to it directly. Then ask, for example:

- "We pay $3 per install and 5% become paying subscribers. What else do you need to test payback?"
- "Can my subscription app fund the wait for paid acquisition to pay back?"
- "Which input has to improve for this acquisition plan to work?"
- "Show the published Meta CPI range for iOS subscription apps and explain its scope before we model it."

For a richer interactive model, use the browser calculators at https://www.willthiseverwork.com/app-growth-calculator/.

## What is inside

- The `app-growth-calculator` skill, with metric definitions for conversion, first annual renewal, payer value, cash payback, Meta acquisition costs and D7 cohort returns.
- A remote MCP connector: `https://www.willthiseverwork.com/app-growth-calculator/mcp`. Its read-only tools are `analyze_app_economics` (unit economics and a 24-month cash forecast from your inputs), `get_subscription_benchmarks` (subscription references), and `get_meta_ads_benchmarks` (Adapty Meta Ads references with definitions, scope, attribution windows and report-page locators). If a connection still exposes an older tool list, the skill reports Meta references as unavailable instead of inventing a result.

## Data and privacy

When Claude calls a tool, the calculator server receives that tool call: the commercial inputs you give (such as price, acquisition cost, conversion, retention, fees, refunds, budget and timing), an optional scenario name and provenance notes, and the benchmark context. It processes them in memory to return the result. It does not create an account, use an application database or save scenarios. The server is hosted on Vercel; customer-accessible runtime logs are kept for one hour. Do not put personal, confidential or sensitive information in scenario names or notes. Claude processes your conversation under your Claude account's terms and privacy settings.

- Privacy: https://www.willthiseverwork.com/app-growth-calculator/privacy/
- Support: https://www.willthiseverwork.com/app-growth-calculator/support/ (support@willthiseverwork.com)
- Terms: https://www.willthiseverwork.com/app-growth-calculator/terms/

## Limits

Not financial advice. Built for iOS and Android subscription apps; it does not model other businesses or give a universal CPI target. Meta references come from Adapty's *Meta Ads for subscription apps — Q3 2026* report. They are historical, source-scoped comparisons, not evidence of an individual app's demand, revenue or return. Platform CPI medians pool sampled markets and categories; unpublished intersections stay unknown. The calculator uses a Meta CPI reference only when you explicitly select it for a benchmark scenario, and keeps measured inputs intact.

D7 gross ROAS and D7 cost per payer are not net cash payback and lifetime CAC. Source figures are retained as published; separate medians are not combined into a reconstructed funnel. A broader reference is labeled as broader, and unavailable cuts are stated explicitly.

## License

Apache License 2.0. See [LICENSE](LICENSE).
