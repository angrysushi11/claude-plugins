# Article Interview

![Article Interview icon](assets/icon.svg)

Turn something you did, decided or learned into an article. Claude interviews you one question at a time, or works from notes and voice-note transcripts you paste, shows you two or three possible angles, then drafts the piece from your answers in your own words.

**Try it:** type `/interview-me` followed by a topic, or nothing at all. For example: `/interview-me I replaced our weekly status meeting with written updates. There might be a LinkedIn article in it.`

## What it does

- Asks one short question per turn, built on your last answer, so you talk instead of filling in a form
- Uses what you've already said, so you don't repeat yourself
- Finds what makes the piece yours: what happened, what you decided, what changed, and the numbers you actually have
- Shows two or three angles before writing, each tied to a reader's question and an example you already gave
- Drafts in your words, then lists what came from you, what it added, and any open gaps

Gaps in the draft are marked `[TK: question]` instead of being filled with invented detail. Each comes with a fallback: cut the passage, or keep the plain version.

## What it needs

A topic, a rough idea, notes, a voice-note transcript or an existing draft. Or nothing: if you don't know what to write about, it starts from something you recently noticed, built or changed your mind about. Works for LinkedIn articles and posts, blog posts, newsletters and essays. No account or connector.

## What it won't do

It won't invent experiences, scenes, quotes, emotions or numbers, or push your story toward a success-story angle because it sounds more publishable. It doesn't publish, post or contact anyone. It can't write from nothing: the substance has to come from you.

## Data and privacy

The plugin is instructions only. It has no server, connector, account, database or telemetry, and it sends nothing to Will This Ever Work. Claude processes the notes, transcripts, drafts and answers you provide under your Claude account's terms and privacy settings. Stories often involve other people or confidential work: the plugin keeps those out of the draft unless you clear them, and you should share only what you're entitled to share.

Privacy notice and support: https://www.willthiseverwork.com/plugins/privacy/ (support email: support@willthiseverwork.com).

## What is inside

The `article-interview` skill, the `/interview-me` command, and two reference files: interview moves (which question recovers what) and drafting (structure, voice, gaps, and a fictional before-and-after).

## License

Apache License 2.0. See [LICENSE](LICENSE).
