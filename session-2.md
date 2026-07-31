# Session 2: build the prototype

Friday, 90 minutes. You're turning evidence into something a judge can open on
their phone.

[Back to the front page](README.md) · [Session 1](session-1.md)

By 12:15 your team has a working web app at a public URL, built from your own
sources, and you've said your pitch out loud once.

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

## 1. Source sprint (20 min)

Your repo has two sources. **Your team adds at least three more today**, and
everyone writes one.

This is also where you learn the part Wednesday didn't get to: writing a file,
opening a PR, and merging it. You'll do it again for the app, so get it wrong
here where it's cheap.

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

While that's happening, everyone not writing a source starts step 2.

## 2. Lock the concept (10 min)

Everyone in the room, out loud. Claude asks, you decide. This is the same
interview you ran on Wednesday, pointed at a solution instead of a question.

```
We're designing a solution to our challenge: "How might we help a household reduce waste and make smarter choices about what members buy, use, and throw away?"

It could be a business, a program, a service, a product, a campaign, or
something we haven't thought of yet. Don't assume which one.

Before you suggest anything, interview us. Ask one question at a time, give us
multiple-choice options, and keep going until you know who this is for, what it
actually does, how it would work in the real world, and what we're deliberately
leaving out. Use everything in sources/ and wiki/ as background, and tell us
when our answers contradict our own evidence.

When we're done, write the design to wiki/concept.md and commit it.
```

Talk, don't type. Use your laptop's dictation. Spoken answers are longer and
better than anything you'd type in 30 seconds, and the whole team hears the ask.

Then bring the new sources in:

```
Ingest everything in sources/ and update the wiki.
```

## 3. Plan, then cut it (5 min)

```
Write a short plan for building a page that shows our concept to someone who
has never heard of it. List the steps in order. Keep it to what four people can
finish in 25 minutes.
```

Read the plan out loud and cut anything you can't finish. Scoping is the lesson
here. A small thing that works beats a big thing that doesn't.

## 4. Build what you'll show (25 min)

Your concept might be a business, a program, a service, a product, or something
else. What you build today is the page that makes it real to a judge who has
never heard of it. **The page is not the idea. It's how you show the idea.**

Depending on what your team decided, that page might be:

- **A business** — the landing page. What it offers, who it's for, and the
  figures from your sources that prove people need it
- **A program** — the page someone lands on to join. Who runs it, who it
  serves, how you sign up, what it costs
- **A product or app** — a clickable mockup of the one screen that matters most
- **A campaign** — the thing people would actually see, and what you want them
  to do next
- **Anything at all** — a dashboard of your own evidence that makes the problem
  impossible to ignore

```
Build it as index.html in the root of this repo so GitHub Pages can serve it.
Use real figures from our sources and put the citation next to each number on
the page. No invented statistics.
```

## 5. Verify (5 min)

Never let Claude tell you it's done. Make it show you.

```
Show me it works. Open the page, check every link, and check every number on
it against the file in sources/ it came from. Tell me what's broken or
uncited. Don't tell me it should work.
```

Fix whatever it finds. Then merge.

## 6. Deploy (10 min)

Merge to `main` and your page goes live here:

**https://lmu-glp.github.io/2026-sdg-12/**

Give it a minute. Open it on your phone. If a judge can't open it Monday, it
doesn't count.

## 7. Say it out loud (10 min)

Ninety seconds, timed, to another team. They ask you one question afterward.

```
Write a 90-second pitch script from our wiki and our concept. Plain spoken
language, not a summary. Open with the problem and the number that proves it,
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
- `wiki/concept.md` and `wiki/pitch.md` are merged to `main`
- Every number on the page traces to a file in `sources/`
- At least five sources in `sources/`, three of them yours
- A punch list with a name on each task, for Saturday 9:00–10:30 AM, Sunday
  5:15–10:00 PM, and Monday 9:00–10:00 AM
