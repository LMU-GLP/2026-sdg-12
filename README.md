# SDG 12: Responsible Consumption and Production — GLP 2026

**Your challenge:** How might we help a household reduce waste and make smarter choices about what members buy, use, and throw away?

**Your region is open.** Los Angeles, South Korea, or any other part of the
world. Research two before you commit to one.

Every prompt you need today is on this page, in order. Each one has a copy
button in its top-right corner, so you never have to select text by hand.

## 1. Start together

One person drives. The whole team answers out loud. This runs once — it decides
your angle and builds the structure everyone else works inside.

```
We're the SDG 12 (Responsible Consumption and Production) team. Our challenge:
"How might we help a household reduce waste and make smarter choices about
what members buy, use, and throw away?" We can focus on Los Angeles, South
Korea, or any other part of the world.

Read this gist and set up this repo as an LLM wiki for that challenge:
https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f
But before you build anything, interview us for context. Ask one question at a
time, give us multiple-choice options, and keep going until you know enough
about our challenge, our candidate regions, and what we need to research.
```

## 2. Split up — one source each

Now everyone runs their own session. Claim a different source from the list,
and swap `[your source]` and `[your region]` for what you picked.

```
Find a source on [your source] in [your region]. Create a markdown file in
sources/ with the page title, the URL, today's date, the key facts and figures
with short direct quotes, and a two-sentence summary. Don't edit index.md or
the wiki pages yet.
```

Claim one each:

- UN targets for your goal: `sdgs.un.org/goals/goal12`
- One dataset (UN Stats, World Bank, or a local source)
- A news story about the problem in your first region
- A news story about the problem in your second region
- One product or program already trying to solve this

Watch the actions Claude takes. That list is where your citations come from.
Write down the numbers that matter and quote them exactly. Don't copy whole
articles into the repo. A judge wants the figure and the source, not the page.

## 3. Save your work

You never type git commands. Ask:

```
Commit our work with a note about what we did, and push it.
```

Claude saves to your own draft branch and shows you each command it ran.

## 4. Merge, so your work counts

Your work isn't on `main` until you publish it. Open the diff view (the
`+42 -18` indicator at the top of your session), select **Create PR**, then
**Merge**.

If GitHub says there's a conflict, that's normal when several people work at
once. Ask:

```
Merge main into our branch and resolve the conflicts.
```

## 5. Finish together

One person drives again. Everyone watches the pages connect to each other.

```
Ingest everything in sources/ and update the wiki.
```

## 6. Ask your wiki a hard question

Make it a question you genuinely don't know the answer to.

```
Between our two candidate regions, where is this problem worse, and for whom?
Cite your sources, and save the answer as a page in wiki/.
```

That cited answer is the start of your idea, and it's what you'll defend on
Monday when a judge asks where your data came from.

## If you finish early

```
Find contradictions and gaps in our wiki, and tell us what we're missing.
```

## How the team works

**Start together, split up, then finish together.** The interview in step 1 and
the synthesis in step 5 run once, with one driver. Everything in between is
parallel: each of you gets your own draft branch, which is what lets four
people work at the same time without overwriting each other.

Merge the PRs one at a time when you regroup.

## Before you leave

- Your work is **merged to `main`** — check on GitHub, not in Claude
- A problem statement with at least two citations
- A region you can defend out loud

