# Edition protocol

How the morning agent sets *The Early Edition*. Published to the mirror repo because the
routine's prompt has a hard length limit; the **safety invariants live in the prompt**, not
here, so a spec fetched over the network can never talk the editor into publishing.

Ruled by Sid, 2026-08-27: the paper is the daily surface for the wire. *What Needs You* keeps
the things that need **him** — billing, clients, filings. Two surfaces, two jobs: reading and
acting. Do not move client obligations into the paper.

---

## 1 · Read

```
https://raw.githubusercontent.com/Jaax-Labs/feed-catches/main/catches.json
```

Gives `{generatedAt, count, clicks, catches[]}`. Each catch may carry:

- `extract` — `{ok, text, chars, fetchedAt}`. **This is the actual content of the thing**,
  fetched by the Worker at catch time. The Worker has open egress; you do not. You cannot
  fetch these pages yourself, so the extract is the only real material you will get. Write
  from it.
- `clock` — `daily` or `slow`. **This is the field, not `lane`.** `lane` says
  `brief` on every row forever; it is the push-cap contract for a different surface
  and carries no editorial meaning. The 29 August edition printed with no split and
  flagged the gap on its own front page, correctly: the field it was told to read
  did not exist. Fixed 2026-08-29.
- `questions` — which of Sid's standing questions it matched. Always an array;
  empty means unrouted, which is never a reason to drop something.
- `spiked` — present and `true` only when the row trips TASTE's explicit spike
  list. Advisory. You still decide.
- `pri`, `title`, `sub`, `ctx`, `acts`, `detector`, `detectedAt`
- `editorial` (top level, beside `catches`) — `{clocks, routed, unrouted,
  unmappedLaneFamilies}`. The wire's own accounting of the cut it already made.
  If `routed` is 0 across a full window, the four standing questions matched
  nothing and are decoration; say so in the ledger rather than staying quiet.

**Freshness gate, before anything else.** If `generatedAt` is missing or older than six
hours, the wire has frozen. A frozen mirror serves HTTP 200 with a full plausible body
forever, so the status code proves nothing. **Publish the paper anyway, with the front-page
notice described in §7.** Never publish silence.

## 2 · Select

- **`clock: "daily"`** prints every day.
- **`clock: "slow"`** prints **on Mondays only**. Other days it accumulates; say how many wait.
- If every row carries the same clock, that is a wire defect, not a quiet week.
  Print the paper and say so plainly, the way §7 handles a dead wire.
- Inside a lane: priority first, then whether it matched a standing question.
- **No fixed number of stories.** A quiet day is a short paper. If the length never varies,
  the length has stopped carrying information and he will learn to skim it.
- Zero stories is legitimate. Print the masthead, the ledger, and say the day was quiet.

Sid's four standing questions — what this wire watches *for*, ratified 2026-08-27:

1. **model-switch** — a model ships that he should actually switch to
2. **agent-craft** — the craft of running agents changes
3. **graph-memory** — the graph / memory thread moves
4. **lab-board** — a lab makes a move that changes the board

A match is a strong reason to print. **A non-match is not a reason to spike** — the unrouted
pile is where anything genuinely new necessarily appears first.

## 3 · Merge at edition time

The wire files everything; the desk decides what is one story. Three rows for one launch — a
routing row, a weights upload, a library release — is **one story**, and saying so *is* the
editorial work. Yesterday's GLM lead was exactly this.

Merge on the subject, not the source. When you merge, the **sequence** is often the story:
*"the routing row was visible before the blog post"* means something. Keep it.

## 4 · Write

**Write from `extract.text`, not from `ctx`.** `ctx` is the publisher's own blurb; the extract
is the page. Sid's complaint about the first edition — *"the information extracted was pretty
limited just cards"* — is answered here or nowhere.

- **Lead:** one story, 4–6 short paragraphs, a deck, a byline.
- **Others:** 2–3 paragraphs.
- **Briefs:** two or three sentences.
- **Decision altitude.** What changed, what it costs, what it replaces, whether it is usable
  today. Never syntax. He operates at intent and architecture and openly disclaims code-level
  detail; writing below that altitude is as useless to him as writing above it.
- **Attribute claims.** A vendor's benchmark is *"the publisher's figures"*, printed as a
  claim. Never launder a press release into a finding.
- **Say when something does not matter.** *"Sector news; nothing here asks anything of you"*
  is a service. A paper that never says it is not worth opening.
- **Plain English.** No "hop 0", no "cascade shape", no priorities, no detector names.
- **Never invent.** If the extract failed and you have only a title, write only what is
  observable. A confident wrong sentence is worse than a dull true one.

**WHERE UNREADABILITY GOES.** Ruled by Sid 2026-08-29. It belongs in the source line, never in
the prose. Mark it once, beside the attribution:

```
Src: Latent Space · headline only, body unreadable
```

The prose itself never hedges, never trails off, and never ends on what the paper could not do.
When the facts run out, the story stops. The 29 August edition printed some version of "we
couldn't read it" eleven times in 13,274 characters, and it was the LAST SENTENCE of five
separate stories. That trains a reader to skim, which defeats the honesty it was trying to buy.

**A row marked `truncated` is a publisher's free preview, not the article.** SemiAnalysis ships
~24,000 characters and then stops. Treat it as a long excerpt: everything in it is quotable, and
the piece may have concluded something you have not seen. Say "the rest is paywalled" in the
source line, not in the last paragraph.

**Do not print the machine's reasoning per item.** Sid ruled on 2026-08-27 that the page stays
clean — no "held for slow lane because…" labels next to stories. The ledger in §6 carries the
accounting instead.

**Typography carries meaning** (measured off the live NYT): headlines are the same face at
opposite weights — **700 for hard news** (something shipped, something changed) and **300 for
features** (an interview, an essay, an argument). Use `hed-news` and `hed-feature`. It lets him
read the kind of story before reading the story.

## 4b · Whose paper this is

Fetch:

```
https://raw.githubusercontent.com/Jaax-Labs/feed-catches/main/TASTE.md
```

It is not a list of likes. It is the **tensions to hold** while choosing — built from his watch
history, his bookmarks, and six gauges he ratified himself. Read it before you select, and let
it shape what leads and how you write. Three of its calls bind hardest:

- **Breadth ⇄ Depth (60, rising).** He runs many projects at once. Do not narrow the paper to
  whatever he touched yesterday; adjacent fields are the working mode, not a distraction.
- **Product Fluency (42).** Write at decision altitude — what changed, what it costs, what it
  replaces. Never syntax.
- **Consumption ⇄ Production (57).** He watched 1,833 videos in ninety days. This paper adds
  more. Every extra story is a vote for consumption: **when in doubt, cut it and count it.**

Spike outright, and only these: crypto/web3 · Kubernetes/Terraform-scale infrastructure ·
prompt-tips listicles · personality drama · vector-database *product announcements* (a measured
retrieval result is a different thing). Everything else gets a lane, not a verdict.

**Apply it silently.** Sid ruled 2026-08-27 that the page carries no per-item machine
reasoning — no "held because…" labels beside stories. The ledger in §6 is the accounting; the
stories are just stories.

**It is a draft he has only partly checked.** Two of its claims were wrong and he overruled
both — in each case it had read *absence of a word in his writing* as *absence of interest*. So
treat it as a strong prior, not a rule: if a story is plainly important and the profile is
silent on it, print the story.

## 4d · The writing standard

Fetch:

```
https://raw.githubusercontent.com/Jaax-Labs/feed-catches/main/WRITING-STANDARD.md
```

Ten criteria, four of them hard gates. Its definition, which is the whole thing in one line:
**writing that read the source, reached a conclusion, and put that conclusion in a sentence
short enough to be wrong.** Machine prose is recognisable by its total absence of exposure, not
by its vocabulary.

**Score every story. Enforce nothing yet.** Ruled by Sid 2026-08-29: for the first week every
story prints regardless of its score, and the scores go in the ledger so he can see where the
rubric disagrees with his own reading. The rubric has never been calibrated against a real
draft, and turning on gates before that would silently spike stories nobody could see it remove.

Two things it measured that change how to use the style rules:

- **The em dash carries no signal about quality.** Measured across 27,540 words, and again by a
  second run over 66,057. Professional journalism uses them at least as freely as vendor
  marketing does. Keep the ban as house style; never count it as evidence a draft is good.
- **Banned phrases separate good prose from machine prose. Banned single words do not.** The
  AI-vocabulary list showed complete overlap between the two classes.

And the trap in the anchor: **Harari's openings and closings are his weakest, most imitable
moves.** His middles are the reason he is on the list. Do not write his first or last sentence.

## 5 · The wildcard

One row per day, in its own box, labelled **"Printed Because It Was Cut."** Take something the
selection would have dropped and print it anyway.

This exists because a ranker that is never wrong in public is never corrected. Its own copy
states the test: if these are consistently useless the ranker is right and the box goes; if he
keeps opening them, the ranker is narrowing him.

On Mondays, prefer a wildcard from the daily lane, since the slow lane already prints.

## 6 · The ledger

The dateline's `N printed` and the ledger's `printed` row are the same number.
The 29 August edition said 17 in one and 25 in the other. Count once, print twice.

Every edition ends with the cut, as a table:

```
cleared the wire · printed · held for the slow lane · folded into other stories
· spiked as noise · waiting for Monday
```

The numbers must reconcile. This is the most important structural element in the paper: Sid
built twelve "readouts", none had a reader, and each took **months** rather than days to prove
dead — because nothing counted what was not being used. A cut nobody is told about reads as
full coverage.

## 7 · When the wire is down

Do not skip the edition. Print it with a front-page notice above the masthead rule, in the
warning colour, saying the wire has been down and since when — plainly, in words, no jargon.

A paper that quietly stops arriving is indistinguishable from a quiet week. That confusion is
the exact failure this entire system exists to prevent, and it is Sid's documented root bug:
**absence rendering as health.**

## 8 · Ship

Fetch the template:

```
https://raw.githubusercontent.com/Jaax-Labs/feed-catches/main/edition-template.html
```

Replace everything between `<!-- EDITION:BEGIN -->` and `<!-- EDITION:END -->` with your
stories. Leave the masthead, styles and the click-receipt script untouched. Update the
dateline counts to the truth.

Every story headline links via `data-go="<catch id>"` and its real `href`; the script rewrites
those through the click receipt. Do not link-wrap by hand.

Verify before publishing: the result still contains `EDITION:BEGIN`, `UnifrakturMaguntia` and
the `/go` script, and exceeds 12,000 characters. Then publish with the Artifact tool to:

```
https://claude.ai/code/artifact/ed8478cb-f802-4631-940b-51c8232e1ba1
```

If any fetch or check fails, **stop and report**. Never publish a page you have not verified.
