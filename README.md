# The Founding Reader

Search the Declaration, Articles of Confederation, Constitution and Bill of Rights, all 85 Federalist essays, the major Anti-Federalist writings and three founding-era antislavery documents. Retrieve exact passages and whole documents with attribution, dates and reading links, open fifteen curated Federalist-versus-Anti-Federalist debates, and trace which writers answered which. Search results are candidates for your assistant to evaluate; the tools quote only the collection's text and never invent passages, authorship or replies.

This plugin bundles one remote MCP connector and one skill. The connector points to `https://foundingreader.com/mcp`, a public, read-only, no-authentication endpoint operated by Gerald Norby. It exposes four read-only tools: `search_founding_passages` finds candidate paragraphs by keyword across all 136 documents; `get_founding_source` retrieves exact text by document, paragraph or reference such as 'Federalist 78' or 'Article III, Section 1', with context and whole-document pagination; `get_founding_debate` opens one of fifteen curated debates with each side's exact excerpts; and `get_founding_connections` finds documented replies and curated links for a writer, document, paragraph or constitutional clause. The skill tells Claude when to use those tools and how to quote, attribute and paginate their results.

## What the plugin sends and receives

When Claude calls a tool, it sends the endpoint short search terms, a document or provision reference, optional collection, author or document filters, and pagination or context settings. The endpoint returns public-domain source text, editorial notes and metadata. It makes no calls to an AI provider, requires no account, and does not write tool inputs or results to an application log or database. Leave personal details out of queries. The plugin contains no executable code, hooks or local servers.

Privacy policy: https://foundingreader.com/plugin/privacy
Terms: https://foundingreader.com/plugin/terms
Support: https://norbonics.com/support (norbonics@outlook.com)

## Install

In Claude Code:

```
claude plugin marketplace add DlaregY/the-founding-reader-claude-plugin
claude plugin install the-founding-reader@founding-reader
```

In Claude chat or Cowork, upload the release ZIP under Customize > Plugins > Upload plugin.

## Try it

- Where do the Federalist Papers discuss the dangers of faction? Quote the key passage.
- Did Brutus respond directly to anything Hamilton wrote? Show the evidence.
- Show me the full text of Federalist 10.

Search results are candidates, not verified answers. A missing result means the passage is not in this collection, never that a founder did not write it.
