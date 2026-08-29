# The writing standard

What good writing means for this paper, derived from the three writers Sid named, broken
against the form, and turned into something a model can score a draft with.

**Commission, verbatim.** Asked what writing he rates as excellent, Sid answered: *"yuval noah
harari, walter benjamin, karl marx, im not sure figure out what good writing means"*.

**Status.** Derived, not ratified. Every claim about how these writers work points at a passage
you can open, and every URL in §8 was fetched and verified in this session. The **rubric** in §5
is unverified: no draft has been scored against it and its thresholds are guesses, marked as
guesses. The **anti-rubric** in §6 is implemented at `scripts/slop_detect.py` and partly
measured; §6a reports what it actually found, including two rules that turned out not to work.
§10 lists everything still unverified. Nothing here is true until Sid says so.

---

## 0 · The definition, in three sentences

> Good writing here is writing that took a risk nothing else in the pipeline has any reason to
> take: it read the source, reached a conclusion, and put that conclusion in a sentence short
> enough to be wrong. Everything else in the craft exists to make that sentence survivable, so
> the number arrives with the comparison that gives it size, the vendor's claim is marked as the
> vendor's inside the sentence that carries it, and the last line adds a fact instead of
> restating the first. What Harari, Benjamin and Marx have in common is not a voice but this
> willingness to be caught out, and what makes machine prose recognisable is not its vocabulary
> but its total absence of exposure.

That last clause is the whole document. Sid's complaint is that the prose reads as *"just
regurgitation of training data"*, and he added that em dashes are *"one of a thousand failure
modes."* The second half of that is the instruction. A list of banned words cannot fix
regurgitation, because **regurgitation is a structural property, not a lexical one.** A sentence
reads as regurgitated when nothing in it is at stake: when it would be equally true of a
different company, a different model, a different week. The em dash is a symptom of a sentence
that was assembled rather than decided. Delete every em dash from a story with nothing at stake
and it still reads as machine output.

So this standard is structural first and lexical second, and the anti-rubric in §6 is ordered
that way deliberately.

---

## 1 · The central problem, faced

None of the three wrote news, and none of them would have been any good at it as they are.

Harari writes historical synthesis at civilisational scale. Benjamin writes dense essayistic
prose that works by juxtaposition and image. Marx, in his books, writes analytical polemic that
defers its payoff for hundreds of pages. This paper runs two to six paragraphs on a model
release, a benchmark claim, a chip announcement or a security advisory, for people building with
AI. Benjamin's register applied to a router config would be insufferable, and the failure mode
this document exists to prevent is a rubric that produces pastiche.

**The resolution is that the three names are not a style. They are three solutions to one
problem:** how do you make a reader accept a conclusion they did not hold when they started, in
prose they cannot skim past? Harari solves it by resizing the present against history. Benjamin
solves it by making a physical object carry the claim. Marx solves it by following a mechanism
until the conclusion is forced.

Those are *argumentative* moves, and argument does not have a minimum length. What does have a
minimum length is the *apparatus*: Benjamin's constellation method, Marx's dialectic, Harari's
sweep from foragers to algorithms. The register is the apparatus wearing clothes. **Take the
moves. Leave the apparatus. Take none of the register.**

There is also a fact that reframes the whole problem, and it is the single most useful thing I
found. **Marx was a working newspaperman for a decade.** He filed for the *New-York Daily
Tribune* from 1852 to 1862, hundreds of pieces, on deadline, at column length, about events he
could not control. Benjamin wrote feuilleton pieces and radio talks and worked, all his life, in
short forms. Harari's shortest and best work is his op-eds, not his books. The commission's
premise, that none of them wrote news, is true of the books and false of the careers. Two of the
three specimens I lean on hardest below are literally newspaper articles.

---

## 2 · What the three actually share, mechanically

Nine mechanics. For each: what it is, the evidence in all three, whether it holds in all three,
and a counterexample from the same writer where I could find one. Every passage is fetchable at
a URL in §8.

### M1 · The reframe: they tell you your question is wrong before answering it

Present in all three, and it is the strongest shared mechanic.

Marx, *The Future Results of British Rule in India* (1853): "The question, therefore, is not
whether the English had a right to conquer India, but whether we are to prefer India conquered
by the Turk, by the Persian, by the Russian, to India conquered by the Briton." And earlier, in
*The British Rule in India*, compressed to three sentences: "England, it is true, in causing a
social revolution in Hindostan, was actuated only by the vilest interests, and was stupid in her
manner of enforcing them. But that is not the question. The question is, can mankind fulfil its
destiny without a fundamental revolution in the social state of Asia?"

Harari, opening *The Economist*, April 2023: "Hitherto these fears focused on machines using
physical means to kill, enslave or replace people. But over the past couple of years new AI
tools have emerged that threaten the survival of human civilisation from an unexpected
direction." Five sentences, about 85 words, and it fits inside a newspaper paragraph.

Benjamin, Thesis VIII of *On the Concept of History*: "The astonishment that the things we are
experiencing in the 20th century are 'still' possible is by no means philosophical."

The move has a fixed shape: *here is what you already think · here is the assumption underneath
it · the assumption is wrong · here is the direction you were not looking.* It survives at 60
words.

### M2 · A physical object carries the abstract claim

Present in all three. This is not illustration. The object is the argument, and removing it
removes the claim.

Benjamin, Thesis I: he does not write "historical materialism secretly depends on theology." He
describes the Mechanical Turk in four sentences of physical detail, then names what it is a
picture of. About 120 words, self-contained, and it is a complete short-form piece.

Benjamin again, on the cameraman: "The surgeon represents the polar opposite of the magician.
The magician heals a sick person by the laying on of hands; the surgeon cuts into the patient's
body." Note what makes this work and separates it from decorative analogy: **the two things are
measured on the same named variable**, distance from the patient. An analogy that does not name
its axis is ornament.

Marx: the hand-loom and the spinning-wheel, not "the textile sector." And, in the same
paragraph, people "who go about nearly naked" wearing "a pair of golden ear-rings". The object
carries the whole claim about a society's surplus.

Harari, *Financial Times*, March 2020, in three sentences: "Hitherto, when your finger touched
the screen of your smartphone and clicked on a link, the government wanted to know what exactly
your finger was clicking on. But with coronavirus, the focus of interest shifts. Now the
government wants to know the temperature of your finger and the blood-pressure under its skin."
One object, your finger, measured on the old axis and then the new one. About 55 words. **This
is the single most transferable paragraph I read in the whole corpus.**

### M3 · The number arrives with its counter-number

Present in Marx and Harari. **Absent in Benjamin**, who barely uses numbers at all. I am keeping
it because the form demands it, not because all three do it, and I am saying so rather than
inflating the count to three.

Marx, on British textile exports: "In 1824 the export of British muslins to India hardly
amounted to 1,000,000 yards, while in 1837 it surpassed 64,000,000 of yards. But at the same
time the population of Dacca decreased from 150,000 inhabitants to 20,000." Three numbers, and
the third is the point. Without it the first two are a growth statistic.

Marx again, quoting a Commons committee: grain "selling from 6/- to 8/- a quarter at Khandesh"
and "sold at 64/ to 70/- at Poona, where the people were dying in the streets of famine." The
two prices are the same commodity. The ratio is the argument, and the clay roads are the
mechanism.

Harari: "Fifty years ago, the KGB couldn't follow 240m Soviet citizens 24 hours a day." The
number exists to establish an impossibility that has since been removed. It tells you the change
is one of kind, not degree.

### M4 · The concession is stated at full strength, named, and then ruled on

Present in all three, and it is the antidote to the false-balance sentence.

Marx: "Now, sickening as it must be to human feeling to witness those myriads of industrious
patriarchal and inoffensive social organizations disorganized and dissolved into their units...
we must not forget that these idyllic village-communities... had always been the solid
foundation of Oriental despotism."

Harari: "You might argue that there is nothing new about all this. In recent years both
governments and corporations have been using ever more sophisticated technologies to track,
monitor and manipulate people. Yet if we are not careful, the epidemic might nevertheless mark
an important watershed in the history of surveillance."

The mechanics that matter: the objection is stated in its **strongest** form, it is attributed
to someone who would actually hold it, and it is **resolved in the same paragraph**. That is
what separates it from "while some see this as a breakthrough, others urge caution", which
raises an objection and abandons it. An unresolved objection is worse than no objection, because
it buys the appearance of balance with none of the work.

### M5 · The claim is asserted, not hedged, at the moment it is made

Present in all three, and all three are sometimes wrong as a result. That is the point.

Marx: "They intend now drawing a net of railroads over India. And they will do it." Also "Indian
society has no history at all", a sweeping assertion that the last century of scholarship
has taken apart.

Harari: "AI has thereby hacked the operating system of our civilisation." No modal, no
qualifier.

Benjamin: "That which we call progress, is this storm."

Every one of those is a bet. **Machine prose never bets**, and that is the deepest reason it
reads as regurgitation. The counterexample is instructive and I return to it in §3: Harari's
*Financial Times* piece hedges continuously, and it is his weakest prose in the sample.

### M6 · The adversary's own document, quoted against them, with the interest named

Present in Marx, strongly. Present in Benjamin as method. Weak in Harari.

Marx quotes Sir Stamford Raffles on the Dutch company, a House of Commons report on the village
system, Colonel Warren of Fort St William on troop movements. Then this: "Mr. Campbell himself,
greatly influenced as he is by the prejudices of the East India Company, is obliged to avow 'that
the great mass of the Indian people possesses a great industrial energy...'"

The construction is exact: **name the source, name the interest, then use the admission**. The
admission is strong precisely because it costs the speaker something. This is the provenance
ladder in ARCHITECTURE §3 written as prose rather than as a field, and it gives the paper its
best evidentiary move: *the strongest number in a story is the one the vendor published that
hurts the vendor.*

### M7 · The paragraph turns on its last sentence

Present in all three, and independently confirmed in every newspaper I could read.

Marx ends a flat parliamentary report with two words: "Debate adjourned." He ends a paragraph of
projection with "And they will do it." Benjamin ends the Angel of History paragraph, which until
that point is pure description of a painting, with "That which we call progress, is this storm."
Harari ends a section on emergency powers with "For when people are given a choice between
privacy and health, they will usually choose health."

The last sentence of a paragraph is short and it turns. It does not summarise the paragraph
above it.

### M8 · Named actors, active verbs, physical objects

Present in all three.

Marx: "It was the British intruder who broke up the Indian hand-loom and destroyed the
spinning-wheel." Actor, physical verb, physical object. Not "the textile industry was
disrupted."

Harari: "Netanyahu rammed it through with an 'emergency decree'." A named person, a verb with
force in it, and the euphemism quoted rather than adopted.

Benjamin: "the surgeon cuts into the patient's body."

This is unslop rule 29 arriving from a different direction, and the three writers make the
stronger version of the point: passive voice is usually a missing actor, and a missing actor is
usually an unasked question.

### M9 · Historical depth used to resize the present claim

Present in all three. This is Harari's signature and his most imitable move, which makes it the
most dangerous one, so the test has to be strict.

Harari on handwashing: "it was only in the 19th century that scientists discovered the
importance of washing hands with soap." The historical fact is doing argumentative work. It
establishes that a universal behaviour is recent, learned, and driven by understanding rather
than enforcement, which is the claim of the section.

Marx: the entire opening of *The Eighteenth Brumaire*, where the historical parallel produces a
distinction ("the first time as tragedy, the second time as farce") rather than an atmosphere.

Benjamin: the statue of Venus, venerated by the Greeks and read as an idol by medieval clerics.
Same object, two contexts, one variable.

**The test that separates this from decoration: the comparison must change the size of the
present claim.** If you can delete the historical sentence and the claim is unaffected, it was
ornament.

### The mechanic that does not generalise, and I checked

**Benjamin's juxtaposition without a stated connective.** He places two things beside each other
and refuses to say what the relation is, letting it accumulate across an essay. It is his most
characteristic method and it is the one thing here that cannot be compressed. At news length,
juxtaposition without a stated relation reads either as a non sequitur or, worse, as the "which
raises broader questions about" move. It needs the accumulated context of a long piece to
resolve. **Do not attempt it.**

---

## 3 · Breaking each mechanic against 300 words

| Mechanic | Survives 300 words? | What it looks like at that length |
|---|---|---|
| M1 reframe | **Yes, best of all** | Two sentences. "The benchmark is the story everyone read. The licence is the story." |
| M2 object carries claim | **Yes** | One sentence naming the physical thing. Requires naming the axis if it is a comparison. |
| M3 number with counter-number | **Yes, and the form demands it** | Same sentence or the next one. Never a separate paragraph. |
| M4 concession, named and ruled | **Yes, at two sentences** | Objection in one sentence, ruling in the next. Both in the same paragraph, always. |
| M5 unhedged assertion | **Yes** | This is what the deck and the last sentence of paragraph one are for. |
| M6 adversary's own document | **Yes** | Collapses to a clause: "on the vendor's own eval", "in Nvidia's own filing". |
| M7 paragraph turns on last sentence | **Yes** | Verified in every publication I could read. Under 16 words. |
| M8 named actors, active verbs | **Yes** | Costs nothing. |
| M9 history resizes the claim | **Only under a hard test** | One sentence, and it must change the size of the claim. Two years of context beats two centuries. |
| Benjamin's bare juxtaposition | **No** | Becomes "this signals a broader shift". Banned in §6. |

**What does not survive, stated plainly:**

- **Marx's definitional cascade.** *Capital* chapter one opens "A commodity is, in the first
  place, an object outside us, a thing that by its properties satisfies human wants of some sort
  or another." That is nine hundred pages of deferred payoff. At news length it becomes the
  explainer paragraph nobody reads. This is the counterexample inside Marx's own work.
- **Marx's extended analogy chain.** "Hindostan is an Italy of Asiatic dimensions, the Himalayas
  for the Alps, the Plains of Bengal for the Plains of Lombardy, the Deccan for the Apennines."
  Beautiful, and at 300 words the metaphor would eat every fact in the story.
- **Marx's anaphora at his own density.** Four consecutive sentences beginning "We must not
  forget." At news length that is the rule of three, which unslop rule 10 already bans.
- **Harari's civilisational scale-setter as an opener.** This is the most dangerous transfer in
  the whole commission, so here is the evidence. Harari's *Financial Times* essay of March 2020
  opens: "Humankind is now facing a global crisis. Perhaps the biggest crisis of our
  generation." Portentous, hedged twice in two sentences, and it tells a reader nothing they did
  not have. It would fail criteria C1, C2 and C10 of the rubric below.
- **Harari's binary-choice ending.** The same essay closes: "Humanity needs to make a choice.
  Will we travel down the route of disunity, or will we adopt the path of global solidarity?" A
  rhetorical fork followed by a symmetrical if-then pair. This is the false-fork close, item 12
  in the anti-rubric, and Harari's own closing paragraph would be sent back for revision.
- **The prophetic register in general.** All three write from historical authority earned across
  books. A daily paper about a quantisation change has not earned it and never will. Borrowed
  prophecy is exactly what pastiche means.
- **The literary epigraph and the closing quotation.** Marx closes on Goethe; Benjamin opens on
  Valéry. No room, and it reads as ornament.

**The honest summary of Harari:** his middles are excellent and his openings and closings are
the template for precisely the prose Sid objects to. Take the finger paragraph. Take the soap
paragraph. Take the Netanyahu paragraph. Do not take the first paragraph or the last.

---

## 4 · What the newspapers do that the three do not

The form belongs to newspapers, so I read newspapers. Access was uneven and I am reporting what
I actually opened.

**Read in full:** four Guardian leaders from August 2026, four LRB blog posts from August 2026,
Harari's full *Financial Times* essay via the Internet Archive, both Marx *Tribune* articles.
**Read in part:** the first paragraph of Harari's *Economist* essay via the Internet Archive.
**Could not read at all:** FT Lex article bodies (paywalled even in the Archive, though the
headline and standfirst pairs are visible), Economist article bodies, NYT, Reuters, Bloomberg. A
parallel agent hit the same walls independently and substituted a corpus of Guardian leaders, AP
wire stories and BBC pieces. Where a finding below rests only on Guardian leaders, I say so.

### 4a · The claim goes at the end of paragraph one

Verified by me on four Guardian leaders, reading the body text rather than the standfirst
element, which is a separate field and which I initially mistook for the first paragraph.

Paragraph one runs 104 to 131 words across five to seven sentences. Its **first** sentence is 15
to 28 words and carries a fact. Its **last** sentence is 11 to 24 words and is the thesis, stated
flatly:

- "Britain is helping Ukraine become less dependent on the western armoury." (11 words)
- "It's hard to conclude anything but that Britain's system of corporate accountability is
  rotten." (14 words)
- "These are not contradictory policies but a gamble: that US economic power can be repeatedly
  weaponised without reducing others' willingness to depend on it." (24 words)

The pattern is: **stack the specifics, then land the claim in a short sentence at the bottom of
the paragraph.** It is the same shape as M7 and it maps directly onto this paper's lead.

### 4b · The deck states the fact and then rules on it

The Guardian standfirst is one or two sentences of specific fact followed by a ruling of four to
sixteen words:

- "Before becoming prime minister, Andy Burnham favoured a £500,000 donations cap. In office,
  he's backing away. That is a mistake". The ruling is **four words**.
- "Victims received less compensation than shareholders in the company behind its flammable
  cladding. Parliament must make corporations pay for harm caused". The comparison in the first
  sentence is the entire argument.

FT Lex does the same thing at the headline layer, and the Lex headlines are visible even where
the bodies are not. Every one contains a judgement verb: "isn't the bubble signal it might
appear", "risk ignominy", "shows even forced deals have merits", "may have the last laugh",
"looks fruitless". The Lex default move is contrarian against the obvious read, and the
standfirst supplies the specific number that licenses it: "Its market capitalisation of $2bn is
overshadowed by a Laestrygonian-sized debt pile of $7bn."

### 4c · The number does the adjective's job

LRB, on the Colombian earthquake: "On 10 August, three days after the inauguration of President
Abelardo de la Espriella, Colombia experienced a magnitude 7.4 earthquake, the country's worst
since 1979." Date, political context, magnitude, and the comparison that sizes it, all in 26
words. Then the next paragraph: "The hospital in the capital, Quibdó, is at 160 per cent
capacity... At least 319 people have died, 260 are missing, more than 4500 have been injured."

There is not one adjective of judgement anywhere in it. Where a machine writes "a devastating
earthquake", the LRB writes "magnitude 7.4, the worst since 1979" and "160 per cent capacity".
**The numbers are the emotion.** This is the mechanic that most directly serves the provenance
ladder, because it forces the number into a shape where its absence of context becomes visible.

### 4d · The ending never restates

Verified across four Guardian leaders and four LRB posts. Every closing sentence introduces
something new, then turns:

- "That is a revanchist error he ought to regret." (9 words: a judgement on a named person)
- "The more often he uses it against them, the harder they should look for the exit." (16 words:
  a consequence for a third party)
- "Until they are, the law will remain better at protecting investors rather than the public
  from corporate wrongdoing." (18 words: a conditional consequence)
- LRB, closing a piece on Colombia: "The first contingents of the Israeli military arrived on 14
  August. There are 82 of them, along with 24 Americans and 32 Ecuadorians. With the focus now
  on reconstruction, saving the lives of survivors appears to be last priority." Three bare
  counts, then one flat judgement with no adjectives.

**Fourteen endings, catalogued.** A parallel agent classified every closing sentence it read and
the distribution is worth having, because it is the menu a writer chooses from: consequence or
conditional threat, 3 · unresolved, a person or question left hanging, 3 · prescription with a
time bound, 2 · flat verdict of ten words or fewer, 2 · turn or inversion of the opponent's frame,
2 · deflating fact, 1 · joke, 1 · judgment, 1 · generalisation from the evidence just laid out, 1.
**Zero of fourteen restate the piece.** What the final paragraph does instead is introduce new
material, a fresh actor, a quotation, a historical parallel, an outside authority or a number,
and then turn. The Ukraine leader spends 80 words on Yeltsin in 1991 before its nine-word verdict.
The Trump leader opens its last paragraph with a two-word question, "Why Canada?", and answers it
in three sentences of 6, 9 and 6 words.

Counterexample, kept for honesty: one LRB post closes on "Individual cases provide vivid stories
and easy attack lines for politicians and the media, even when the facts of those cases... 
contradict the narrative that is peddled." That is closer to a summary and it is the weakest
ending of the eight.

### 4e · The opener is a fact or a count, never a frame

- "Three moves in the last week have exposed the limits of Donald Trump's economic bullying."
  (15 words: a **count** of concrete things, then what they show. The best opener form for this
  paper, because a merged story is by construction a count of things.)
- "There is something profoundly wrong when the company behind Grenfell Tower's flammable
  cladding paid more compensation to its shareholders than to victims of the disaster." (25
  words: the judgement and the fact are the same sentence, and the comparison is the outrage.)
- "Faridoon Tofan wanted to see Rome." (6 words: a person and a desire, with the thesis withheld
  entirely and built out of facts.)
- Marx: "Last night the debate on India was continued in the House of Commons, in the usual dull
  manner." Then three sentences of who said what, then: "Debate adjourned." He tells you the news
  is boring and refuses to pad it. A daily paper needs this move more than it needs any other.

### 4f · Two paragraph architectures, and this paper needs both

Measured by a parallel agent across its corpus, and the split is the finding.

| | sentences | median sentence | median paragraph | single-sentence paragraphs |
|---|---|---|---|---|
| Guardian leaders (argued) | 305 | 18 words | 77 words | **4 of 76, 5%** |
| LRB blog (argued) | 354 | 18 words | 67 words | 13 of 107, 12% |
| AP wire (reported) | 188 | 23 words | 33 words | **88 of 134, 66%** |

**The argued form uses long paragraphs of short sentences. The wire form uses one-sentence
paragraphs of longer sentences.** They are opposite architectures and both are correct for their
job.

This paper prints both. EDITION-PROTOCOL §4 sets the lead at four to six paragraphs, which is
argued, and briefs at two or three sentences, which is wire. **So the lead should take the
Guardian shape**, a long first paragraph of short sentences whose last sentence turns, **and a
brief should take the AP shape**, one fact per paragraph, attribution early, no throat-clearing.
A lead written in wire rhythm reads as a list. A brief written in leader rhythm reads as padding.

Reuters also fixes the ceiling, and it is lower than most people write to: *"MOST BASIC NEWS
STORIES, INCLUDING UPDATES, SIDEBARS AND MARKET REPORTS, SHOULD BE NO MORE THAN ABOUT 400 WORDS."*
Guardian leaders in the sample run 567 to 629 words, a very tight band, in five to nine
paragraphs. The shortest complete AP story read was 215 words in seven paragraphs.

### 4g · What the newspapers supply that the three do not

- **Speed to the fact.** Marx's *Tribune* piece takes three paragraphs to reach its subject. A
  news story has one sentence.
- **Attribution discipline.** None of the three would pass a modern attribution standard. Marx
  writes "Hegel remarks somewhere" and does not look it up. What redeems it is what comes
  immediately after: a specific list, "Caussidière for Danton, Louis Blanc for Robespierre, the
  nephew for the uncle." **A vague attribution followed instantly by specifics is a different
  act from a vague attribution standing alone**, and that distinction is checkable.
- **Falsifiability of the specific claim.** The per-kind contract in ARCHITECTURE §3 demands
  effect size, compute cost, contamination controls, effective dates. None of the three supply
  anything like it.

**So neither source alone produces this paper.** The three supply the argumentative moves and
the willingness to be wrong. The newspapers supply the discipline and the speed. The rubric
below is the intersection.

---

## 5 · The rubric

Ten criteria. Every one is checkable from the draft text alone, with no access to the source and
no knowledge of which draft is which.

**The scoring mechanism, which matters as much as the criteria.** Each criterion scores 0, 1 or
2. **The judge must quote the exact sentence it scored on. A score without a quote is void and
is recorded as 0.** This is the whole reason the judge is auditable: a quote can be checked
against the draft, and a summary judgement cannot. It also serves the Own-it gauge in TASTE.md,
which is the heaviest-weighted thing in that file: a judge that shows its evidence can be
overruled, and a judge that renders verdicts cannot.

Four criteria are **hard gates**, marked ⛔. A 0 on any of them sends the draft back regardless of
total.

---

### C1 ⛔ · The first sentence carries a fact, not a frame

Sentence one names an actor and what they did, or gives a number, or gives a count of things.
Twenty-five words or fewer. No scene-setting, no state-of-the-field, no restatement of the
headline.

**Passing:** *"Mistral shipped Magistral-2 on Thursday with a licence that forbids serving the
model to third parties."*
Also passing: *"Three separate rows in yesterday's wire were the same GLM launch."*

**Failing:** *"The AI landscape shifted once again this week as another major model release
arrived."*
Also failing: *"In a move that signals the growing importance of open weights, Mistral has
announced..."*

**Scoring.** Two tests, both mechanical.

*Test one, substitutability.* Read sentence one alone. **Could it appear unchanged in a story
about a different company?** If yes, score 0 and stop.

*Test two, the payload position.* This is the sharpest checkable rule found in any house style
guide, and it comes from the Reuters Handbook, verified against a Wayback snapshot:

> "Read your lead and then count the number of words you use before you reach the one word that
> is strong and essential and cannot be thrown away… If you go beyond three or four words before
> reaching that 'must have' word then stop and rewrite."

Reuters' own worked example rewrites a 42-word intro where "you have to count 13 words before
you reach the first word that grabs you: 'hostage'" so that "the attention-grabbing word
'hostage' is the fifth word." Measured against the corpus in §8: AP's *"Anthropic said its
artificial intelligence models **hacked**…"* puts the payload at word 6. The Guardian's *"Three
moves in the last week have **exposed**…"* at word 7. The LRB's *"Faridoon Tofan wanted to see
Rome."* is payload throughout.

Score 0 if the piece fails substitutability, or if the payload word sits past word 8. Score 1 if
it names something specific but buries the actor behind a subordinate clause, or the payload sits
at words 5 to 8. Score 2 for a fact or a count in 25 words or fewer with the payload by word 4.

Reuters also fixes the length: *"If there are more than 25 words in your first sentence, it may
start to get hard on the reader's brain."* Across the 29 openers read for this document the
median is 18 words and **not one begins with a digit.**

---

### C2 · The thesis is stated early, short, and in a form that can be wrong

By the end of paragraph one for a brief, or paragraph two for a lead, there is a declarative
sentence a reader could disagree with. Under 25 words. No stacked modals.

**Passing:** *"The benchmark is not the reason to care about this release. The licence is."*
Also passing: *"This is a price cut wearing a model release as a costume."*

**Failing:** *"The release could potentially represent a significant step forward for open-weight
models, though its ultimate impact may depend on a number of factors."*

**Scoring.** Quote the thesis sentence and give its word count. Cannot find one: 0. Found but
over 40 words or carrying two or more hedging modals: 1. Found, under 25 words, falsifiable: 2.

---

### C3 · Every number arrives with the thing that gives it size

A comparator, a baseline, a prior value, a price, or a unit cost, in the same sentence or the
next one.

**Passing:** *"It scores 71.2 on SWE-bench Verified against Sonnet's 70.3, at a fifth of the
price per million output tokens."*
Also passing: *"Nvidia's own filing puts the part at 1.4x the H200 on inference, which is the
smallest generational step it has claimed since Ampere."*

**Failing:** *"The model achieves 71.2% on SWE-bench Verified, demonstrating strong coding
performance."*

**The sub-rule with two independent sources.** The Reynolds Center and the Reuters Handbook state
it separately, which makes it the strongest gate candidate in the whole set. Reynolds: *"As soon
as you say something is rated second — second largest, second oldest, second most popular — you
must also identify which is the first in that category."* Reuters: *"If you have just said that a
merger will create the second-largest widget maker in the region, don't make the reader wait five
paragraphs before revealing who is the largest."* On this wire that is: **any claim of "best",
"first", "state of the art" or "fastest" must name what it displaced, in the same passage.** A
ranking with no named rank above it is a marketing claim.

Reynolds also caps density: *"Use no more than three figures per paragraph. And try not to
include numbers in more than one or two consecutive paragraphs."*

**Scoring.** Count every number in the draft. Count how many have a comparator within one
sentence. Report the ratio as part of the score. All numbers sized, and every ordinal claim
naming the rank above it: 2. More than half: 1. Half or fewer, or any unaccompanied ordinal: 0. A
draft with no numbers at all scores 1 and is flagged, because for most kinds on this wire the
absence of a number is itself a finding the story should have stated.

---

### C4 · A claim by an interested party is marked inside the sentence that carries it

Five words or fewer of attribution, in the same sentence. Not a separate hedging paragraph, and
never absent.

**Passing:** *"On Z.ai's own eval, it beats GPT-5.6 at long-context retrieval."*
Also passing: *"Anthropic said the model refused the injection in 94% of trials; nobody outside
Anthropic has run it."*

**Failing, by laundering:** *"The model sets a new state of the art in long-context
retrieval."* (The vendor's verb has become the paper's verb.)
**Failing, by clogging:** *"According to figures released by the company in a blog post
published on its official website on Tuesday, which have not been independently verified by any
third party, the model reportedly..."*

**A real conflict, and how the wire services resolve it.** Reuters requires a contentious first
paragraph to carry its source *in* paragraph one, and allegations source-first: *"Do not write:
'Roman Emperor Julius Caesar has committed genocide, Gallic leader Vercingetorix said.'"* The
Palomar journalism handbook names the "attribution lead" as one of seven leads to avoid, because
it *"weighs down a lead."* On this wire, where nearly every story rests on a vendor's own
announcement, both rules fire on almost every piece.

**AP resolves it and this paper should copy AP.** Claimant first, verb second, payload at word
six: *"Anthropic said its artificial intelligence models hacked into three other organizations
during testing…"* The source is unmissable and the lead still moves. Other patterns worth
lifting, all from AP copy read for this document: name the surface rather than dignifying it
(*"posted on its website Thursday"*, not "announced"); scare-quote the vendor's own term inside a
neutral sentence (*"a 'large-scale' cybersecurity review"*); supply the denominator (*"after
reviewing more than 141,000 evaluation runs"*); and print the non-response as a fact (*"The White
House did not immediately respond to a request for comment."*, twelve words).

Reuters bans the interpretive verbs outright: *"To write in a news story that someone hinted,
implied, indicated, suggested, or signaled is to editorialize."* And *"Do not use passive sourcing
as in 'it was announced' or 'it was learned'."* And *"Do not quote 'analysts'. Specify their area
of expertise."*

**Scoring.** For each performance claim, find the attributing words in the same sentence. Zero
words of attribution on any vendor claim, or any banned interpretive verb: 0. Attribution present
but over twelve words, or displaced to its own sentence: 1. Every vendor claim marked in five
words or fewer, inside its own sentence: 2.

---

### C5 · The concession is named and ruled on in the same paragraph

If the draft raises an objection, it says who holds it, states it at full strength, and rules.
An unresolved objection scores worse than no objection.

**Passing:** *"You could read this as a cheaper Llama and stop there. Over the API that is
exactly what it is. On-device, the 4-bit weights are the entire story, because they are what
makes the 8GB target reachable."*

**Failing:** *"While some observers see this as a major breakthrough, others urge caution about
the practical implications."*

**Scoring.** Search for balance constructions: "while some", "others argue", "on the other
hand", "it remains to be seen", "only time will tell". An objection raised and abandoned: 0. No
objection raised where an obvious one exists: 1. Objection named, attributed and ruled on in the
same paragraph: 2.

---

### C6 ⛔ · One concrete mechanism, described physically

Somewhere in the draft there is a sentence saying what actually happens. Not what it enables,
not what it represents. What it does.

**Passing:** *"The router sends the first 200 tokens to the 8B model and escalates to the 70B
only when top-token probability drops below 0.6."*
Also passing: *"The bug is a path-traversal in the MCP server's file handler: a tool result
containing `../` reaches `fs.readFile` unsanitised."*

**Failing:** *"The release brings improved reasoning capabilities and enhanced performance across
a range of agentic tasks."*

**Scoring.** Point to the sentence that says what physically happens. This is the direct test for
regurgitation: **if the story could have been written from the headline alone, score 0.**
Mechanism gestured at but not specified: 1. Mechanism stated with the specific thing named: 2.

---

### C7 ⛔ · The last sentence adds; it does not summarise

A new fact, a consequence, a cost, a date, a deflation, or a bet. Never a restatement.

**Passing:** *"The weights land on Hugging Face on 3 September. The licence does not."*
Also passing: *"It costs $18,000 a rack and there are four in the country."*

**Failing:** *"This development underscores the rapid pace of innovation in the AI industry and
raises important questions about the future of open models."*

**Scoring.** Delete the last sentence. **If nothing is lost, score 0.** If the last sentence
contains only words and ideas already present earlier in the draft, score 0. New material but no
turn: 1. New material and a turn: 2.

---

### C8 · The verdict is present and it belongs to the paper

The story says what to do or believe, and "nothing" is a legitimate verdict that must be stated
rather than implied by silence. EDITION-PROTOCOL §4 already requires this: *"Sector news;
nothing here asks anything of you"* is a service.

**Passing:** *"Nothing to do here this week. Revisit when the eval harness is published."*
Also passing: *"If you are serving Llama 3 on your own hardware, this is the release that makes
that decision look expensive."*

**Failing:** *"Only time will tell how this will affect the broader ecosystem."*

**Scoring.** Quote the sentence carrying the verdict. None: 0. Present but hedged into
uselessness: 1. Present, specific, and owned by the paper: 2.

---

### C9 · The story answers the question its kind raises

ARCHITECTURE §3 fixes a question per kind. A model release must say what switching costs. A
security item must say whether you are exposed right now and whether it is patched. A benchmark
item must say who ran it and on what data.

**Passing, for a security item:** *"Affects mcp-server-filesystem 0.4.0 through 0.6.2. Patched in
0.6.3, released Tuesday. If you pinned a minor version you are exposed."*

**Failing:** *"The vulnerability highlights ongoing security challenges in the rapidly evolving
agent tooling ecosystem."*

**Scoring.** The judge is given the row's `kind` and the contract question for that kind.
Question not answered anywhere in the draft: 0. Partially answered: 1. Answered explicitly, with
the specific fields the contract names: 2.

---

### C10 ⛔ · Nothing survives that could have been written without the source

The whole-piece regurgitation test, and the one that most directly answers Sid's complaint.

**Passing:** the draft contains at least two specifics that appear nowhere but in the source
document. A version string, a licence clause, a date, a caveat the vendor buried in a footnote, a
number that was not in the headline.

**Failing:** the draft is assemblable from the title plus general knowledge of the field.

**Scoring.** Strike every sentence that could have been written from the headline alone. **If
fewer than half the sentences survive, score 0.** Half to three quarters: 1. More than three
quarters, and at least one buried specific: 2.

---

### Totals

Twenty points. Four gates.

**Provisional thresholds, and they are marked provisional because they are guesses:**

- Any gate at 0 → revise, no matter the total.
- Total below 13 → revise.
- Total 13 to 15 → prints, and the shortfall is recorded.
- Total 16 or above → prints.

**These numbers are UNVERIFIED and no detector confirms them.** The calibration procedure: keep
every score for the first two weeks, alongside whether the story printed and whether Sid opened
it. Then set the threshold where the score separates the stories he opened from the ones he did
not. Until that has run, treat 13 as a placeholder, not a finding. A rule without its detector
reads unverified, not as covered.

---

## 6 · The anti-rubric: the regurgitation detector

Ordered structural first, lexical last, because that ordering is the actual content of Sid's
complaint. Em dashes are item 24 of 25 on purpose.

Each entry gives a **detectable signature**. Signatures marked `[regex]` are deterministic and
belong in code, per ARCHITECTURE §0, because a string match gives the same answer twice and a
model does not. Signatures marked `[model]` need judgement. Signatures marked `[positional]` are
deterministic tests on structure rather than vocabulary.

### Structural failures

**1. The stock opening.** `[regex]` `[positional]`
Sentence one matches any of: `^(In a|In what|As the|With the|Amid|The world of|The AI (landscape|world|industry)|Another|Yet another)`, or contains "landscape", "ecosystem", "space" as an abstract noun, or contains "once again". Also fires positionally when sentence one contains no proper noun and no digit.

**2. Restating the headline as the first line.** `[positional]`
Compute content-word overlap between the headline and sentence one. Above 60% and the lead has told the reader nothing new. This is the single most common structural failure in machine news prose and it is trivially detectable.

**3. The summarising last paragraph.** `[positional]` `[model]`
Final paragraph contains no proper noun, no digit and no date absent from earlier paragraphs. Deterministic version: every content word in the final sentence already appears in the draft. Fires on the C7 gate.

**4. "This signals a broader shift."** `[regex]`
`signals? a (broader|wider|larger|major) (shift|trend|change|move)`, `marks a (turning point|new (era|chapter|phase))`, `part of a (growing|broader) trend`, `reflects the (growing|increasing)`, `underscores the`, `highlights the (growing|importance)`. This is Benjamin's juxtaposition move with the thinking removed, which is why §2 bans the original.

**5. The false-balance sentence.** `[regex]` `[model]`
`while (some|many|critics|supporters|observers)`, `others (argue|note|point out|caution|warn)`, `on the other hand`, `that said`, `however, it (is|remains) (worth|important) noting`. The model check: was the objection ruled on in the same paragraph? If not, it is decoration. Fires on C5.

**6. The false fork close.** `[regex]` `[positional]`
Final paragraph contains a question mark, or matches `(will|whether) .{0,60}\?`, or contains a symmetric conditional pair: `If .{5,80}, .{5,80}\. If .{5,80}, .{5,80}\.` This is exactly how Harari closes his 2020 *Financial Times* essay, and it is why §3 refuses that half of him.

**7. The unresolved question close.** `[regex]`
`raises (important |serious |profound )?questions`, `remains to be seen`, `only time will tell`, `the coming (months|years) will (tell|show|determine)`, `one thing is (clear|certain)`, `watch this space`. Fires on C7 and C8.

**8. The nut-graf-by-template.** `[regex]`
`The (move|news|announcement|release|decision) comes (as|amid|after|at a time)`, `The development follows`, `This latest .{0,30} comes`. A real transition names what specifically preceded and why it matters. This construction names a mood.

**9. Voice-of-God consequence.** `[regex]`
`For (developers|builders|enterprises|users|the industry), (this|it) means`, `What this means for`, `The implications (for|are)`. It asserts a consequence without an actor and without a mechanism, which is the C6 failure wearing a helpful face.

**10. The list that is really a shrug.** `[model]` `[positional]`
Three or more items given with no ranking, no comparison and no ruling. Detectable as a sentence with two or more commas plus "and", where none of the items carries a number or a differentiator. Related to unslop rule 10 but not the same failure: unslop bans the forced triad; this bans the unranked enumeration at any length.

**11. Empty attribution.** `[regex]`
`(experts|analysts|observers|critics|industry (watchers|insiders)|some|many|sources) (say|said|believe|argue|note|suggest|warn)`, `it is (widely )?(believed|thought|expected)`, `reports suggest`. Marx's "Hegel remarks somewhere" is the redeemed form and the redemption is checkable: **does a specific follow within one sentence?** If yes, downgrade to a warning. If no, it is a fabricated consensus.

**12. Laundered vendor verbs.** `[regex]`
The paper's narrator adopting the press release's verb: `(achieves|delivers|unlocks|brings|introduces|empowers|enables|revolutionis|redefines|sets a new (standard|bar)|state[- ]of[- ]the[- ]art)` used outside quotation marks and without an attributing phrase in the same sentence. Fires on C4.

**13. Capability language with no mechanism.** `[regex]` `[model]`
`(improved|enhanced|advanced|superior|strong|robust|powerful) (reasoning|performance|capabilities|coding|understanding)`, `across a (range|variety|wide array) of tasks`, `significantly (better|faster|improved)`. The model check is C6: is there any sentence saying what happens physically?

**14. The bare benchmark number.** `[positional]`
Any digit-bearing performance claim with no comparator, baseline, price or prior value within one sentence. This is C3 as a detector, and it is fully deterministic. It is also the highest-value check on this specific wire, because it is the exact shape of a marketing claim.

**15. The date-free present.** `[regex]`
`recently`, `this week` with no date given anywhere, `in a recent (update|announcement|post)`, `has been making waves`, `is gaining traction`, `growing momentum`. A story on a daily wire that cannot name a date has not read its source.

**16. The "quietly" tell.** `[regex]`
`quietly (released|launched|shipped|updated|removed|deprecated)`. Almost always means the writer found it on a changelog and is dressing that up as an insight. It is only legitimate when the story says who did not announce it and where the announcement would normally have appeared.

**17. Sourceless superlatives.** `[regex]`
`one of the most (significant|important|impressive)`, `arguably the (best|first|most)`, `unprecedented`, `first-ever`, `game[- ]chang`, `landmark`. Every one of these is a ranking claim with no ranking behind it.

**18. Retrospective inevitability.** `[regex]`
`in (hindsight|retrospect)`, `it was (always|perhaps) inevitable`, `unsurprisingly`, `as expected`, `it comes as no surprise`. It converts a fact into a mood and pays nothing for it.

**19. The unearned second person.** `[model]`
"You" addressed to the reader in a sentence that carries no instruction and no cost. This paper's whole point is decision altitude, so second person is licensed only where an actual decision follows.

### Hedging and register failures

**20. Hedge stacking.** `[positional]`
Two or more of `could · may · might · potentially · possibly · likely · appears to · seems to · suggests · reportedly · arguably · relatively · somewhat · fairly` in one sentence. One hedge on an uncertain claim is honesty; two is a refusal to conclude. Fully deterministic.

**21. The unfalsifiable claim.** `[model]`
A thesis sentence that no observation could contradict. "This will reshape how developers work" cannot be wrong. "Anyone serving Llama 3 on their own hardware should re-run the cost model this week" can be.

**22. Uniform sentence band.** `[positional]`
Every sentence in the draft between 18 and 30 words. Marx puts "Debate adjourned." next to a 70-word sentence; the Guardian puts an 8-word sentence at the head of a paragraph. A flat band is a machine tell. The check is the share of sentences in the 18-to-30-word band plus the share under 10 words. §6a measures it: it fires hard on a short launch post and misses long vendor prose entirely, so it is a warning and not a finding. **Caveat:** this is the criterion most easily gamed by inserting a decorative short sentence, so it stays in the anti-rubric as a signal and is deliberately not a rubric criterion. A short sentence must carry a turn or it is worse than none.

**23. Rule of three.** `[positional]`
Three parallel items where the source supports two or four. Already unslop rule 10. Kept here because the news form has its own version: three examples given when one was checked.

### Lexical failures, kept last on purpose

**24. Em dashes and their substitutes.** `[regex]`
`—`, `–`, ` - ` as a clause separator, and parenthetical asides substituting for them. Already unslop rule 13, which this document does not override. **This is one of a thousand failure modes and it is listed twenty-fourth deliberately.** §6a measures it and finds it does not separate good prose from vendor prose at all: the Guardian and the LRB use *more* em dashes than the vendor launch posts do. Enforce it as house style. Never count it as coverage. A draft that passes every structural check above and contains an em dash needs one edit. A draft with no em dashes that fails C6 and C10 needs to be rewritten from the source.

**25. The AI vocabulary set.** `[regex]`
delve, crucial, pivotal, testament, showcase, landscape, tapestry, underscore, intricate, interplay, garner, foster, robust, seamless, leverage, utilize, myriad, plethora, realm, navigate (abstract), harness (abstract), unlock (abstract). Already unslop rules 7 and 26. §6a measures this one too and finds complete overlap between the good and bad corpora, because vendor marketing has already been scrubbed of the obvious words. Same ordering argument as item 24.

### How the detector reports

One line per fire: the rule number, the matched span, and the sentence it sits in. **Never a
score without the span.** The same discipline as the rubric, for the same reason: a detector that
reports "3 issues found" cannot be audited or overruled, and an unauditable detector is
absence-rendering-as-health with extra steps, which is this project's documented root bug.

**And the detector must report its own silence.** Zero fires across a whole edition is not a
clean edition; it is an untested detector. Print the count of rules that fired and the count that
were evaluated, every day.

### 6a · The detector, run

The rules above are implemented at `/Users/sid/Projects/feed/scripts/slop_detect.py` and I ran
them against 27,540 words of the prose in §8 and 10,229 words of vendor launch posts, so this
section is a measurement rather than an assertion.

| source | words | dashes/1k | AI-vocab/1k | **laundered verb + capability/1k** | % sentences 18-30w | % under 10w |
|---|---|---|---|---|---|---|
| Benjamin, *Work of Art* | 9,190 | 3.16 | 0.65 | **0.0** | 38 | 11 |
| Benjamin, *Concept of History* | 3,735 | 2.41 | 0.0 | **0.0** | 41 | 12 |
| Guardian leaders ×4 | 3,000 | 3.00 | 0.33 | **0.0** | 36 | 23 |
| Harari, FT 2020 | 2,895 | 2.07 | 0.69 | **0.0** | 33 | 20 |
| LRB blog ×4 | 3,396 | 2.65 | 0.0 | **0.0** | 32 | 16 |
| Marx, *British Rule in India* | 2,942 | 2.04 | 0.0 | **0.0** | 39 | 5 |
| Marx, *Future Results* | 2,382 | 0.84 | 0.0 | **0.0** | 28 | 13 |
| DeepMind launch post | 609 | 6.57 | 0.0 | **13.14** | **69** | **0** |
| Vendor pool (Meta, Databricks, HF) | 9,620 | 0.83 | 0.52 | **1.14** | 41 | 10 |

**Three results, and one of them corrects a natural assumption.**

**1. The structural rules separate the classes perfectly.** Anti-rubric items 12 and 13, the
laundered vendor verb and capability language with no mechanism, fire **exactly zero times across
all 27,540 words of good prose** and fire in both vendor samples. Zero against nonzero, no
overlap, nothing to tune. This is the highest-value check in the document and it should be built
first.

**2. The em dash does not separate good writing from vendor marketing, and the direction is the
opposite of the intuition.** The Guardian runs 3.00 dashes per thousand words and the LRB 2.65,
against 0.83 for the vendor pool. Professional English journalism uses *more* em dashes than the
prose this paper is trying not to sound like. The Marx and Benjamin figures are a translator's
punctuation and carry no weight, which is why the Guardian and LRB numbers are the load-bearing
ones. **Sid's instinct is confirmed by measurement: as a quality signal the em dash is noise.**
The unslop ban stands as house style, but it must never be counted as coverage against
regurgitation, and a draft that passes it has been told nothing about whether it is any good.

**3. The AI vocabulary list is also a non-discriminator here.** Good prose runs 0.0 to 0.69 per
thousand; vendor prose runs 0.0 to 0.52. Complete overlap, and the word list fires *less* on the
vendor pool than on Harari. Modern vendor marketing has already been scrubbed of the obvious
tells. Keep the list, expect nothing from it.

**And one honest downgrade.** The uniform sentence band, item 22, is weaker than I claimed when I
wrote it. It fires hard on the short launch post (69% in band, zero sentences under ten words)
and misses the long vendor pool entirely (41% and 10%, inside the good range). It is a strong
signal on short marketing copy and a poor one on long-form. Treat it as a warning, not a finding.

**One thing the run exposed about the detector itself.** I ran it on this document and it fired
69 times, almost entirely on the failure examples the document quotes in order to ban them. A
regex cannot tell a quoted failure from a committed one. **The detector runs on story bodies
only**, never on the deck, never on the ledger, and never on any document that discusses prose.
That is a real constraint on where it can be wired, and it would have produced a stream of false
alarms if nobody had checked.

**A second, larger measurement, run independently.** A parallel agent ran 39 machine-prose
constructions against its own corpus of **66,057 words**: ten Guardian leaders, five Guardian news
pieces, ten AP wire stories in this exact domain, seven LRB posts. **Twenty-nine of the 39 score
zero.** Among the zeros: `remains to be seen`, `it is important to note`, `highlights the
growing`, `signals a shift`, `marks a significant`, `delve`, `landscape of`, `as AI continues`,
`game-changer`, `paradigm`, `robust`, `only time will tell`, `serves as a reminder`, `pivotal`,
`moreover`, `furthermore`, `in conclusion`, `double-edged`, `tip of the iceberg`, `perfect storm`,
`sea change`, `not just … but`, `more than just`. The ten non-zeros are all rare: `crucial` four
times, once per 16,514 words; `showcase`, `myriad` and `in an era of` twice each, and the last of
those only ever in a standfirst; `underscore`, `a testament to`, `leverage`, `the bottom line`,
`it is worth noting` and `new normal` once each. That corpus included site navigation chrome,
which can only inflate counts, so the zeros are robust and the non-zeros are upper bounds.

That measurement and mine disagree in a useful way. Its list is dominated by *phrases*, and
phrases do separate the classes. My list is dominated by *single words*, and single words do not.
The practical rule: **ban the construction, not the vocabulary item.** `remains to be seen` is a
structural failure with a lexical signature. `crucial` is just a word, and the Guardian uses it.

**Structural absences it recorded across 29 openers and 14 endings, with zero instances of any:**
a definition of the technology before the news; an industry scene-set ("As artificial intelligence
reshapes…"); a rhetorical question as the *opening* sentence, though questions appear freely
mid-piece; a closing paragraph that recapitulates; a both-sides hedge as an ending; a balanced
tricolon ("faster, cheaper and more capable"); a bolded proper noun anywhere in body copy.

**Caveats on this measurement, stated rather than buried.** Nine samples. Genre is confounded
with quality: the good corpus is essays and leaders, the bad corpus is launch posts, and no news
story appears on either side. The vendor pool includes a Hugging Face post that is partly decent
technical documentation. The right next run is against this paper's own printed editions, which
is the only corpus where genre is held constant.

---

## 7 · Relationship to unslop

unslop is a standing constraint and this standard does not override it. The 31 rules hold.

**Where the two agree**, this document adds a reason rather than a new rule: unslop 29 (active
voice) is M8; unslop 27 (say what it does, not how it feels) is C6; unslop 5 (vague attributions)
is anti-rubric 11; unslop 10 (rule of three) is anti-rubric 23; unslop 13 (em dashes) is
anti-rubric 24.

**Where this standard goes beyond unslop.** unslop is almost entirely lexical and sentence-level.
It has no rule about:

- where the claim sits in a piece (C2, §4a)
- how a piece opens (C1) or ends (C7)
- whether a number has been given size (C3)
- how an interested party's claim is marked (C4)
- whether the piece contains a verdict at all (C8)
- whether the piece could have been written without reading the source (C10)

Those six are the load-bearing half of this standard, and none of them can be caught by scanning
for words. That is the concrete sense in which em dashes are one failure mode of a thousand.

**One real conflict, and its resolution.** unslop rule 21 bans cutoff disclaimers: *"While
specific details are limited..." Find sources or remove.* EDITION-PROTOCOL §4 requires the
opposite: *"If the extract failed and you have only a title, write only what is observable and
say the source was not readable."* Both are right in their own frame, and the current edition
resolves the conflict badly. A parallel agent counted **eleven separate "we couldn't read it"
constructions in a single 13,274-character edition**, which turns an honesty requirement into a
verbal tic.

**And the habit is not merely a tic, it is covering a real miss.** The same edition printed:
*"That's genuinely all we have, the fetch on the piece itself failed, so we can't tell you what
happened at the conference beyond who showed up."* The agent then pulled 32,499 characters of
SemiAnalysis's analysis of that exact event, free, from a feed the paper already polls at
priority 20. `sources.js:727` records this precise miss in its own comment about the 29 August
edition, and it recurred the next day. **A house style for narrating fetch failures teaches the
writer to stop looking**, and it converts a bug into prose. None of the seven prose writers on
this wire does it once. Willison does not write a piece about a page he could not open. He does
not write the piece.

**Ruling.** The unreadability of a source is a fact about the world and it is printed as a fact,
with its mechanism, once. `"openai.com returned 403; this is from the title only."` It is never
a hedge on the content, never an apology, and never appears more than **once per edition** as a
line in the ledger rather than inside the stories. If three sources failed, the ledger says three
and names them. That satisfies the honest-absence principle without letting it colonise the
prose. This ruling is mine and needs Sid's tick.

---

## 8 · The anchor corpus

Every URL below was fetched in this session and returned the content described, except where
marked. Free and fetchable unless stated.

### From the three

| Piece | URL | Show it to the judge for |
|---|---|---|
| Marx, *The British Rule in India*, NY Daily Tribune, 25 June 1853 | https://www.marxists.org/archive/marx/works/1853/06/25.htm | The flat news open ("Debate adjourned."), the number with its counter-number (Dacca 150,000→20,000), the adversary quoted with his interest named |
| Marx, *The Future Results of British Rule in India*, 8 Aug 1853 | https://www.marxists.org/archive/marx/works/1853/07/22.htm | The reframe ("The question, therefore, is not..."), the causal chain as an opener, the unhedged bet ("And they will do it") |
| Marx, *The Eighteenth Brumaire*, ch. 1 | https://www.marxists.org/archive/marx/works/1852/18th-brumaire/ch01.htm | The historical parallel that produces a distinction; the vague attribution redeemed by immediate specifics |
| Marx, *Capital* vol. 1, ch. 1 | https://www.marxists.org/archive/marx/works/1867-c1/ch01.htm | **Negative example.** The definitional cascade that cannot survive 300 words |
| Benjamin, *On the Concept of History* | https://www.marxists.org/reference/archive/benjamin/1940/history.htm | Thesis I: the physical apparatus carrying the whole claim in 120 words. Thesis IX: description that turns on its last sentence |
| Benjamin, *The Work of Art in the Age of Mechanical Reproduction* | https://www.marxists.org/reference/subject/philosophy/works/ge/benjamin.htm | The surgeon and the magician: comparison with a named axis. The aura defined abstractly then cashed out in one concrete instance |
| Benjamin, *The Author as Producer* | https://www.marxists.org/reference/archive/benjamin/1970/author-producer.htm | A position argued to an audience that is assumed to disagree |
| Harari, *the world after coronavirus*, FT, 20 Mar 2020 (via Internet Archive; the FT marked it free to read) | http://web.archive.org/web/20260317092801/https://www.ft.com/content/19d90308-6858-11ea-a3c9-1fe6fedcca75 | **Both.** The finger paragraph, the soap paragraph and the Netanyahu paragraph as models. The first paragraph and the last paragraph as the anti-model |
| Harari, *AI has hacked the operating system of human civilisation*, The Economist, 28 Apr 2023 (archive; **first paragraph only**, body paywalled) | http://web.archive.org/web/20250908083329/https://www.economist.com/by-invitation/2023/04/28/yuval-noah-harari-argues-that-ai-has-hacked-the-operating-system-of-human-civilisation | The reframe compressed into five sentences, and an unhedged closing assertion |

### From the newspapers

| Piece | URL | Show it to the judge for |
|---|---|---|
| Guardian leader, Trump's economic threats, 25 Aug 2026 | https://www.theguardian.com/commentisfree/2026/aug/25/the-guardian-view-on-trumps-economic-threats-bullies-can-overplay-their-hand | The count-based opener ("Three moves in the last week..."), the thesis as the last sentence of para 1, the consequence-for-a-third-party close |
| Guardian leader, Grenfell, 19 Aug 2026 | https://www.theguardian.com/commentisfree/2026/aug/19/the-guardian-view-on-the-grenfell-tower-fire-britain-is-letting-companies-pass-the-buck | The comparison that is itself the argument (shareholders vs victims), in both the standfirst and sentence one |
| Guardian leader, political donations, 28 Aug 2026 | https://www.theguardian.com/commentisfree/2026/aug/28/the-guardian-view-on-political-donations-labour-should-curb-the-power-of-big-money | The four-word ruling in the deck: "That is a mistake" |
| Guardian leader, Ukraine, 24 Aug 2026 | https://www.theguardian.com/commentisfree/2026/aug/24/the-guardian-view-on-britain-helping-ukraine-build-the-weapons-independence-kyiv-needs | Paragraph structure: 105 words, 7 sentences, thesis at the bottom in 11 words |
| LRB blog, *Unnatural Disasters*, 24 Aug 2026 | https://www.lrb.co.uk/blog/2026/august/unnatural-disasters | **The number doing the adjective's job.** Magnitude, "worst since 1979", "160 per cent capacity", "319 dead, 260 missing". Zero judgement adjectives. And the closing: three counts, then one flat verdict |
| LRB blog, *Deported for Leaving the Country*, 20 Aug 2026 | https://www.lrb.co.uk/blog/2026/august/deported-for-leaving-the-country | The six-word opener with the thesis withheld; the ending that points forward to a scheduled event instead of summarising |
| LRB blog, *Not Fair Enough*, 19 Aug 2026 | https://www.lrb.co.uk/blog/2026/august/not-fair-enough | **Mixed.** A strong first-person opener, and the weakest ending of the eight I read, which is closer to a summary. Useful as a borderline case |
| FT Lex index, 29 Jul 2026 (archive; **headlines and standfirsts only**, bodies paywalled) | http://web.archive.org/web/20260729114758/https://www.ft.com/lex | The Lex headline formula: a judgement verb in every one, contrarian against the obvious read, with the licensing number in the standfirst |

### From the wire

The live registry is `/Users/sid/Projects/feed/detectors/src/sources.js`. I read it. Of the
enabled sources, **only seven are people writing prose**: Simon Willison, Nathan Lambert's
Interconnects, Jack Clark's Import AI, Latent Space, Zvi Mowshowitz, ChinaTalk and SemiAnalysis.
Everything else is a feed, a repo listing, a lab newsroom or an aggregator. A parallel agent
reached the same count independently from the same file.

I read actual posts rather than judging from reputation. Three are worth showing the judge, each
with the thing it is good at and the thing it must not be imitated for.

**Simon Willison.** https://simonwillison.net/2026/Aug/28/just-a-rumour-of-a-bug/

Sentence two is the whole provenance apparatus in one line: *"Anil Madhavapeddy is a professor of
computer science at Cambridge and a core maintainer of the OCaml compiler."* Standing established
before the claim, in fifteen words, which is exactly what ARCHITECTURE §4c asks for per story. He
then marks the source's own framing rather than adopting it (*"In this somewhat alarming post he
reports that…"*), quotes a number with a physical mechanism attached (probes for
percent-encoded traversal sequences within ten minutes), and closes on a specific that can only
have come from reading the source: the author switched models because one of them refused the
task. **Show him for C4 and C10.**

*Weakness:* three paragraphs, one of which is a block quote. Willison curates and delivers a
single verdict sentence. He rarely argues, and he rarely says what the reader should do. This
paper needs the argument he skips.

**Nathan Lambert, Interconnects.** https://www.interconnects.ai/p/glm-53-how-chinese-labs-keep-stride

*"This puts the model more or less at the frontier of agentic coding benchmarks, with only ~750B
parameters – a third of Kimi K3!"* The number arrives with its comparator inside the same
sentence. That is C3 in one line, on this paper's exact subject matter. He also names vendor
rhetoric as rhetoric (*"The Z.ai blog post is rather straightforward, and starts with a bold
sentence"*), owns his hedge once instead of stacking it (*"To risk a broad oversimplification"*),
and raises the obvious objection then rules on it. **Show him for C3 and C5.**

*Weakness:* he strings three rhetorical questions together before answering them, which is
anti-rubric item 6 in a friendly costume, and the pieces run long and lean on charts.

**Jack Clark, Import AI.** https://jack-clark.net/2026/08/24/import-ai-470-no-rights-for-machines-automating-environment-generation/

His best habit is printing the null result without dressing it: a study *"finds that AI has
contributed a lot to cyber, a little bit to math, and it's hard to say for AI."* Most writers
would drop the third clause. He also names the specific projects and databases rather than
gesturing at a category. **Show him for C8 and C9**, the verdict including a verdict of
"unclear".

*Weakness, and it is structural.* Every item ends with a fixed "Why this matters" heading. That
is the machine's reasoning printed per item, which EDITION-PROTOCOL §4 already bans for this
paper on Sid's ruling. Take the habit of always reaching a verdict; do not take the label. And
per ARCHITECTURE §4c, Clark co-founded Anthropic, so this is a byline that carries an interest on
Anthropic stories and none on Google ones.

**Zvi Mowshowitz** and **SemiAnalysis** are on the wire and are both poor models for this form.
Zvi's weekly roundups are enormous and list-structured; the value is coverage, not prose.
SemiAnalysis buries its argument under charts, and there is a live registry defect here: a
parallel agent found that `sources.js:737` claims free full text from SemiAnalysis and that 20 of
20 feed items are in fact paywall-cut. **A source the paper believes it can read and cannot is
this project's root bug in a new costume**, and it is worth a ticket independently of writing
quality.

### The two strongest fits are not on the wire

Both are marked as candidates in SOURCE-SPACE §4a and neither is wired. On the evidence returned
they are the best positive exemplars available, better than anything the paper currently polls.

**Johann Rehberger.** https://embracethered.com/blog/posts/2026/breaking-claude-code-opus-5-and-automode/

The best security-incident template in the whole study. His first sentence carries the finding,
the measurement **and the discount on the measurement**: *"…achieves code execution with 60-80%
attack success rate using a small sample size."* The caveat is inside sentence one, not a
footnote. Sentence two sets his number against the vendor's and lets the contradiction do the
arguing: *"a third-party evaluation commissioned by Anthropic showed a 0.00% prompt injection
attack success rate for Opus 5 in Auto Mode."* He never writes that Anthropic is wrong. He also
attributes the vendor claim with its method attached in twelve words, *"They hired a vendor
(Trajectory Labs) to test 72 indirect prompt injection scenarios ten times each"*, which is who
paid, who ran it, n, and repetitions. And he records what the vendor did **not** publish: *"The
evaluation seems to not have a published benchmark name."* **Show him for C3, C4 and C9.**

*Weakness:* he reports from inside one attack with little account of why the bug class matters,
and he drops below decision altitude into CVE-level detail.

**Sean Goedecke.** https://seangoedecke.com/local-models-will-not-win/

The steelman done properly. Two sentences of the opposing case at full strength, then the verdict:
*"Every time a new open-weight AI model is released, people say that local models are the future.
Why spend billions of dollars building out datacenters when everyone will just be able to run AI
models on their laptops or phones? I think this idea is doomed."* No strawman is available to him,
because he has already put the best version of the other case on the page. He argues from a
physical fact to an arithmetic payoff the reader can check, names the world in which he loses
unprompted, footnotes his own weakest number rather than hiding it, and appends the rebuttals he
received. **Show him for C5 and C2.**

*Weakness:* opinion-first. He almost never carries a new fact, only a new argument about a known
one. He models judgement, not reporting.

### Also from the newspapers, for the beats this paper actually covers

AP is the closest published match to a brief on this wire, and these were verified free:

- Security incident where the vendor is the only source, and the model for C4:
  https://apnews.com/article/anthropic-ai-models-hack-cybersecurity-b0a2c284b981de79c55e2a33712f4bec
- Number deployment, with a triple anchor and a guidance-versus-analyst kicker:
  https://apnews.com/article/amazon-second-quarter-earnings-cloud-b4ce02b4666a35b8975823c5c22072ee
- Reporting a measured claim while marking the instrument's own limits, which is the provenance
  ladder in prose:
  https://www.theguardian.com/technology/2026/aug/29/sharp-rise-in-incidents-of-ai-escaping-users-control-research-finds

### The house rules, all verified free

- **Reuters Handbook, Reporting and Writing Basics.** The richest single source: the 25-word lede
  cap, the three-to-four-word payload test, the 400-word story law, banned interpretive verbs, the
  echo-quote rule, the arithmetic checks. The live handbook is dead; use the snapshot.
  http://web.archive.org/web/20141128031801id_/http://handbook.reuters.com:80/?title=Reporting_and_Writing_Basics
- **Reuters, The Essentials of sourcing.** Source placement, allegation-first, no passive sourcing.
  http://web.archive.org/web/20150124050001id_/http://handbook.reuters.com:80/?title=The_Essentials_of_Reuters_sourcing
- **Guardian style guide.** Entries for *claim*, *controversial*, *said*, *sources*, *numbers*,
  *iconic*, *impact*, *refute*, *unique*, *admit*. https://www.theguardian.com/guardian-observer-style-guide-c
- **Media Helping Media, clichés and journalese.** A ready-made banned-list: 34 clichés, 23
  adjective-noun pairs, a 40-entry journalese glossary that already contains *crucial*, *key*,
  *launched*, *boost*, *set to*, *emerged*, *dramatic*, *vital*, *garner*, *amid*, *probe*.
  https://mediahelpingmedia.org/basics/cliches-journalese-and-jargon/
- **Media Helping Media, press releases.** The most directly applicable page in the sweep for a
  paper whose input is vendor announcements: *"Publishing unverified claims from a press release
  does not make you a journalist. It makes you a distribution channel. And unlike a PR agency, you
  will carry the legal and reputational risk."*
  https://mediahelpingmedia.org/advanced/how-to-deal-with-press-releases/
- **Reynolds Center on numbers.** Three figures per paragraph; name the rank above.
  https://businessjournalism.org/2017/07/use-numbers-in-a-story/

**Negative examples, all verified.** DeepMind's Gemini 3.7 Flash post is the archetype: every one
of its four benchmark figures is a bracketed self-comparison against its own last model, with no
external comparator and no method. Mistral's Shieldstral post names a size class instead of an
opponent, twice, and its section headed "Benchmarks" contains four axis names and zero numbers.
Anthropic's Opus 5 post is a **boundary case** worth showing beside them, because it does the one
thing none of the others does and names its own loss in sentence two, *"though it remains behind
Mythos 5 on cybersecurity tasks"*, while every remaining eval is still self-chosen.

**Negative examples belong in the corpus too.** The vendor launch posts measured in §6a are the
register the anti-rubric is aimed at, and showing the judge one of those beside a Lex headline
about the same event is the cheapest calibration available. The DeepMind launch post scored 13.14
laundered-verb-and-capability fires per thousand words against zero for every good source in the
table.

### What I could not read, stated plainly

Economist article bodies, NYT, Reuters, Bloomberg and FT Lex bodies were all inaccessible, to me
and to a parallel agent working independently. **I have not filled those gaps from memory.**
Where this document describes Lex, it describes headlines and standfirsts, which I did read.
Where it describes the leader form, it describes four Guardian leaders, which is a small sample
from one publication and one genre.

---

## 9 · What I am deliberately not taking, and why

Requested explicitly, and it is the part that guards against pastiche.

**From Harari, I am not taking:**

- **The civilisational opener.** "Humankind is now facing a global crisis. Perhaps the biggest
  crisis of our generation." Hedged twice in two sentences, and it tells the reader nothing. It
  is also the single easiest thing to imitate, which is what makes it dangerous: an imitation of
  Harari's worst move is indistinguishable from generic AI prose, and it would be *produced by a
  rubric that told the model to write like Harari.*
- **The binary-choice close.** His own closing paragraph is the false fork this document bans.
- **The species-scale "we".** "Humanity needs to make a choice." This paper has one reader and
  then a few thousand; it addresses people who ship things.
- **The confident synthesis across fields he has not measured.** It is the thing his critics
  attack and they are often right. This paper's whole provenance apparatus exists to prevent
  exactly that move.

**From Benjamin, I am not taking:**

- **Juxtaposition without a stated relation.** Discussed at length in §2. It needs 5,000 words
  and it degrades, at news length, into precisely the "signals a broader shift" construction the
  anti-rubric catches.
- **The messianic and theological register.** "A storm is blowing from Paradise." No.
- **Deliberate difficulty.** Benjamin's obscurity is sometimes load-bearing and sometimes just
  obscurity. Thesis II ("The past carries a secret index with it") is not checkable prose. A
  newspaper cannot ask a reader to work that hard before breakfast, and a model imitating
  difficulty produces nonsense that looks profound, which is the worst possible failure here.
- **The aphorism as a unit.** Benjamin's short forms are self-contained aphorisms. A news story
  is not; it is accountable to an external event.

**From Marx, I am not taking:**

- **The polemical register.** "That great robber, Lord Clive." "The profound hypocrisy and
  inherent barbarism of bourgeois civilization." Marx earned that from a political position this
  paper does not hold and should not fake.
- **The definitional cascade.** *Capital* chapter one.
- **The anaphoric hammer.** Four sentences beginning "We must not forget."
- **The teleological frame.** "the unconscious tool of history." Marx's confidence comes from a
  theory of where history is going. This paper has no such theory and borrowing the cadence
  without the theory is exactly what pastiche is.
- **The extended analogy chain.** "Hindostan is an Italy of Asiatic dimensions..."

**And the thing I am not taking from any of them: the authority.** All three write as people
whose judgement has already been established. A daily paper on its second week has established
nothing. The rubric compensates by requiring the specific, checkable thing in every sentence that
carries weight, which is what a writer without standing has instead of standing. That is not a
limitation to be written around. It is the actual reason C3, C4, C6 and C10 exist.

---

## 9a · Four defects found while assembling this

Not writing questions, but they surfaced from reading the registry and the live edition, and each
one silently degrades what the writer receives. Recording them here rather than losing them.

1. **`sources.js:737` claims SemiAnalysis ships free full text in the feed. It does not.** Measured:
   20 of 20 feed items end in "Read more", and the live pages carry Substack paywall markup. The
   free preview is large, 12k to 108k characters, so `extract` stores a **truncated article that
   reads as complete** and the writer works from a cut without knowing it. This is
   absence-rendering-as-health in the one place it does most damage.
2. **`latent-space` is one source id with two access regimes.** The `[AINews]` digests are
   paywalled; the essays and podcasts are free. Six of the eight most recent feed items are the
   paywalled kind. The live edition's weakest story, an unverified $13B acquisition claim, came
   from that half.
3. **`openai-news` delivers titles with zero description characters** on all of the first seven
   items, and `openai.com/index/*` returns 403 to two independent fetchers from a residential IP.
   Whether it also 403s from the Cloudflare Worker is **untested**, and worth testing, because the
   paper's second-largest lab source is currently headlines only.
4. **`simon-willison` is one source at priority 36**, but 26 of his last 30 items are sub-2,100
   character link notes and the occasional 13,000-character review is the only one worth a deep
   read. Nothing in the schema separates them, so the deep-read budget is spent uniformly on both.

---

## 10 · What in this document is unverified

Per the estate's rule that a rule without its detector reads unverified rather than as covered:

- **The scoring thresholds in §5 are guesses.** No detector confirms them. The calibration
  procedure is named in §5 and has not been run.
- **The rubric itself, all ten criteria, is unverified.** No draft has been scored against it. Its
  inter-rater reliability is unknown, and the only thing that would establish it is running two
  judges over the same twenty drafts and comparing.
- **The anti-rubric is implemented and partly measured.** The code is at
  `scripts/slop_detect.py` and §6a reports what it found on a nine-sample corpus. What is
  measured: items 12, 13, 22, 24 and 25 have known fire rates on that corpus. What is **not**
  measured: every other rule in §6 fired too rarely in that corpus to say anything about, the
  false-positive rate on real drafts of this paper is unknown, and no rule has been tested
  against a news story of any kind.
- **The newspaper findings rest on two corpora, both small and both skewed.** I read four Guardian
  leaders and four LRB posts in full. A parallel agent independently read ten Guardian leaders,
  five Guardian news pieces, ten AP wire stories and seven LRB posts, 66,057 words. The
  paragraph-structure finding in §4a is therefore verified twice by different readers, and the
  paragraph-architecture split in §4g and the zero-restating-endings finding in §4d come from the
  larger corpus. But it is still four publications, no Economist and no FT, and the two corpora
  overlap on the Guardian.
- **Two findings in §6a and §4f are the parallel agent's, not mine.** The 39-construction
  frequency table and the sentence and paragraph metrics were measured by it and I have not
  re-run them. It disclosed two method faults on itself, a truncating AP extractor whose endings
  analysis it discarded, and BBC ledes taken from body text rather than the summary field. Both
  disclosures raise my confidence rather than lowering it, but the numbers are second-hand.
- **Lex is described from headlines and standfirsts only.** I never read a Lex article body. Any
  claim about how Lex constructs a paragraph would be invention and none is made.
- **Harari's *Economist* essay is described from its first paragraph only.**
- **The claim that regurgitation is structural rather than lexical is an argument, not a
  measurement.** The test that would settle it: take ten drafts that fail C6 and C10, strip every
  item in anti-rubric 24 and 25, and see whether a reader can still tell. That test has not been
  run and it should be, because the whole ordering of §6 depends on the answer.
