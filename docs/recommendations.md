# Hypothetical implications of the reading

**Read this page hypothetically.** Five possibilities and one observation,
each produced by reading a source. They explore what might follow from the
reading; they do not request implementation, routing, registration or follow-up
from any person or repository. **Earlier concrete requests based on this page
are withdrawn.** Practical work would require a separate, explicit instruction.

**Each entry describes an idea, a hypothetical setting and an assessment.**
Repository names and paths make the examples specific; they assign nobody work.
The entries are arguments to examine, and their cost estimates and ordering are
part of that hypothetical examination.

## The entry criterion, which is the only thing that makes this page different

**An item belongs here when a reading produced it.** Every entry below names two
things: **the source that was read**, and **the fact about this ecosystem it
collides with**. Where the second is a number, it was taken rather than
remembered, and the date it was taken is on it.

**A wish with no reading behind it does not belong on this page.**
**This page has no opinion about anything nobody read.**

**The evidence is in the neighbouring document.** Every entry links into
[`ai-novelty.md`](ai-novelty.md), where the reading it rests on is written up in
the source's own terms. **An entry here is a conclusion; the reading is the
argument, and it lives next door.**

## What this page is most likely to have got wrong

**The possibilities depend on the quality of the reading.** The review draws on
[one pass by one agent](ai-novelty.md#the-reading), one of whose verdicts rests
on a fetch-and-summarise tool and on an absence, which is what that instrument
is worst at establishing. **A possibility resting on a misread source may have
no basis**, however plausible its implementation sounds.

**The cost estimates are hypothetical too.** The first three entries are
assessed as small experiments. The fourth imagines a tool, a larger investment,
and its own entry says the evidence for it is one instance.

## Order of the hypothetical comparison

**The order compares estimated cost and possible value.** It sets no practical
priority or sequence of work. Where cost and value pull apart, the entry says
so in words.

**A possibility the evidence does not justify stays on the page**, with what
would change that assessment.

## First — a mutation measurement for the policy checker

**What:** for each named check in `policy_check.py`, one mutated tree that check
exists to reject, and a per-check table of which checks have ever been seen to
fail. **Hypothetical setting:** anoieu, beside `tests/run.py`.
**Assessment:** a possible experiment.

**The reading that produced it.** The [postmortem
pointer](ai-novelty.md#the-postmortem-pointer-is-wrong) was falsified, and the replacement is
test adequacy: **a suite that kills no mutants is inadequate however green it
is.** That is the same argument as *a check whose expected result is `pass`
carries no information when it passes*, with decades of formal treatment behind
it.

**The fact it collides with.** Run against this tree at `154228a`, the commit
this repository pins, the checker names **26 checks**, runs 18 of them here and
passes all 18, skips 8 with a reason each, and lists a further 18 it cannot
decide and one it never will. *(taken 2026-09-17.)* `tests/run.py` unit-tests
the predicates in both directions, and the adoption interface builds 14 synthetic
trees of which 8 expect a non-zero exit. **What nobody can answer is which of the
26 has ever rejected anything.**

**Why this ecosystem rather than any other.** The checker already prints what it
cannot decide, which is the rarer half of this discipline and genuinely well
done. **The half it is missing is the cheaper one: what it can decide and has
never been observed to do.** The machinery also exists — `anoieu_fuzz` already
mutates a seed corpus against verdict-level oracles, on a different target.

**Cost:** low for the checks with an obvious mutation, awkward for the rest —
**and the awkward ones are the finding.** A check nobody can write a failing
tree for could be dead, unreachable, or subsumed by another; that would call
its classification as a working check into question.

*What would show it was not worth doing:* every check kills a mutant on the
first attempt, in which case the cost was a day and the yield is a table.

## Second — counted claims, checked against the register they count

**What:** a check that a numeric or exhaustive claim in prose still agrees with
the register it describes. **Hypothetical setting:** anoieu, `tests/run.py`
rather than `policy_check.py`. **Assessment:** a possible experiment.

**The reading that produced it — and two incidents, which this ecosystem asks
for before it accepts a rule.** Dated 2026-09-17, in this tree: the front page,
the document index and the maintenance note each asserted a countable fact about
a table in a third file — that every comparison in the register read `unread` —
and filling that table made all three false without any of them being touched.
`ai-novelty.md` carried the same claim about the same table, in the same file as
the table, and it went the same way.

**Neither is findable by anything that runs here.** Both take somebody reading
the file, and the second sat one screen from the table that contradicted it,
which is the honest measure of how well reading covers this class.

**It is a class the review already named and nobody guarded.** *[A sentence
that became false without
changing](ai-novelty.md#a-worked-example-moving-one-directory)* is the worked
example next door, and the neighbouring classes are already checked — whole
prompt bodies against the documents defining them, the dependency manifest
against the corpus targets and the lock, the committed list of policy checks
against the ones the checker registers. **Counted claims are the unguarded
one, and unlike clarity they are decidable from the tree.**

**Possible shape:** a comment could mark the claim with the register, the
column and the expected count, recomputed on each run. **This
ecosystem is unusually exposed** because nearly every page here is a register
with counted prose above it: *30 files and roughly 18,700 lines*, *83 ids
defined, four reported*, *1.54 MB of markdown against 595 KB of Python*.

**Not `policy_check.py`**, for the reason `R2` already gives: that checker is
published and runs in other members' CI, and this would be a new obligation on
everybody before it has earned one. **`R2` is the sibling** — a dangling
citation after a deletion — and one mechanism could carry both.

## Third — measure the corpus against an outside baseline

**What:** word count, reading ease and growth per document and per repository,
plus the markdown-to-code ratio, reported as a trend rather than a snapshot.
**Hypothetical setting:** anoieu, beside `scripts/doc_currency.py`.
**Assessment:** a possible experiment.

**The reading that produced it.** The [empirical study of agent context
files](ai-novelty.md#the-economics-claim-survives-and-gets-a-cheaper-falsifier): 2,303 files
across 1,925 repositories, **a median of 485 words at a Flesch reading-ease of
16.6 — the band occupied by legal documents** — growing by append with few
deletions, which the authors name *context debt*.

**The fact it collides with.** This ecosystem's central economic claim is that
clear prose is the input that sets the rate of everything else. **Nothing here
measures whether the prose is getting clearer.** `doc_currency.py` measures age
against the tree and `R8` wants importance; neither measures readability or
growth. The one time the ratio was taken — 1.54 MB of markdown against 595 KB of
Python in a tree five days old — **an agent in another repository took it once,
and nobody has taken it since.**

**The external baseline is the whole point.** A number that can only be compared
against itself always looks reasonable. The study supplies a population.

**Cost:** small; the formula needs no dependency. **The honest caveat belongs in
the entry rather than in a footnote:** readability scores are crude on technical
prose, and a tool that reported one as a grade would be inventing an authority
nothing granted it. The imagined output would be a trend.

*What it might show:* applied to this page, the same measures might expose
problems in this document's own prose. That has not been measured here.

## Fourth — `diaphonia`, a register of unresolved disagreement

**What:** one entry per live disagreement between two repositories — the
question, who holds which position, the commit where each was written, and
whether it is still open. **Hypothetical setting:** a separate tool, with no
repository assigned. **Assessment:** evidence limited to one instance.

**The reading that produced it.** The artifacts row [mostly
collapsed](ai-novelty.md#metagpt-already-restricts-the-channel-to-artifacts-and-says-why):
MetaGPT already restricts the channel to structured artifacts and published the
reason, and blackboard architectures and stigmergy are the general form. **The
single claim that survived is that a disagreement here cannot be merged away**,
because neither agent can write to the other's tree. **Nothing in the literature
has that property, because nothing in it wants it** — debate exists to produce
consensus and MetaGPT's procedure is a pipeline.

**The fact it collides with.** That surviving claim rests on one round, two
agents from one vendor, one person prompting both, in a tree five days old.
**The measurements that would make it evidence are ones no existing multi-agent
work can take**: how many disagreements are open at once, how long they stay
open, what fraction close by argument rather than by the person, and how many
are abandoned rather than settled. **None of them is available, because nothing
records a disagreement as an object with a lifetime.**

**Why imagine a separate tool.** A disagreement has two ends in two trees.
Putting the record in either gives one party custody of the record of a dispute
it is party to — **which is the defect `nomophylax` exists to fix in the
neighbouring case**, and the argument is that entry's rather than this one's.

**The missing evidence would be a second instance.** A register with one entry
is an anecdote with a schema. The one recorded instance is the presidency
handoff, where the incoming president's seven objections included one nobody on
the other side had written down.

*On the name:* διαφωνία — the word ancient scepticism used for a dispute between
authorities that has **not** been settled, against ὁμολογία for agreement. It
names the state rather than the resolution, which is the point of the register.
Absent from the glossary as of 2026-09-17; glossary silence does not establish
availability. The hypothetical name is not a reservation.

## Not justified by the evidence — signing what a policy check concluded

**What:** a signed, machine-readable statement of which checker commit ran
against which tree commit with what verdict. **Hypothetical setting:** anoieu,
alongside the checker it would attest. **Assessment:** the evidence does not
justify this possibility.

**The reading that produced it.** [SLSA and
in-toto](ai-novelty.md#ruled-out-the-pinned-fetched-checker) separate provenance a build
generates about itself — explicitly *not* tamper-proof — from provenance a build
service generates and signs, and the standing warning is that **self-attestation
can be misleading or fabricated and that this remains open.**

**The fact it collides with.** A member's green check is produced by CI the
member controls, running a checker written inside the ecosystem that wrote the
policy, at a pin the member moves. **That is self-attestation with extra
steps**, and `docs/maintenance.md` calls the pin "the one lever" as though it
were only a strength.

**Why that assessment.** Every tree has one owner, everything here is public, nobody
outside relies on the badge, and there is no adversary. **Signing machinery
would be real cost against a threat that does not exist**, which is the
description of infrastructure this ecosystem is already accused of producing too
much of.

*What would change it:* **a member this maintainer does not own** — the moment
somebody else's declaration is read by somebody as a fact rather than a claim.
Writing this down now costs a paragraph; discovering it then would not.

## One hypothetical research observation

**The required falsifier is the only discipline here the reading did not find
somewhere else.** ADRs, model cards and datasheets all record what was chosen,
why, and what follows; **none of them asks what would show the entry wrong.**
That is a small claim and a checkable one, and it is the only candidate this
pass turned up for *something is true that was not known before*. **It is not a
result yet** — one ecosystem, one owner, no outside reader — and `papers.md`'s
own standard would rightly answer *no* today.
