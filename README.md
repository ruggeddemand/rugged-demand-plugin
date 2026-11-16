# Rugged Demand for Claude

Lets Claude in VS Code (Claude Code) work with your Rugged Demand apps: your lead sites and leads,
site images, and the Rugged Demand site-building playbook. What it can reach is set by Rugged
Demand for your account.

## Set up

1. **Make a token.** Sign in at https://my.ruggeddemand.ai, open **Apps** and choose **New token**.
   Copy it; it's shown once.
2. **Give your computer access to this repository** (it's private). With the GitHub CLI:
   `gh auth login`, then `gh auth setup-git`.
3. **Install the plugin** in Claude Code:

   ```text
   /plugin marketplace add ruggeddemand/rugged-demand-plugin
   /plugin install rugged-demand@rugged-demand
   ```

   When asked, paste your token. Claude Code keeps it in your system's secure store.
4. **Check it works:** ask Claude "What can you reach in Rugged Demand?"

## Updates

Turn on auto-update in `/plugin` → Marketplaces → rugged-demand, or run
`/plugin marketplace update rugged-demand` now and then.

## If something stops working

- "This token no longer works": make a new token in the portal and update it in `/plugin`.
- An app or domain is missing: ask Rugged Demand; access is set per account.
