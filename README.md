# Rugged Demand for Claude

Lets Claude in VS Code (Claude Code) work with your Rugged Demand apps: your lead sites and leads,
site images, and the Rugged Demand site-building playbook. What it can reach is set by Rugged
Demand for your account.

## Set up

1. **Make a token.** Sign in at https://my.ruggeddemand.ai, open **Apps** and choose **New token**.
   Copy it; it's shown once.
2. **Give your computer access to this repository** (it's private). Send Rugged Demand your GitHub
   username and accept the invitation GitHub emails you. Then, with the GitHub CLI:
   `gh auth login`, then `gh auth setup-git`.
3. **Install Claude for the terminal.** The Claude panel in VS Code can't install plugins: typing
   `/plugin` there says "/plugin isn't available in this environment". In VS Code open
   **Terminal → New Terminal** and run the line for your computer, then reopen VS Code:

   ```text
   Mac:      curl -fsSL https://claude.ai/install.sh | bash
   Windows:  irm https://claude.ai/install.ps1 | iex
   ```

4. **Install the plugin.** In a new terminal, type `claude` (sign in with your Claude account if
   asked), then:

   ```text
   /plugin marketplace add ruggeddemand/rugged-demand-plugin
   /plugin install rugged-demand@rugged-demand
   ```

   When asked, paste your token. Claude Code keeps it in your system's secure store. Type `/exit`
   and reopen VS Code; the plugin now works in the Claude panel too.
5. **Check it works:** in the Claude panel, ask "What can you reach in Rugged Demand?"

## Updates

Run `claude` in the terminal, then turn on auto-update in `/plugin` → Marketplaces → rugged-demand,
or run `/plugin marketplace update rugged-demand` now and then.

## If something stops working

- "This token no longer works": make a new token in the portal, then run `claude` in the terminal
  and update it in `/plugin`.
- "/plugin isn't available in this environment": you're in the Claude panel. Run `claude` in the
  terminal and type it there (step 4).
- An app or domain is missing: ask Rugged Demand; access is set per account.
