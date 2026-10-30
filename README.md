# Fix It First

A self-serve troubleshooting tool for INHA bookkeepers to work through before filing a Tight/Hurdlr tech ticket. About 31% of tech tickets turn out not to be tech issues at all (per the Tech Ops Hub tracking); this walks a bookkeeper through branching yes/no questions sourced from real Slack threads and Judy Gingerich's Confluence SOP, resolving on the spot wherever possible and only routing to a ticket when nothing fits.

No build step, no backend — a single static `index.html` (vanilla JS, no framework). Hosted on GitHub Pages because the team does not have individual Claude accounts, so this previously lived as a private Claude Artifact that no bookkeeper could actually open.

**Live:** https://karenherring-hcp.github.io/fix-it-first/

## How it ends

The tool never auto-files a ticket — there's no backend and no Slack API access from a static page. The final screen pre-fills the ticket description (issue type + everything already checked) with a copy-to-clipboard button, and links directly to the `#inha_mgmt_workflow` Slack channel. The bookkeeper still has to run the existing `INHA Technical Issue–Tech Support Ticket` shortcut themselves and paste in the text — that workflow has no link trigger, so there's no way to jump straight into it from outside Slack.

## Maintenance

New facts/corrections get folded into `CATS` / `FASTTRACK` in `index.html` directly — no CMS, no database. Judy's "Check Here First" Confluence page (linked in the footer) is the authoritative source when the two disagree.
