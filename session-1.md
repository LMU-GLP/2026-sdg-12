# Session 1: build the research wiki

Wednesday. You're turning your challenge into evidence: real sources, real
figures, and a problem statement your team can defend out loud.

[Back to the front page](README.md) · [Session 2](session-2.md)

## Open it

1. Go to **[claude.ai/code](https://claude.ai/code)** and sign in with your Claude account
2. If this is your first time, you'll see one button: **Connect to GitHub**. Click it
   and authorize. When GitHub asks which organizations Claude can reach, include
   **LMU-GLP**
3. Above the message box you should see **Full network access**. If you do, you're
   set. If you see anything else, click it and choose **Full network access**. Claude
   can't read a single web page without it, and it fails quietly
4. Click **+ Select repo...** and choose **LMU-GLP/2026-sdg-12**
5. Not in the list? You haven't accepted your GitHub invitation. Open
   [github.com/notifications](https://github.com/notifications), accept it, reload


## 1. Start together

One person drives. The whole team answers out loud. This runs once per team,
because it decides your angle and builds the structure everyone else works
inside.

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

**Then merge it right away**, before anyone splits up. Your teammates' sessions
start from `main`, so until you merge, they'll open an empty repo and build a
second, different wiki.

## 2. Split up, one source each

Everyone now runs their own session. If you opened this repo before the driver
merged, run this first:

```
Pull the latest from main so I have the wiki the team just merged.
```

**Claim a different source from this list.** Two are already in `sources/`, so
these are the ones still missing:

- UN targets for your goal: `sdgs.un.org/goals/goal12`
- One dataset (UN Stats, World Bank, or a local source)
- A news story about the problem in your first region
- A news story about the problem in your second region
- One product or program already trying to solve this

**Then run this prompt**, swapping `[your source]` and `[your region]` for the
one you claimed:

```
Find a source on [your source] in [your region]. Create a markdown file in
sources/ with the page title, the URL, today's date, the key facts and figures
with short direct quotes, and a two-sentence summary. Don't edit the wiki pages
yet.
```

Watch what Claude does while it works: it searches, opens a page, then writes a
file. Those actions are where your citations come from.

Write down the numbers that matter and quote them exactly. Don't copy whole
articles into the repo. A judge wants the figure and the source, not the page.

## Save your work

You never type git commands. Ask:

```
Commit our work with a note about what we did, and push it.
```

Claude saves to your own draft branch and shows you each command it ran.

## Merge, so your work counts

Claude has been saving to a **draft branch**: your own private copy of the team's
work. Nobody else can see it, and none of it counts yet.

To publish it you open a **pull request**, usually shortened to **PR**. That's
GitHub's word for a proposal. It says: here are my changes, should we add them to
the team's real work? Somebody looks at it, then merges it. At a company a
teammate reviews it first. Today your team is the reviewer.

Two clicks, in two different places.

**In Claude Code:** look just above the message box for the bar with your branch
name and a green count like `+482 -0`. Click it to see everything Claude changed,
then select **Create PR**.

**Then on GitHub:** Claude gives you a link to the PR. Open it and press **Merge
pull request**, then **Confirm merge**.

Lost the link? Go to [your repo](https://github.com/LMU-GLP/2026-sdg-12) and
click the **Pull requests** tab. Yours will be in the list.

There is no merge button inside Claude Code. Creating the PR only proposes the
change. Merging is what puts it on `main`.

If GitHub says there's a conflict, that's normal when several people work at once.
Ask:

```
Merge main into our branch and resolve the conflicts.
```


You'll do this twice: once right after step 1, so your teammates start from the
wiki instead of an empty repo, and again once everyone's sources are in.

## 3. Finish together

One person drives again, and everyone watches the pages connect to each other.

```
Ingest everything in sources/ and update the wiki.
```

## 4. Read what you built

Merge again, then look at what's actually on `main`:

**[github.com/LMU-GLP/2026-sdg-12](https://github.com/LMU-GLP/2026-sdg-12)**

You should see `sources/` holding the raw pages, `wiki/` holding what Claude
wrote from them, and `CLAUDE.md` holding the rules. Click into `wiki/` and read
the pages as a team.

If you only see the README, your work is still on a draft branch. Go back and
merge.

This is the first time you see the whole thing instead of one answer at a time.
It's also where you notice if your evidence is thinner than you thought. If a
page makes a claim with no citation behind it, treat it as a placeholder. Never
put it in your pitch.

## 5. Decide, and write it down

This is the hard question, and it's the same move as step 1. Claude asks, you
decide.

```
Help me draft a problem statement from our wiki. Ask me one question at a time.
```

Answer out loud, as a team. The questions come from your own evidence, so this
is where you find out which region you can actually defend and who your project
is really for. Argue about it. That argument is the work.

When you're happy with it:

```
Save it to wiki/problem-statement.md and commit.
```

Then read it out loud one more time. If any team member can't defend a sentence
in it, that sentence needs a better source. Merge it.

## 6. If you finish early

```
Find contradictions and gaps in our wiki, and tell us what we're missing.
```

## Before you leave

- Your work is **merged to `main`** and you can see it on GitHub
- `wiki/problem-statement.md` exists, with at least two citations
- A region you picked on purpose and can defend out loud
- No uncited claims in anything you plan to pitch
