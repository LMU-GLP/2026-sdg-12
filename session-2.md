# Session 2: build the prototype

Friday, 90 minutes. You're turning evidence into something a judge can open on
their phone.

[Back to the front page](README.md) · [Session 1](session-1.md)

By 12:15 your team has a problem statement you can defend, something live at a
public URL, and a pitch you've said out loud once.

```mermaid
flowchart LR
  R["Research<br/>sources and wiki"] --> P["Problem statement<br/>which region, who"]
  P --> S["Solution<br/>business? program? app?"]
  S --> B["Prototype<br/>a page they can open"]
  B --> T["Pitch<br/>90 seconds"]
```

Each box depends on the one before it. That's why the order is fixed: you can't
choose a solution before you know whose problem you're solving, and you can't
know that until you've read your own research.

## How today works

**One person drives.** One laptop sends the prompts. The driver is the slowest
part of this team, and the decisions are what matter, so those belong to
everybody:

- **Driver** — types, and reads what Claude did back to the team
- **Everyone** — answers the interviews out loud, argues, decides
- **One reader** — opens the repo on GitHub on their own laptop and reads what
  actually landed, while the driver keeps working
- **One timekeeper** — the clock below is real

## Open it

1. Go to **[claude.ai/code](https://claude.ai/code)** and sign in with your Claude
   account
2. **Check the network setting first.** Above the message box there's a cloud
   button. It should already say **Full network access**. If it says anything
   else, click it and change it. Claude cannot read a single web page without
   this, and it fails quietly: searches come back, then nothing loads
3. Click **+ Select repo...**
4. In the dropdown that opens, click **Connect to GitHub**
5. GitHub asks whether Claude can access your account. Press the green
   **Authorize** button
6. Back in the repo list, search for `2026-sdg-12` and click
   **LMU-GLP/2026-sdg-12**

**Repo not in the list?** You haven't accepted the invitation to it yet. Open
**[github.com/LMU-GLP/2026-sdg-12/invitations](https://github.com/LMU-GLP/2026-sdg-12/invitations)**
and press **Accept invitation**. Then reload Claude Code and go back to step 3.


Only the driver needs to do this. Everyone else can read the repo straight from
[github.com/LMU-GLP/2026-sdg-12](https://github.com/LMU-GLP/2026-sdg-12).

## Your clock

| | |
|---|---|
| 10:55 | Build the wiki |
| 11:05 | **Read it** |
| 11:10 | Write the problem statement |
| 11:20 | **Read it out loud** |
| 11:25 | Design the solution |
| 11:35 | Plan, build, verify |
| 12:05 | Deploy |
| 12:10 | Show it |

## 1. Build the wiki, in one shot (10 min)

Two sources are already in `sources/`, one on each region. **Read them before
you send anything** — they're the only evidence you have right now:

- [Los Angeles](sources/la-sb1383-organic-waste.md)
- [South Korea](sources/korea-food-waste-system.md)

This prompt reads them, finds three more, and builds the wiki from everything
in `sources/`.

```
Set up this repo as an LLM wiki for our challenge:
"How might we help a household reduce waste and make smarter choices
about what members buy, use, and throw away?"

Read this gist first. It's the pattern we're using, and it explains how the
whole thing should be structured:
https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

Then start from the two sources already in sources/ and read them both. Find
three more: the UN targets for our goal at
https://sdgs.un.org/goals/goal12, one dataset with real figures, and one
program or business already working on this problem. Save each new one as its
own file in sources/, in the same format as the two that are there: page title,
URL, today's date, key figures with short direct quotes, and a two-sentence
summary.

Now build the wiki in wiki/ from all sources, following the structure the
gist describes. Every claim has to cite the source file it came from. Include
one page comparing Los Angeles and South Korea, because we haven't picked a
region yet.

Also write wiki/index.md, listing every page with a link and a one-line
summary, so we know where to start reading.

When you're done, tell us what you found and what surprised you.
```

Watch it work. It searches, opens pages, then writes files. Those actions are
where your citations come from.

Then save it, and publish it so the rest of the team can actually see it:

```
Commit our work with a note about what we did, and push it.
```

Now publish it. Claude saved to a **draft branch**, the driver's own private
copy. Nobody else can see it and none of it counts yet.

A **pull request**, or PR, is GitHub's word for a proposal: here are my changes,
should we add them to the team's real work? At a company a teammate reviews it
first. Today your team is the reviewer.

Ask Claude to open one:

```
Create a pull request for our work and give me the link.
```

Open the link it gives you, press **Merge pull request**, then **Confirm
merge**.

**Didn't get a link?** Go to
[your repo](https://github.com/LMU-GLP/2026-sdg-12) and click the
**Pull requests** tab. There'll be a yellow banner naming your branch with a
green **Compare & pull request** button. Press that, then **Create pull
request**, then **Merge pull request**.

Claude can open the pull request. It cannot merge it — merging is always your
click, and it's what puts the work on `main`.

Don't skip this. Until you merge, the wiki exists only on the driver's private
branch, and the next step asks everyone else to read it.

**You can add more sources later, any time today.** If you spot a gap, or a
judge-proof number you wish you had, just ask for it:

```
Find a source on [what you want] and save it to sources/ in the same format as
the ones already there.
```

A new file in `sources/` changes nothing on its own, though. The wiki is what
your page and your pitch get built from, so every time you add a source, follow
it with:

```
Ingest everything in sources/ and update the wiki.
```

Then commit, push, and merge again.

## 2. Read what you built (5 min)

**Stop typing.** Everyone opens the wiki on their own laptop:

**[github.com/LMU-GLP/2026-sdg-12/tree/main/wiki](https://github.com/LMU-GLP/2026-sdg-12/tree/main/wiki)**

**Start with `index.md`.** It lists every page with a one-line summary, so read
that first, then open the two or three pages that sound most important. Don't
try to read all of them in five minutes.

Empty, or a 404? You haven't merged. Go back and merge, then reload.

This is the step teams skip, and everything after it is built on what you find
here. Four questions, out loud:

- Which region has more evidence behind it, LA or South Korea?
- Which number is the most surprising?
- Which claim has no citation under it? That's a placeholder, not evidence
- What does the wiki say that you didn't already believe?

If everything in the wiki is something you already assumed, Claude told you what
you wanted to hear and you should push back on it.

## 3. Write the problem statement (10 min)

Everyone answers, out loud. Claude asks, you decide.

```
Interview us until we have a problem statement we can defend. Ask one question
at a time and give us multiple-choice options.

We need to end up with: the region we're committing to, who specifically is
affected, how many of them, and what our sources actually say about them. Use
everything in sources/ and wiki/, and tell us when our answers contradict our
own evidence.

Don't write it until we've answered. Then save it to
wiki/problem-statement.md, with a citation on every figure, commit, and push.

Then print the whole problem statement in the chat so we can read it.
```

Argue about this. The region is a real choice and you have evidence for both.

## 4. Read the problem statement out loud (5 min)

**Stop typing again.** One person reads it aloud, slowly, to the team.

Everyone else can follow along. Claude prints the statement in the chat and
gives you a link to the PR it pushed to — open that link and you'll see the
file. **You don't need to merge for this**, and you don't need to go hunting
for a branch.

Scrolled away? Ask:

```
Show us the problem statement again.
```

Then, honestly: **can every single one of you defend every sentence?** If
anyone hesitates on a sentence, that sentence needs a better source or it needs
to go.

```
Here's what we're unsure about: [say what]. Find a source that settles it, or
tell us the claim isn't supported and cut it.
```

This is the paragraph you'll get asked about first on Monday, so it's worth
the five minutes.

## 5. Design the solution (10 min)

Now, and only now, the solution. You couldn't have done this first — you didn't
know whose problem you were solving.

```
Now interview us about our solution to that problem statement.

It could be a business, a program, a service, a product, a campaign, or
something we haven't thought of yet. Don't assume which one.

Ask one question at a time with multiple-choice options, and keep going until
you know who it's for, what it actually does, how it would work in the real
world, and what we're deliberately leaving out. Push back when our idea doesn't
match the problem statement we just wrote.

Then save it to wiki/concept.md, commit, and push.
```

Talk, don't type. Use your laptop's dictation. Spoken answers are longer and
better than anything the driver would type in 30 seconds, and the whole team
hears the ask.

## 6. Plan, then cut it (5 min)

```
Write a short plan for building a page that shows our concept to someone who
has never heard of it. List the steps in order. Keep it to what we can finish
in 25 minutes.
```

Read the plan out loud and cut anything you can't finish. Scoping is the lesson
here. A small thing that works beats a big thing that doesn't.

## 7. Build it (25 min)

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

One technical rule: it has to be `index.html` in the root of this repo. That
exact name and place is what makes it show up as a real web page later — step 9
explains why.

```
Build it as index.html in the root of this repo so GitHub Pages can serve it.
Use real figures from our sources and put the citation next to each number on
the page. No invented statistics.
```

Then keep going. If the first version is dull, say so and ask for better. Ask
for a chart. Ask it to work on a phone. You have 25 minutes and Claude is fast,
so the limit is what you ask for, not what it can do.

## 8. Verify (5 min)

Never let Claude tell you it's done. Make it show you.

```
Show me it works. Open the page, check every link, and check every number on
it against the file in sources/ it came from. Tell me what's broken or
uncited. Don't tell me it should work.
```

Fix whatever it finds.

## 9. Deploy (5 min)

First save it:

```
Commit our work with a note about what we did, and push it.
```

Then publish it, the same way as step 1:

```
Create a pull request for our work and give me the link.
```

Open the link, press **Merge pull request**, then **Confirm merge**. Merging is
what publishes the page. Nothing goes live from a draft branch.

Your page is here:

**https://lmu-glp.github.io/2026-sdg-12/**

Give it a minute, then open it on your phone.

## Why that address works

**GitHub Pages** is a free service that turns a repo into a real website. It's
already switched on for your repo, so anything you merge to `main` gets served
at the address above. No hosting to set up, no account to make, nothing to pay
for. Merging is the deploy.

And `index.html` is the front door. When someone types an address that ends in
a slash with nothing after it, the browser asks the server for `index.html` by
default. That's a rule of the web, not something GitHub invented, and it's why
step 7 insisted on that exact filename in that exact place. Name it anything
else and the address above shows a 404, even though your file is sitting right
there in the repo.

## 10. Write the pitch, then say it out loud (5 min)

Write it first:

```
Write a 90-second pitch script from our problem statement and our concept.
Plain spoken language, not a summary. Open with the problem and the number
that proves it, name who it's for, say what our solution actually is, point at
what we built, and end with what we want. Save it to wiki/pitch.md, commit,
and push.
```

Then one person reads it out loud to the rest of the team, timed.

Everyone else listens for anything that doesn't land: a number that comes out
of nowhere, a sentence nobody could follow, a claim you can't say with a
straight face. Say what you noticed, fix it, and you're done for today.

**On Monday you won't be reading this.** You also don't need it memorised word
for word — that almost always sounds worse than knowing it. Know it well enough
to talk to it: the problem, the number that proves it, who it's for, what you
built, what you want. Saturday's pitch workshop is where you get there.

Today just proves the script exists and fits in 90 seconds.

## What's next

Today ends here. The repo doesn't.

Everything you built is on `main`, and you can open Claude Code on this repo any
time before Monday.

**Keep building.** If your prototype is a rough first version, make it a second
one. Add a page, add a chart, make it work properly on a phone. If your solution
needed something you ran out of time for, ask for it now.

**Use it for the presentation too.** Claude can write your deck from the same
wiki your page came from, which is what keeps the slides, the pitch and the demo
saying the same thing:

```
Draft our 10-minute presentation from wiki/. One slide per section, and put the
citation for every number on the slide where that number appears.
```

**Give it the actual assignment.** Put the project brief and the judging rubric
into the repo — a `docs/` folder is fine — then commit and push them. Now Claude
is working against the real criteria instead of guessing at them:

```
Read the brief and the rubric in docs/, then tell us what our presentation is
missing and what a judge would push on.
```

That last one is worth running Sunday night, once the deck exists.


## Saving and merging, any time

You never type git commands. To save:

```
Commit our work with a note about what we did, and push it.
```

To publish, ask Claude to open the pull request:

```
Create a pull request for our work and give me the link.
```

Open that link, press **Merge pull request**, then **Confirm merge**.

No link? Go to [your repo](https://github.com/LMU-GLP/2026-sdg-12) → the
**Pull requests** tab → the green **Compare & pull request** button on the
yellow banner.

Claude can open a pull request. Only you can merge it.


## Before you leave

- Your page is **live** at the URL above and opens on a phone
- `wiki/problem-statement.md`, `wiki/concept.md` and `wiki/pitch.md` are merged
  to `main`
- Every number on the page traces to a file in `sources/`
- At least five sources, all cited in the wiki
