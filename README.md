# Launchdog agent plugin

Launch your product on Launchdog, the weekly launch board, from your coding agent: it drafts the listing from your site, books a free or paid week and adds the badge.

[Launchdog](https://launchdog.dev) is a weekly product-launch board whose makers manage their listings through an MCP server. This plugin connects your coding agent to it and teaches it the launch flow, for Claude Code, Codex and Cursor.

## What it adds

- **The `launchdog` MCP server** at `https://launchdog.dev/mcp` (remote, streamable HTTP). You sign in with OAuth in your browser the first time your agent uses it; there are no API keys, and nothing is stored in this plugin.
- **The `launch` skill**: the step-by-step flow from a draft listing to a booked launch week. Your agent drafts the listing from your live site, shows it to you before saving, lets you pick a free or paid week, and for a free launch adds the Launchdog badge to your home page with your OK to commit.

## What it sends and runs

The plugin runs nothing on your machine: no scripts, hooks or packages. Your agent calls the Launchdog MCP server, which reads your public home page to draft the listing and to check the badge. Paid launches return a Stripe Checkout link for you to open: the agent never pays. See the [privacy policy](https://launchdog.dev/privacy-policy) and [terms](https://launchdog.dev/terms-and-conditions).

## Install

- Claude Code: `claude plugin marketplace add DevStarks/launchdog-agent-plugin`, then `claude plugin install launchdog@launchdog`.
- Codex: `codex plugin marketplace add DevStarks/launchdog-agent-plugin`, then install Launchdog from `/plugins`.
- Cursor: install Launchdog from the Cursor Marketplace.

Then ask your agent to "launch this product on Launchdog". If you added the server by hand before (`claude mcp add launchdog …`), remove that copy so the tools aren't listed twice.

## More

The tools, their errors and fixes are documented at [https://launchdog.dev/docs/mcp](https://launchdog.dev/docs/mcp). Questions: support@launchdog.dev.

This folder is generated from the Launchdog app; changes made here are overwritten.
