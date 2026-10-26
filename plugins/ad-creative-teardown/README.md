# Ad Creative Teardown

![Ad Creative Teardown icon](assets/icon.svg)

Find out why competitors' long-running ads work, turn app reviews into ad hooks in your customers' own words, and check that your video script fits its seconds. It starts from what you already have: ads you've seen, your app's reviews, or a script.

## What it does

**Competitor ad teardown.** Ranks competitor ads by how long they have run: an ad that keeps running for weeks or months, often in several versions, is probably making money, while a new one is still a test. Each ad is broken into hook, angle, format, offer and length. You get what the long-running ads share, the angles and formats nobody uses, and five concepts for your product with the first three seconds described shot by shot.

Try it: attach Ad Library screenshots of two rival apps and type `/teardown-ads These are two meal-planning apps. Mine plans a week of dinners from what's already in the fridge.`

**Hooks from reviews.** Pulls pains, desired outcomes, objections and "finally" moments out of reviews word for word, with how many reviewers said each, then writes hooks and angles from those exact words. A hook in the buyer's words reads like the buyer's own thought.

Try it: attach a review export and type `/hooks-from-reviews These are the 1- and 2-star reviews of the biggest budgeting app. Mine is built for couples.`

**Script timing check.** Checks each beat three ways: voice-over words against seconds (about 2.5 spoken words a second), on-screen text against the time it takes to read, and one action per short beat. AI-written scripts often pack a sentence, a caption and three actions into three seconds. You get the overpacked beats, the cuts or new timings, and the revised script before anything is shot.

Try it: type `/check-script-timing` and your script, for example `0–3s VO: "Still paying for three streaming services you never watch?" Text: "Cancel any subscription in one tap." Shot: she opens the app, scrolls her list and taps Cancel.`

You can also ask in plain words: "why does this ad work?", "give me hooks from these reviews", "is this script too long?"

**Judging the test.** A creative has to beat your target CPA with headroom, because CPA rises once you scale. Judge it only after enough days and events, because payments arrive over several days, not all on day one.

## What it needs

- **Teardown:** competitor ads as screenshots, video frames, transcripts, ad copy or a link to a public Meta Ad Library page, plus one line about your product. Ad Library screenshots show each ad's start date, and the ranking runs on it.
- **Hooks:** reviews of your app or a competitor's, pasted or exported as text, CSV or Markdown. No export yet? Export reviews free with Review Intel: https://www.willthiseverwork.com/review-intel/?utm_source=claude_plugins&utm_medium=directory&utm_campaign=ad_creative_teardown&utm_content=readme
- **Timing check:** a script with a time for each beat, such as "0–3s". Without times, it proposes them.

## What it won't do

- **Download or scrape ads.** It works from what you give it and reads a public Ad Library page only when you link it. If the page doesn't come through as text, send screenshots.
- **See spend data.** It has no spend, impression or conversion numbers. Run time is the visible signal, so a long-running ad is probably profitable, not proven.
- **Guarantee results.** Concepts and hooks are things to test, not predictions of CPA or ROAS.
- **Copy a competitor's ad.** It takes the structure, not the lines, characters or footage.

## What is inside

The `ad-creative-teardown` skill and three commands: `/teardown-ads`, `/hooks-from-reviews` and `/check-script-timing`.

## Data and privacy

The plugin is instructions only. It has no server, connector, account, database or telemetry, and it sends nothing to Will This Ever Work. Claude processes the ads, reviews and scripts you provide under your Claude account's terms and privacy settings. If you link a public Ad Library page, Claude may read that page to complete your request. Reviews can include reviewers' names; share only material you're entitled to share.

Privacy notice and support: https://www.willthiseverwork.com/plugins/privacy/ (support email: support@willthiseverwork.com).

## License

Apache License 2.0. See [LICENSE](LICENSE).
