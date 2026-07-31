# Session 2: build the prototype

Friday, 90 minutes. You're turning evidence into something a judge can open on
their phone.

[Back to the front page](README.md) · [Session 1](session-1.md)

By 12:15 your team has a problem statement you can defend, something live at a
public URL, and a pitch you've said out loud once.

## How today works

**One person drives.** One laptop sends the prompts. That's not a demotion for
everyone else, because the driver is the slowest part of this team and the
decisions are what matter:

- **Driver** — types, and reads what Claude did back to the team
- **Everyone** — answers the interviews out loud, argues, decides
- **One reader** — opens the repo on GitHub on their own laptop and reads what
  actually landed, while the driver keeps working
- **One timekeeper** — the clock below is real

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

Two sources are already in `sources/` — one on Los Angeles, one on South Korea.
This prompt reads them, finds three more, and builds the wiki from all five.

```
Set up this repo as an LLM wiki for our challenge: "How might we help a household reduce waste and make smarter choices about what members buy, use, and throw away?"

Read this gist first. It's the pattern we're using, and it explains how the
whole thing should be structured:
https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f

Then start from the two sources already in sources/ and read them both. Find
three more yourself: the UN targets for our goal at
https://sdgs.un.org/goals/goal12, one dataset with real figures, and one
program or business already working on this problem. Save each new one as its
own file in sources/, in the same format as the two that are there: page title,
URL, today's date, key figures with short direct quotes, and a two-sentence
summary.

Now build the wiki in wiki/ from all five sources, following the structure the
gist describes. Every claim has to cite the source file it came from. Include
one page comparing Los Angeles and South Korea, because we haven't picked a
region yet.

When you're done, tell us what you found and what surprised you.
```

Watch it work. It searches, opens pages, then writes files. Those actions are
where your citations come from.

Then save it:

```
Commit our work with a note about what we did, and push it.
```

## 2. Read what you built (5 min)

**Stop typing.** Everyone reads, on GitHub or over the driver's shoulder. This
is the step teams skip, and it's the one that decides whether Monday goes well.

Four questions, out loud:

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
wiki/problem-statement.md, with a citation on every figure, and commit.
```

Argue about this. The region is a real choice and you have evidence for both.

## 4. Read the problem statement out loud (5 min)

**Stop typing again.** One person reads it aloud, slowly, to the team.

Then, honestly: **can every single one of you defend every sentence?** If
anyone hesitates on a sentence, that sentence needs a better source or it needs
to go.

```
Here's what we're unsure about: [say what]. Find a source that settles it, or
tell us the claim isn't supported and cut it.
```

This is the paragraph a judge attacks first on Monday. Five minutes now is
cheaper than freezing in front of them.

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

Then save it to wiki/concept.md and commit.
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

One technical rule: it has to be `index.html` in the root of this repo, because
that's the file GitHub Pages publishes.

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

Save, then merge to `main`, and your page goes live here:

**https://lmu-glp.github.io/2026-sdg-12/**

Give it a minute. Open it on your phone. If a judge can't open it Monday, it
doesn't count.

## 10. Say it out loud (5 min)

Ninety seconds, timed, to another team. They ask you one question afterward.

```
Write a 90-second pitch script from our problem statement and our concept.
Plain spoken language, not a summary. Open with the problem and the number
that proves it, name who it's for, say what our solution actually is, point at
what we built, and end with what we want. Save it to wiki/pitch.md and commit.
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
- `wiki/problem-statement.md`, `wiki/concept.md` and `wiki/pitch.md` are merged
  to `main`
- Every number on the page traces to a file in `sources/`
- Five sources, all cited in the wiki
- A punch list with a name on each task, for Saturday 9:00-10:30 AM, Sunday
  5:15-10:00 PM, and Monday 9:00-10:00 AM
