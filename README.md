# SDG 12: Responsible Consumption and Production — GLP 2026

**Your challenge:** How might we help a household reduce waste and make smarter choices about what members buy, use, and throw away?

**Your region is open.** Los Angeles, South Korea, or any other part of the
world. Research two before you commit to one.

## Start here

This repo is nearly empty on purpose. Paste this into Claude Code. It will
interview you first, then build the wiki around your answers:

> We're the **SDG 12 (Responsible Consumption and Production)** team. Our challenge: *"How might we help a household reduce waste and make smarter choices about what members buy, use, and throw away?"* We can
> focus on Los Angeles, South Korea, or any other part of the world.
>
> Read this gist and set up this repo as an LLM wiki for that challenge:
> https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f — but before you build anything, interview us for context. Ask one
> question at a time, give us multiple-choice options, and keep going until you
> know enough about our challenge, our candidate regions, and what we need to
> research.

## Finding sources

Ask Claude to search the web and read pages for you:

> Find three sources on our problem in the regions we are considering. For each
> one, create a markdown file in sources/ with the page title, the URL, today's
> date, the key facts and figures with short direct quotes, and a two-sentence
> summary. Then ingest them into the wiki.

Watch the list of actions Claude takes while it works. That list is where your
citations come from.

Write down the numbers that matter and quote them exactly. Don't copy whole
articles into the repo — a judge wants the figure and the source, not the page.

## Saving your work

You do not type git commands. While you work, ask:

> Commit our work with a note about what we did, and push it.

Claude saves to your team's **draft branch** and shows you each command it ran.

## Publishing at the end of a session

Your work isn't on `main` until you publish it. Two clicks, once per session:

1. Open the diff view (the `+42 -18` indicator at the top of the session)
2. **Create PR**, then **Merge**

Think of it as: Claude drafts, your team reviews, then you publish.

## One driver at a time

One person per team drives Claude in a session; everyone else watches the
screen and decides together. Two people running separate sessions on this repo
creates two draft branches that fight each other. Swap drivers whenever you
like — just not at the same time.
