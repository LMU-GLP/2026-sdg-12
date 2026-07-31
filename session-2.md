# Session 2: build the prototype

Friday, 90 minutes. You're turning evidence into something a judge can open on
their phone.

[Back to the front page](README.md) · [Session 1](session-1.md)

By 12:15 your team has a problem statement you can defend, something a judge
can open at a public URL, and a pitch you've said out loud once.

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


Then, always, before anything else:

```
Pull the latest from main so I have everything the team has merged.
```

## 1. Source sprint (15 min)

Your repo has two sources. **Your team adds at least three more today**, and
everyone writes one.

This is also where you learn the part Wednesday didn't get to: writing a file,
opening a PR, and merging it. You'll do it again when you build, so get it
wrong here where it's cheap.

**Claim a different source from this list.** The first one is the easiest, so
whoever goes first should take it:

- UN targets for your goal: `sdgs.un.org/goals/goal12`
- One dataset (UN Stats, World Bank, or a local source)
- A news story about the problem in your chosen region
- One product or program already trying to solve this
- Anything your two seeded sources told you was missing

Swap `[your source]` and `[your region]` for the one you claimed:

```
Find a source on [your source] in [your region]. Create a markdown file in
sources/ with the page title, the URL, today's date, the key facts and figures
with short direct quotes, and a two-sentence summary. Don't edit the wiki pages
yet.
```

Save it, open a PR, merge it. The steps are at the bottom of this page.

## 2. Ingest what you found (5 min)

One person drives. Everything merges first, then:

```
Ingest everything in sources/ and update the wiki.
```

Merge that too.

Do this **before** the interview, not after. The next step asks Claude to
design against your evidence, and until you ingest, your wiki still only knows
about the two sources you were given. You'd be deciding without the three you
just went and found.

## 3. Lock the problem, then the concept (10 min)

Everyone in the room, out loud. Claude asks, you decide.

**Two things, in this order.** Wednesday was supposed to end with a problem
statement and most teams never got there, so it happens now. It has to come
first, because you can't choose a solution before you've chosen the problem.
Five minutes on each.

```
Two things, in order, and interview us for both. Ask one question at a time,
give us multiple-choice options, and use everything in sources/ and wiki/ as
background. Tell us when our answers contradict our own evidence.

FIRST, our problem statement. Which region can we actually defend, who
specifically is affected, and what do our sources say about them?

THEN, our solution to it. It could be a business, a program, a service, a
product, a campaign, or something we haven't thought of yet. Don't assume
which one. Keep asking until you know who it's for, what it actually does,
how it would work in the real world, and what we're deliberately leaving out.

Save the problem statement to wiki/problem-statement.md and the solution to
wiki/concept.md, then commit both.
```

Argue about the first half. That argument is the work, and the problem
statement is the first thing a judge will push on Monday. If anyone on your
team can't defend a sentence in it, that sentence needs a better source.

Talk, don't type. Use your laptop's dictation. Spoken answers are longer and
better than anything you'd type in 30 seconds, and the whole team hears the ask.

## 4. Plan, then cut it (5 min)

```
Write a short plan for building a page that shows our concept to someone who
has never heard of it. List the steps in order. Keep it to what four people can
finish in 25 minutes.
```

Read the plan out loud and cut anything you can't finish. Scoping is the lesson
here. A small thing that works beats a big thing that doesn't.

## 5. Build it (25 min)

Now make your solution come to life. Tell Claude what you decided and let it
build.

**What you build is up to you.** Some options, none of them required:

- **A web app** — if your solution is a product, build the actual thing
- **A website for your business** — the real site, not a picture of one
- **A sign-up page for your program** — how somebody would genuinely join
- **A dashboard** — your evidence, laid out so the problem is impossible to
  ignore
- **Something else entirely** — if you can describe it, Claude can probably
  build it. Ask

One technical rule: it has to be `index.html` in the root of this repo, because
that's the file GitHub Pages publishes.

```
Build it as index.html in the root of this repo so GitHub Pages can serve it.
Use real figures from our sources and put the citation next to each number on
the page. No invented statistics.
```

Then keep going. If the first version is dull, say so and ask for better. Ask
for a chart. Ask it to make the page work on a phone. You have 25 minutes and
Claude is fast, so the limit is what you ask for, not what it can do.

## 6. Verify (5 min)

Never let Claude tell you it's done. Make it show you.

```
Show me it works. Open the page, check every link, and check every number on
it against the file in sources/ it came from. Tell me what's broken or
uncited. Don't tell me it should work.
```

Fix whatever it finds. Then merge.

## 7. Deploy (7 min)

Merge to `main` and your page goes live here:

**https://lmu-glp.github.io/2026-sdg-12/**

Give it a minute. Open it on your phone. If a judge can't open it Monday, it
doesn't count.

## 8. Say it out loud (8 min)

Ninety seconds, timed, to another team. They ask you one question afterward.

```
Write a 90-second pitch script from our problem statement and our concept.
Plain spoken language, not a summary. Open with the problem and the number
that proves it,
name who it's for, say what our solution actually is, point at what we built,
and end with what we want. Save it to wiki/pitch.md and commit.
```

You'll polish delivery Saturday at the pitch workshop. Today just proves the
script exists and fits in 90 seconds.

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


## Before you leave

- Your page is **live** at the URL above and opens on a phone
- `wiki/problem-statement.md`, `wiki/concept.md` and `wiki/pitch.md` are merged to `main`
- Every number on the page traces to a file in `sources/`
- At least five sources in `sources/`, three of them yours
- A punch list with a name on each task, for Saturday 9:00–10:30 AM, Sunday
  5:15–10:00 PM, and Monday 9:00–10:00 AM
