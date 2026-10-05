# Will This Ever Work plugins for Claude

Five Claude plugins by Dasha Antonova (DoubleDash). Each folder under `plugins/` is a separate plugin with its own README, license and manifest at `.claude-plugin/plugin.json`.

| Plugin | Name | Version | What it does |
| --- | --- | --- | --- |
| [ASO Keyword Intent](plugins/aso-keyword-intent) | `aso-keyword-intent` | 0.1.1 | Classify raw keyword phrases for App Store metadata or SEO content planning without rewriting the original queries. |
| [Job Interview Story Coach](plugins/interview-story-coach) | `interview-story-coach` | 0.1.2 | Build truthful interview stories from a job description and practise role-specific interviews. |
| [Make My Product Clear](plugins/make-my-product-clear) | `make-my-product-clear` | 0.1.2 | Rewrite existing product pages, app listings, and product descriptions so customers see why the product matters and what to do next. |
| [App Growth Calculator](plugins/app-growth-calculator) | `app-growth-calculator` | 0.1.1 | Test whether a subscription app's paid growth pays back, what input must improve, and whether cash can cover the wait. |
| [Review Intelligence](plugins/review-intelligence) | `review-intelligence` | 0.3.3 | Analyze public app reviews to see what people love, hate, and wish worked differently before deciding what to build, improve, test, or say. |

App Growth Calculator and Review Intelligence each include a remote MCP connector hosted at willthiseverwork.com. The other three are instructions-only skills that send nothing to an external service.

## Install in Claude Code

```
claude plugin marketplace add angrysushi11/claude-plugins
claude plugin install review-intelligence@doubledash
```

Support: support@willthiseverwork.com
