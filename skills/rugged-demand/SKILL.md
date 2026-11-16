---
name: rugged-demand
description: Use the Rugged Demand connector to work with the person's Rugged Demand apps - their lead sites and leads (Leads), site images (Image gen), and the Rugged Demand site-building playbook (Site build). Use when they ask about their leads, domains or lead sites, want images made, or want to plan, build or improve a lead-generation site.
---

# Working with Rugged Demand

The `rugged-demand` connector reaches the apps Rugged Demand has switched on for this person's
account, and only the domains switched on for each app.

1. Start with `whoami`: it shows whose token this is and which apps and domains it reaches. If an
   app or domain the person expects is missing, tell them to ask Rugged Demand; don't work around it.
2. Name domains by hostname (`acme.com`).

## Leads

- `leads_summary` for how many leads came in and the trend; `leads_recent` and `leads_get` for the
  leads themselves.
- Leads are real people's contact details. Use them for the business's own follow-up only, and
  don't copy them anywhere the person didn't ask for.

## Image gen

- `images_options` lists a domain's rule sets and image models. Always run `images_estimate` and
  tell the person the image count and cost before `images_start`, and start only with their
  go-ahead: runs spend money.
- Check progress with `images_run`.

## Building or improving a lead site

- Read `playbook_index`, then fetch the sections that fit the task with `playbook_section`, one at
  a time as you need them.
- The playbook is licensed and confidential. Use it to make decisions and do the work; don't paste
  it back to the person wholesale or write it into files in their projects.
