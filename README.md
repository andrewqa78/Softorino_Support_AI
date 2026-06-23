# Softorino Support AI

A knowledge base for automating Softorino customer support responses.

## What this is

This repo contains structured support knowledge used by an AI agent to handle incoming tickets. The agent reads relevant KB files, identifies the issue, and either resolves it or escalates to a human agent.

## Structure

```
knowledge_base/
├── global_rules.md          # Support rules, escalation guidelines, reply templates
├── activation_and_license.md
├── waltr_pro.md
├── syc_pro.md
├── alttunes.md
├── iringg.md
├── other_products.md        # Beamer, Folder Colorizer, PicFindr, CleanAppsNow, etc.
├── Softorino_Billing_and_Payments.md
└── Softorino_Products.md
```

Each file contains troubleshooting cases in a standard format: symptoms, common phrases, questions to ask, root cause candidates, resolution steps, escalation triggers, and internal notes.

## How the AI agent uses this

See [SUPPORT_PROMPT.md](SUPPORT_PROMPT.md) for the full instructions given to the agent on how to read and update this knowledge base.

## Updating the KB

When a new ticket reveals a new issue or a better resolution:

```bash
git add knowledge_base/
git commit -m "short description of what changed"
git push
```
