# Brief protocol

How the morning agent turns raw catches into Sid's brief. Published to the mirror
repo so the routine can fetch it; the routine's own prompt carries the safety
invariants, because a spec fetched over the network must never be able to talk the
agent out of refusing to publish.

---

## 1. Select

From `catches[]`, keep a row if ALL hold:

- `detectedAt` is within the last **24 hours**
- `detector` is not `reddit-localllama` and not `hn-newest-100` — both retired to
  window-only. They still get fetched (they feed cascade detection) but no longer
  emit. Any row from them still in the store is residue.
- `pri <= 26`

Sort ascending by `pri`. **Do not take a fixed number of rows.**

The brief is as long as the day deserves. A quiet day is three rows; a real day is
twelve. If it is always the same length, the length has stopped meaning anything and
the reader learns to skim. If more than 25 rows clear the bar, take 25 and SAY in the
brief that you truncated — a silent truncation reads as full coverage.

Zero rows is a legitimate answer. Say so plainly rather than lowering the bar to fill
space.

## 2. Write the verdict

Every row gets `verdict`: **one sentence** on what it means and what, if anything, to
do about it. This replaces the raw field dump as the headline. It is the whole reason
the brief is worth opening.

Rules:

- **Take a position.** "Z.ai shipped GLM-5.3-Flash — first natively multimodal model
  in the GLM line, and transformers already supports it, so it is usable today" is a
  verdict. "New model repo under Qwen. Tags: transformers, safetensors" is a database
  row. He can read database rows; he asked for this because he cannot absorb them.
- **~40 words.** Hard ceiling. Long daily pieces do not get read; this is measured, not
  a style preference.
- **Plain English.** No estate vocabulary, no "hop 0", no "cascade shape". Sid has
  corrected this repeatedly: define a thing in one plain sentence before naming it.
- **Connect rows that are the same story.** If a routing row, a weights upload and a
  GitHub release are all one launch, say so in one verdict and drop the duplicates.
  That connective work is the editorial value; three rows for one event is noise.
- **Never invent.** If a row's own `ctx` does not tell you what it is, say what is
  observable and stop. A confident wrong verdict is worse than a dull right one, and
  it is the failure this whole project exists to prevent.
- **Say when something does not matter.** "Routine maintenance release, nothing to do"
  is a useful verdict. Padding it into significance is how trust dies.

## 3. Health

Set `FEED_HEALTH` next to `FEED`:

```js
var FEED_HEALTH = {
  ok: true,                       // false when the mirror is stale or the fetch failed
  generatedAt: "<iso from mirror>",
  reason: null,                   // when ok:false, what went wrong, in plain words
  daysSinceLastClick: <n|null>    // from the mirror's `clicks`; null = never clicked
};
```

**When the feed is broken, publish the brief WITH `ok:false` and a reason.** Do not
publish nothing.

This is the load-bearing rule. Sid's documented root bug across his whole estate is
*absence rendering as health*: he built twelve readouts, none had a reader, and each
took months rather than days to prove dead. A brief that silently stops updating looks
exactly like a quiet week. A brief that says **"Early signal has been down since
Tuesday"** cannot be mistaken for one.

The client obligations in the brief are still worth showing on a day the feed is
down — so the page still publishes, with the banner.

## 4. Extract the body cleanly

`Artifact read` hands you a full document: a platform-injected `<head>` with a
`frame-runtime` script, then `<body>`, then Sid's authored page, then `</body></html>`.

Republish **only the authored page** — everything after the first `<body>` and **before
the final `</body></html>`. Keep the closing tags and you ship a duplicate: the run on
2026-08-26 left two `</body></html>` lines because it took everything after `<body>`
without trimming the tail, and the platform then added its own. Harmless once, but it
compounds every day nobody looks.

## 5. Verify before publishing

The rendered result must still contain `CURATED`, `claude.use`, and be over 20,000
characters. If any check fails, STOP and report. Never publish a brief you have not
verified, and never publish one built from a failed read.
