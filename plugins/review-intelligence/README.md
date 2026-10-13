# App Review Intel

![App Review Intel logo](assets/logo.svg)

See what people love, hate and wish worked differently in apps they already use, with the App Store and Google Play reviews behind it. Use it to decide what to build, improve, test or say. Every finding shows the reviews it came from; a pattern in reviews is a lead to check, not proof of demand.

## What it does

- Retrieve public app reviews
- Analyze review evidence
- Compare apps and review themes

Major findings carry stable review IDs and short verbatim quotes, and every evidence line names its denominator: percentages use the reviews actually analyzed, not the store's declared total. Inferences stay separate from what reviewers said, and any suggested language comes with a list of what not to claim.

## How to use it

Add the plugin, then open its Connectors tab on claude.ai or in Cowork and connect `review-intelligence`, the Review Intel server. The first time, it asks you to sign in with an email code: no password or API key. It's free during the launch. Claude Code connects to it directly. Then ask, for example:

- "Retrieve reviews from this App Store or Google Play URL and show me the first useful read."
- "Analyze this review export and find the strongest product, pricing, and ASO gaps."
- "Compare these competitor app URLs and identify an evidence-backed opportunity."

You can also paste or upload reviews, for example a Markdown export from https://www.willthiseverwork.com/review-intel/, and Claude analyzes them without calling the connector. Ask for "the full boring version" when you want the complete report.

## What is inside

- The `app-review-growth-analyzer` skill with the Review Intelligence v13 method: core rules, evidence protocol, conversation modes, the full report format and worked examples. The earlier v12 prompt is kept only as a regression baseline and is not used in normal analysis.
- A remote MCP connector: `https://www.willthiseverwork.com/review-intel/mcp`. Its one read-only tool, `retrieve_app_reviews`, returns up to 500 public written reviews per call with stable evidence IDs and explicit coverage counts. Google Play can continue across further batches with a cursor; Apple's public feeds have no equivalent.

## Data and privacy

The connector's sign-in uses OAuth with an email code. When Claude calls `retrieve_app_reviews`, the service keeps the account email address and a usage record for each call: the tool, app ID, store, country, number of reviews and time. It never stores review text. The service reads public review details (rating, date, app version, reviewer name and developer reply) from Apple's and Google's public sources and returns them to Claude. Usage records are kept for 13 months, then deleted or aggregated; account and plan records stay while the account exists. Vercel, network infrastructure and the upstream Apple or Google providers may keep ordinary request logs under their own policies. Reviews you paste or upload are analyzed in your Claude conversation and are not sent to the server. Public review text and reviewer names can still be personal data, so handle them under the rules that apply to your use.

- Privacy: https://www.willthiseverwork.com/review-intel/privacy/
- Support: https://www.willthiseverwork.com/review-intel/support/ (support@willthiseverwork.com)
- Terms: https://www.willthiseverwork.com/review-intel/terms/

## Limits

Reviews show patterns in the sample retrieved. They do not prove revenue, retention, conversion, causality or what every user thinks, and no public-source retrieval covers every review ever posted. Review Intel is not affiliated with or endorsed by Apple or Google.

## License

Apache License 2.0. See [LICENSE](LICENSE).
