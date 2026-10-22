# The Founding Reader

Search the Declaration, Articles of Confederation, Constitution and Bill of Rights, all 85 Federalist essays, the major Anti-Federalist writings and three founding-era antislavery documents. Retrieve exact passages and whole documents with attribution, dates and reading links, open fifteen curated Federalist-versus-Anti-Federalist debates, trace which writers answered which, and check whether a quotation really appears in these documents and under whose name. Search results are candidates for your assistant to evaluate; the tools quote only the collection's text and never invent passages, authorship or replies. A quote missing from the collection is reported as not found here, never as fake.

This plugin bundles one remote MCP connector and one skill. The connector points to `https://foundingreader.com/mcp`, a public, read-only, no-authentication endpoint operated by Gerald Norby. It exposes five read-only tools: `search_founding_passages` finds candidate paragraphs by keyword across all 136 documents; `get_founding_source` retrieves exact text by document, paragraph or reference such as 'Federalist 78' or 'Article III, Section 1', with context and whole-document pagination; `get_founding_debate` opens one of fifteen curated debates with each side's exact excerpts; `get_founding_connections` finds documented replies and curated links for a writer, document, paragraph or constitutional clause; and `verify_founding_quote` checks up to ten claimed quotations against the 136 documents and returns the real source wording, differences and an attribution check that preserves disputed-authorship notes. The skill tells Claude when to use those tools and how to quote, attribute and paginate their results.

## What the plugin sends and receives

When Claude calls a tool, it sends the endpoint short search terms, a document or provision reference, optional collection, author or document filters, pagination or context settings, and, for quote checks, the quotation text with any claimed author or source. The endpoint returns public-domain source text, editorial notes and metadata. It makes no calls to an AI provider, requires no account, and does not write tool inputs or results to an application log or database. Leave personal details out of queries. The plugin contains no executable code, hooks or local servers.

Privacy policy: https://foundingreader.com/plugin/privacy
Terms: https://foundingreader.com/plugin/terms
Support: https://norbonics.com/support (support@norbonics.com)

## Install

Install [The Founding Reader from Claude's plugin directory](https://claude.ai/customize/plugins/id/30172d21-46a0-46f0-8c94-6dbf8f9a712c%40anthropic-plugin-directory).

In Claude Code:

```
claude plugin marketplace add DlaregY/the-founding-reader-claude-plugin
claude plugin install the-founding-reader@founding-reader
```

## Try it

- Where do the Federalist Papers discuss the dangers of faction? Quote the key passage.
- Did Brutus respond directly to anything Hamilton wrote? Show the evidence.
- Is 'Government is not reason, it is force' a real Washington quote?

Search results are candidates, not verified answers. A missing result means the passage is not in this collection, never that a founder did not write it.
