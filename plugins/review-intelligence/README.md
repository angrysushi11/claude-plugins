# Review Intelligence

![Review Intelligence logo](assets/logo.svg)

Analyze public App Store and Google Play reviews for recurring product friction, unmet needs, customer language, pricing, growth, and ASO opportunities. Review evidence and coverage stay visible; findings do not establish demand, revenue, or causality.

## What it does

- Retrieve public app reviews
- Analyze review evidence
- Compare apps and review themes

Major findings carry stable review IDs and short verbatim quotes, and every evidence line names its denominator: percentages use the reviews actually analyzed, not the store's declared total. Inferences stay separate from what reviewers said, and any suggested language comes with a list of what not to claim.

## How to use it

Add the plugin, then open its Connectors tab on claude.ai or in Cowork and connect `review-intelligence`, the Review Intel server. No account, API key or sign-in is needed. Claude Code connects to it directly. Then ask, for example:

- "Retrieve reviews from this App Store or Google Play URL and show me the first useful read."
- "Analyze this review export and find the strongest product, pricing, and ASO gaps."
- "Compare these competitor app URLs and identify an evidence-backed opportunity."

You can also paste or upload reviews, for example a Markdown export from https://www.willthiseverwork.com/review-intel/, and Claude analyzes them without calling the connector. Ask for "the full boring version" when you want the complete report.

## What is inside

- The `app-review-growth-analyzer` skill with the Review Intelligence v13 method: core rules, evidence protocol, conversation modes, the full report format and worked examples. The earlier v12 prompt is kept only as a regression baseline and is not used in normal analysis.
- A remote MCP connector: `https://www.willthiseverwork.com/review-intel/mcp`. Its one read-only tool, `retrieve_app_reviews`, returns up to 500 public written reviews per call with stable evidence IDs and explicit coverage counts. Google Play can continue across further batches with a cursor; Apple's public feeds have no equivalent.

The retriever and MCP server are open source at https://github.com/angrysushi11/review-intelligence.

## Data and privacy

When Claude calls `retrieve_app_reviews`, the server receives the store URL or app ID, the market, sort order and number of reviews requested and, on Google Play, the continuation cursor. It reads public review text and public review details (rating, date, app version, reviewer name and developer reply) from Apple's and Google's public sources and returns them to Claude. It does not log in to either store, does not need OAuth, and has no review database. Vercel, network infrastructure and the upstream Apple or Google providers may keep ordinary request logs under their own policies. Reviews you paste or upload are analyzed in your Claude conversation and are not sent to the server. Public review text and reviewer names can still be personal data, so handle them under the rules that apply to your use.

- Privacy: https://www.willthiseverwork.com/review-intel/privacy/
- Support: https://www.willthiseverwork.com/review-intel/support/ (support@willthiseverwork.com)
- Terms: https://www.willthiseverwork.com/review-intel/terms/

## Limits

Reviews show patterns in the sample retrieved. They do not prove revenue, retention, conversion, causality or what every user thinks, and no public-source retrieval covers every review ever posted. Review Intel and Review Intelligence are not affiliated with or endorsed by Apple or Google.

## License

Apache License 2.0. See [LICENSE](LICENSE).
