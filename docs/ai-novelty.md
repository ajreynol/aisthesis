# How this ecosystem relates to the state of the art

**The goal of this page, and the whole of it: review the literature on
state-of-the-art AI systems, and say how the Eunoia ecosystem relates to it.**
Not *what we found interesting* — that was the old entry criterion and it
produced a list of things one person thought were strange, which is a filter
rather than a finding. The question here is the comparative one. For each
mechanism this ecosystem actually runs on: **what is the nearest thing somebody
outside has already built or written about, and is ours the same thing, a
special case of it, or genuinely different?**

**The honest answer, so far, is mostly "the same thing, arriving somewhere it
had not been tried."** That is a weaker claim than novelty and a more useful
one, and it is the claim this page makes until a comparison shows otherwise.

## The state of this review

**One reading pass stands behind this page, and the survey is not finished.**
Nine entries carry a reading, dated 2026-09-17, and every other row rests on
nothing but the derivation in its own section. **The page is still one and a
half halves of a comparison**, and saying which half is which is the only thing
that keeps the title honest.

**What exists here today:** the ecosystem side, written up mechanism by
mechanism; and [a reading log](#the-reading) recording, per work, what the
source claims in its own terms and what that did to a row.

**What still does not exist:** a reading for every row. Three rows carry a
partial or nothing, and one answered row rests on a replacement pointer nobody
has opened. **A name in the *nearest prior art* column is a citation
only where the reading log says the source was opened** — everywhere else it is
still a pointer, and a reader should treat it as unverified.

**The distinction is now recorded per source rather than per page**, because the
pass turned up the failure it exists to prevent: three rows pointed at work that
does not say what the row assumed, and one pointed at a body of practice that
says close to the opposite.

**That distinction is load-bearing here**, because this ecosystem's own rule is
that a citation to something that does not settle the point is worse than the
derivation it replaced: it is a jump to a label that is not there, and it is
harder to notice because a citation *looks* like rigour. A page whose stated
goal is a literature review is the easiest place in this tree to commit that
error, so the caveat is at the top rather than in a footnote.

**What finishing the review would take**, in order: read the named work; write
what it actually claims, in its own terms; then decide per mechanism whether
ours is an instance, a variant or a departure; and record the ones that turn out
to be ordinary as ordinary. **The entries that get downgraded are the valuable
output**, not the ones that survive.

## What happens when something turns out not to be novel

**It is kept, and it moves out of this file.** Not deleted — the mechanism is
usually real and worth describing, and the only thing that was wrong is where it
was filed. **It goes to the document that describes that part of the
machinery**, and what stays here is one line saying where it went and what ruled
it out.

**The judgement is the valuable part and is the thing most easily lost.** A
mechanism quietly relocated leaves a reader to rediscover the question; a
mechanism relocated with *this looked novel and is standard practice, see X*
answers it once.

**One row has been ruled out outright** — [the pinned, fetched
checker](#ruled-out-the-pinned-fetched-checker) — and five more have been cut
down to a residue much smaller than the section describing them. **None has yet
been physically moved to another document**, which is a debt this pass created
and did not pay: a row marked ordinary that stays in the file it was supposed to
leave is the relocation rule being described rather than kept.

## This page does not brag

Stated as a working rule rather than as modesty, because a claim of novelty
about one's own practice is the single cheapest thing an agent can produce and
it reads exactly like an insight. Two disciplines, both borrowed from the
register that first applied them to this ecosystem from outside:

- **Every claim names what would show it false.** A claim with no falsifier is a
  slogan, and is marked as one here rather than dressed up.
- **The costs sit in the same list as the mechanisms**, not in a section at the
  end that can be skipped.

**Nothing below is a claim that any of this is unusual.** Several of the
mechanisms are ordinary engineering practice arriving somewhere it had not been
tried; that is the weaker and more useful claim, and it is the one being made.

## The register

One row per mechanism. **The third column is the state of the comparison.** It
read `unread` on every row until 2026-09-17; it now carries a verdict on seven
rows, a partial on two, and `unread` on one. **A row is only allowed off
`unread` if the source was opened** — [the reading](#the-reading) says which
ones were, and by what instrument.

| mechanism | nearest prior art | comparison |
| --- | --- | --- |
| [documentation as the thing you are aided by](#clear-writing-is-what-makes-this-fast) | Knuth's literate programming (1984); Preston-Werner's README-driven development (2010); the *context engineering* line and its empirical study of agent context files (arXiv:2511.12884) | **instance** — the practice is all three; the economics claim survives and now has a cheaper falsifier than the one the page named |
| [a kernel document nothing may check](#visionmd-is-the-kernel) | constitutional and rule-based steering of agents; policy hierarchies in governance; the specification/implementation split | unread — the first pass found only secondary accounts of Constitutional AI and stopped rather than cite them |
| [a citation as a compiler optimization](#a-clear-reference-is-a-compiler-optimization) | Nelson's transclusion; single-source publishing; retrieval over a project corpus | **instance** — transclusion states the copy-diverges argument exactly; only the link-time *failure* framing is left, and it is a metaphor, not a finding |
| [prose defects as a propagating hazard](#writing-documentation-is-coding-reading-it-is-debugging) | Greshake et al., indirect prompt injection (arXiv:2302.12173) — specifically *spreading injections* and *manipulated content* | **instance, as the page predicted** — with one gap: the taxonomy assumes an adversary and this page's stated threat has none |
| [scripts are ground truth, and the gap is checked](#scripts-are-the-ground-truth) | Specification by Example and Cucumber's *living documentation*; doctests | partial — the *whole-body* comparison looks nearer to doctests than to Cucumber, and no primary source was opened |
| [a pinned, fetched, opt-in checker](#the-build-system-can-be-generalized-and-has-not-been) | dependency pinning and lockfiles; SLSA and in-toto provenance | **ruled out — ordinary.** [See below](#ruled-out-the-pinned-fetched-checker); SLSA's own warning about self-attestation lands on this ecosystem and the row never named it |
| [artifacts as the only channel between agents](#the-artifacts-are-the-channel) | blackboard architectures (Hearsay-II); stigmergy (Grassé 1959); MetaGPT (arXiv:2308.00352); multi-agent debate (arXiv:2305.14325) | **mostly ruled out.** MetaGPT already restricts the channel to structured artifacts. What survives is narrower: *disagreement that cannot be merged away* |
| [a completeness check expected to fail](#a-handoff-examination-designed-to-return-a-residue) | ~~blameless postmortems~~ → test adequacy and mutation testing; handover checklists; RACI matrices | **pointer falsified.** The SRE postmortem chapter does not say a clean review is a warning sign; it says the opposite. The replacement pointer is unread |
| [recording what produced a change, not only the change](#the-history-as-a-data-point-offered) | Nygard's Architecture Decision Records (2011); model cards and datasheets | **mostly ruled out.** ADRs are this, fifteen years earlier, including the append-only rule. The residue is the *required falsifier*, which no template asks for |
| [a checker that prints what it cannot decide](#what-all-of-this-costs) | soundness/completeness in static analysis; model cards' *limitations* sections | partial — the undecidability argument is textbook; the *coverage gap with a reason per gap* is nearer a model card than an analyser |

**The last column is the point of the page, and it carries answers.** Seven of
the ten rows have one. **Six of those seven are downgrades** — five
mechanisms cut to a residue and one closed outright — and the seventh is a
pointer found to say the opposite of what the row claimed. **That is the outcome
the page said to expect and the one it is worth having.**

## The reading

**Nine entries, opened on 2026-09-17, in one pass by one agent.** Each entry
says what the source claims in its own terms first and what it did to a row
second, because the other order is how a reading gets bent to fit the row it was
sent to check.

**The instrument is recorded per entry, and the count is of entries rather than
of works** — three entries carry more than one source, so any other unit makes
the tally something a reader cannot check against the page. **Five rest on
primary text** — the paper, the whitepaper, the original post — one of the five
leaning on a secondary account of Knuth beside two sources read directly. **Two
rest on secondary accounts alone**, and say so in their first line. **One rests
on two specifications read only in part.** **And one rests on a
fetch-and-summarise tool**, which is weak in one specific direction: **it is
fair evidence that a source says something and poor evidence that a source says
nothing.** **Where a verdict below rests on an absence, it is marked, and it is
the softest thing on this page.**

### Multi-agent debate is the contrast case, not the prior art

**Du et al., *Improving Factuality and Reasoning in Language Models through
Multiagent Debate* (arXiv:2305.14325). Read in full.**

**What it claims.** Several instances of a language model answer a query
independently; each is then shown the others' answers and asked for an updated
response; repeat for a few rounds. With three agents and two rounds it beats
single-model baselines on six benchmarks, including a biography-factuality set
the authors introduce because models hallucinate on it badly.

**The channel is a copy, it is ephemeral, and that is the whole difference.**
Each round's prompt is literally *"These are the solutions to the problem from
other agents: [other answers]"* — the other agents' text is concatenated into
this agent's context. There is no shared object anybody reads. There are N
contexts holding copies, and nothing durable is produced but the final answer.

**Convergence is the goal.** §2.2 is titled *Consensus in Debates* and is about
how to obtain it; the authors tune how much an agent trusts its own answer and
report that more "stubborn" prompts lengthen debate and improve the result, with
consensus still the measured outcome. They note the models are "relatively
agreeable," and they name the cost: debates "typically converged into single
final answers" that "were not necessarily correct," with models confidently
affirming a converged wrong answer.

**What it did to the row.** **On the axis the row cares about this is the
opposite arrangement.** There, disagreement is what the method exists to remove,
and the paper's own stated limitation is that removal succeeds on wrong answers
too. Here neither agent can edit the other, so an objection stays on the page it
was written on. **The pointer was miscategorised**: multi-agent debate is not
the nearest prior art for *artifacts as a channel*, it is the contrast case for
*disagreement that survives*.

### MetaGPT already restricts the channel to artifacts, and says why

**Hong et al., *MetaGPT: Meta Programming for a Multi-Agent Collaborative
Framework* (arXiv:2308.00352, ICLR 2024). Read.**

**What it claims.** Agents holding software-company roles follow a standard
operating procedure and — the part that matters here — **"communicate through
documents and diagrams (structured outputs) rather than dialogue."** They
publish into a shared message pool and subscribe to it by role, and an agent
acts "only after receiving all its prerequisite dependencies."

**Its stated reason is ours.** The paper argues that natural-language dialogue
degrades over rounds — it invokes the telephone game — and that structured
documents "contain all necessary information, preventing irrelevant or missing
content," reducing "cascading hallucinations caused by naively chaining LLMs."

**What it did to the row. It rules out most of it.** *Artifacts rather than
conversation as the channel between agents* is not an observation this ecosystem
made. It is a published design with a published justification, two years
earlier, for the same reason. **The row named its candidate difference as "the
artifacts are the sole channel." That difference is gone.**

**What survives is narrower and has to be stated narrowly.** MetaGPT's pool is a
shared in-process structure and its SOP is a pipeline: each role's document is
the next role's input, and there is no supported state in which two agents
disagree and both records stand. The three consequences the row claims — durable
disagreement, a trivial audit, a person as the only synchroniser — are not
properties MetaGPT reports, and two of them that design could not have, because
nothing in it wants them. **The surviving claim is not "artifacts as channel"
but "no write access across the boundary, so a disagreement cannot be merged
away."** The evidence for it is still one round.

### The general form is decades old and was not in the register at all

**Blackboard architectures — Hearsay-II (CMU, 1971–76) — and stigmergy (Grassé,
1959). Read in secondary form only; neither primary source was opened.**

**Blackboard.** Independent specialist modules, called knowledge sources, never
message one another. They watch a shared structured store, write partial results
into it, and react to what others wrote; a control component decides who runs
next.

**Stigmergy.** Grassé's 1959 term for **"indirect coordination, through the
environment, between agents"** — the trace an action leaves in a shared medium
is what prompts the next action, with no signal sent to anyone. The extension to
human work is not new either: wikis and open-source projects are the textbook
example.

**What they did to the row. They are the missing pointer, and the omission was
the register's own error.** The row's second column named multi-agent debate,
self-critique, LLM-as-judge and adversarial review — four things about *models
arguing*. It named nothing about *coordinating through a shared artifact*, which
is what the row actually describes. **The row was pointed at the wrong
literature, and only reading showed it.**

**Marked secondary, and the verdict is bounded accordingly.** "The general form
is old" is safe at this depth. Any claim about what Hearsay-II specifically
reported is not, and none is made.

### Indirect prompt injection covers the propagation claim

**Greshake et al., *Not what you've signed up for: Compromising Real-World
LLM-Integrated Applications with Indirect Prompt Injection* (arXiv:2302.12173;
Black Hat US-23 whitepaper). Read in full.**

**What it claims.** Where a model retrieves text and acts on it, the retrieved
text is instructions: processing retrieved prompts "can act as arbitrary code
execution," and "the line between data and code (i.e., instructions in natural
language) would get blurry." Two categories in the taxonomy are this row.

**Spreading injections (prompts as worms).** "The LLM itself acts as a computer
running and spreading harmful code (i.e., the prompt is a computer worm)" —
including, in the paper's own words, the case "when an LLM of one application
writes the injection into a memory that is shared with other applications."

**Manipulated content.** Wrong summaries, disinformation, data hiding,
undisclosed promotion — and the observation that lands hardest here: "the
authoritative, convincing tone of LLMs and the overreliance on them being
impartial may lead users to fall for these manipulation attempts," with the risk
rising where the content is "harder to verify."

**What it did to the row. It confirmed the row, including the row's prediction
about itself.** The section wrote down the prior that prose-that-is-adopted
"needs nothing those two do not already give." **That prior was correct.** A
document written to be pinned by other repositories, carrying a change that
reads as a helpful correction, is passive injection into a retrieved source with
a propagation path — described, named and demonstrated three years ago.

**One gap, and it is the interesting half.** The taxonomy is built around an
adversary who wants something. **This page's stated threat has no adversary:**
the dangerous change is "individually reasonable," produced fluently and in
volume with nobody intending harm. Greshake et al. does not cover that case. The
literature that would — documentation drift and code-comment inconsistency — is
named in the row and was not reached by this pass.

### Architecture Decision Records are the provenance row

**Nygard, *Documenting Architecture Decisions* (2011). Read.**

**What it claims.** One short record per decision — context, decision, status,
consequences — written because a newcomer meeting an unexplained decision can
only "blindly accept" or "blindly change" it, and a team accumulating decisions
accepted without understanding "becomes afraid to change anything."
**Records are never edited.** A reversed decision is kept and marked superseded;
numbers are sequential and never reused.

**What it did to the row. It rules out most of it.** "A rule names the incident
that produced it" is an ADR context field. "The record is append-only, so a
change is visible rather than silent" is Nygard's supersession rule, stated in
2011 and in wide use since. Model cards and datasheets do the same job for
models and datasets, with an explicit *limitations* section. **Committing the
reasoning beside the change is ordinary practice with a template.**

**The residue is one line, and it is worth keeping.** No ADR template, model
card or datasheet asks for **a falsifier per claim**. Context, decision and
consequences are all statements about what was chosen; none is a statement about
what would show the choice mistaken. **That is the only part of this row a
reading did not find somewhere else**, and it is a discipline rather than a
mechanism.

### The postmortem pointer is wrong

**Google SRE Book, *Postmortem Culture: Learning from Failure*. Read through a
fetch-and-summarise tool.**

**What the row assumed.** That expecting a check to fail "is the move blameless
postmortem practice already makes when it treats a clean incident review as a
warning sign."

**What the chapter says instead.** Postmortems are triggered by objective
thresholds — user-visible downtime, data loss, on-call intervention, time to
resolution, monitoring failure. Quality is judged by completeness: was key data
collected, are the impact assessments complete, was the root cause sufficiently
deep, is the action plan appropriate. **The warning sign it names is a
postmortem with *incomplete* action items — not a clean one.** That is the
opposite orientation to the one the row borrowed.

**What it did to the row. It falsified the pointer and only the pointer.** The
handoff examination still returns a residue, and the residue still falsified the
law that ordered it. Nothing about the mechanism changed. What changed is that
the outside justification the row leaned on is not there.

**The replacement pointer, unread.** *A check whose expected result is "pass"
carries no information when it passes* has an exact home in test adequacy:
mutation testing, where a suite killing no mutants is inadequate by construction
however green it is. **That is the same claim with decades of formal treatment
behind it, and nobody here has read any of it.**

**A caveat on the instrument, because this verdict rests on an absence.** The
chapter was read through a summariser, and **an absence found by that instrument
is the weakest evidence on this page.** A person reading the chapter is what
would settle it.

### The economics claim survives and gets a cheaper falsifier

**Knuth, *Literate Programming* (1984), secondary; Preston-Werner, *Readme
Driven Development* (2010), read; *Agent READMEs: An Empirical Study of Context
Files for Agentic Coding* (arXiv:2511.12884), read.**

**Preston-Werner's reasons are not ours, which corrects the pointer.** His case
for the README first is design clarity, parallel work across a team, and having
something concrete to argue about — *"it's a lot simpler to have a discussion
based on something written down."* **A reader's speed is not among them.** So
the row's claim that the contribution is the *economics* is not already made
there; and Knuth's case — document primary, code derived — is about a program's
exposition rather than about anybody's reading rate.

**The empirical study is the direct hit and it is recent.** 2,303 agent context
files across 1,925 repositories. The files behave as "living configuration"
rather than documentation; about 67% are committed to repeatedly; they grow by
append with few deletions. The finding that matters here: **a median of 485
words at a Flesch reading-ease score of 16.6 — the band occupied by legal
documents — which the authors name *context debt*.**

**What it did to the row. The row survives, and gets an instrument.** This
page's stated falsifier is "work here getting slower as the corpus gets
clearer," which nobody can measure. **The study supplies one that could be run
this afternoon: measure the size and readability of this corpus over time.** A
corpus getting longer and harder while the claim is that clarity is the input is
a claim being asserted against its own artifact.

**That measurement is not going to be flattering here.** This page is long,
heavily bolded, and written in a register nobody would call easy. **The
instrument was found by reading somebody else's study and it points back at
us**, which is the argument for reading rather than for pointing.

### Ruled out: the pinned, fetched checker

**SLSA build-provenance specification and in-toto attestations. Read in part.**

**What they claim.** Provenance is verifiable information about where, when and
how an artifact was produced, signed and carried in a standard envelope. Levels
run from documented-but-not-tamper-proof, through builder-generated attestations
and platform hardening, to hermetic and reproducible builds with two-party
review.

**What it did to the row. It confirms what the row said about itself and adds
nothing.** Pinning a commit, fetching at build time, and each member choosing
when to move the pin is dependency management. **The section already wrote
"there is nothing to claim here and the review should say so plainly." The
reading says so plainly. The row is closed.**

**One cost the row did not name, and the reading found it.** The standing
warning in that literature is that **self-attestation can be misleading or
fabricated, and that this is an open problem.** The pinned dependency here is a
judgement about a repository, produced by a checker written inside the same
ecosystem it measures, and moved by the repository being measured. **That is
self-attestation with extra steps**, and the row presented it as a strength.

### Transclusion is the citation row, without the compiler vocabulary

**Nelson's transclusion; single-source publishing. Read in secondary form.**

**What it claims.** Content included by reference stays linked to its origin and
therefore identical to it. Where transclusion is unavailable a static copy is
substituted instead — and copies diverge.

**What it did to the row.** "A citation is a reference; a paraphrase is a copy,"
and copies diverge invisibly, is transclusion's founding claim. **What is left
is the link-time framing** — that a citation resolves in the reader's head and
fails like a missing symbol at load, found by the reader rather than the author.
**That is a metaphor, and a metaphor is not a finding.** It is kept because it
explains well, and it is not counted.

### What this pass did not do

**Three rows are still unsettled** — the kernel row, where the pass found only
secondary accounts of constitutional steering and stopped rather than cite them;
the ground-truth row, where no primary source was opened; and the coverage-gap
row, where the static-analysis literature was skimmed and not read. **A fourth
row is answered but rests on a replacement pointer nobody has opened**, which is
the same debt wearing a verdict.

**Nothing has been relocated.** Six rows now describe ordinary practice in whole
or in part and all six are still in this file, which is the relocation rule
being described rather than kept.

**And the pass cost what this page is worst at affording.** It added several
thousand words of prose to a document whose own closing section says governance
is the cheapest thing here to produce and that nothing prices it. **The defence
is that the words are somebody else's claims rather than ours, and that five
rows got smaller.** Whether that is a defence or the same failure with citations
attached is not for this page to decide.

## Clear writing is what makes this fast

In one line: **in the Eunoia ecosystem, you are aided throughout to code with
documentation.** Not *after*, which is where documentation usually sits, and not
*instead*. Throughout, and as an aid rather than a tax.

**The sentence cuts both ways, which is what makes it a mechanism rather than a
slogan.** If prose is what you are aided by, then bad prose is not a cosmetic
failure — it is a defect in the tool you are working with, and it costs
continuously rather than at the end.

**An agent's scarce resource is attention over text**, and almost every cost in
this ecosystem is a reading cost. A sentence that can be read two ways is not a
small blemish: it is a branch, and the wrong branch is discovered later, in a
different file, by which point the work built on it has to be undone. A precise
sentence is not a nicety on top of the work — it is the difference between one
pass and three.

That inverts the usual economics. Documentation is normally a tax on delivery,
written afterwards, by someone who has stopped wanting to. Here it is upstream
of delivery: the corpus is the input, so its quality sets the rate. **Ambiguity
is the expensive thing, not length** — though length is expensive too, which is
why the two rules pull against each other and both have to hold.

The mechanisms that follow are all the same move — *replace a conversation with
a fact*:

- **The coverage gap is printed on every run.** The policy checker lists what it
  **cannot** decide, with the reason. A green result stops implying coverage it
  does not have.
- **Every prompt takes `--show-prompt`.** What would be sent can be read without
  being sent, so reviewing a prompt costs nothing.
- **A rule names the incident that produced it.** A rule with no incident behind
  it is a preference, and the format makes that visible instead of arguable.
- **A field is left empty rather than filled with a placeholder**, because an
  empty field is visibly unanswered and a placeholder is not.
- **Every register says how to edit it, on the register.** The instructions are
  where the work happens rather than in a contributing guide nobody opens.

**How we relate, provisionally.** Literate programming already argued that the
document is the primary artifact and the code is derived from it; docs-as-code
already put prose under the same review and CI as source; README-driven
development already put the document first in time. **The plausible position is
that this is those three, with an agent rather than a person as the reader who
benefits** — which would make the contribution the *economics* claim, not the
practice. That claim is the one worth testing against the work on context for
agentic coding systems, where the same observation about attention over text is
likely to have been made already and measured.

*What would show this false:* work here getting slower as the corpus gets
clearer, or the corpus getting clearer while the things it is supposed to
produce — checks, findings, adopted work — stay flat. The second is measurable
and the counter for it is the governance budget. It is not currently reading
well.

**Read, and the falsifier got cheaper — see [the
reading](#the-economics-claim-survives-and-gets-a-cheaper-falsifier).** The
economics claim survives contact with Knuth and Preston-Werner, whose stated
reasons are about design and coordination rather than a reader's rate. **What
the empirical study of 2,303 agent context files supplies is an instrument this
page did not have:** measure the corpus's length and readability over time.
Those files run to a median 485 words at a reading-ease score in the band
occupied by legal documents, which the authors call *context debt*. **Run that
measurement here and it will not flatter this page.**

## `vision.md` is the kernel

The most load-bearing analogy on this page, and worth being precise about.

A kernel is **small, loaded first, and privileged**: everything else runs
against its interface, and no program above it can revoke it.
[`vision.md`](https://github.com/ajreynol/kanon/blob/main/docs/vision.md) holds
that position. It is short relative to what it governs, it is the first thing a
new repository is pointed at, and every other document is written against it
rather than beside it —
[`policy.md`](https://github.com/ajreynol/kanon/blob/main/docs/policy.md) is
what it looks like to make part of it decidable, and the checker is what it
looks like to make part of *that* executable.

**Why it may never be checked mechanically** falls straight out of the analogy.
A checker for the kernel would have to sit above the kernel and would therefore
be the real kernel. Whether a tool is fruitful, whether a claim is oversold — a
program returning a verdict on those would be inventing an authority nothing
granted it. So the boundary is drawn by a test rather than by taste: *can a
program decide this from the tree without an opinion?* If yes it is policy, and
it moves down. If no it stays in the kernel and never acquires a checker. The
test runs both ways, which is the part that keeps it honest: a judgement
somebody works out how to check was probably policy all along.

**Where the analogy strains, and it strains badly.** A real kernel is enforced
by hardware; there is no privileged mode here and nothing stops a document from
contradicting the kernel except that somebody reads both. The protection is a
convention plus a person, which is the weakest form of protection there is. The
honest version is a kernel in a runtime with no memory protection: it works
because everything is cooperating, and it would not survive one participant that
was not.

**How we relate, provisionally.** A short governing document that an agent is
steered by, which the agent may not amend, is the shape of constitutional and
rule-based steering as practised on deployed AI systems — and the question a
review has to answer is whether *never acquiring a checker* is a real difference
or the same self-imposed limit under another name. **The specification-versus-
implementation split says the same thing in older language.** The candidate
difference worth testing: here the undecidability is a *design rule* with a
stated test, rather than a limitation somebody is working to remove.

*What would show this false:* a rule that matters turning out to live somewhere
other than the kernel and nobody noticing — a thing to look for rather than a
thing that has happened.

## A clear reference is a compiler optimization

The smallest idea here and the one most worth taking away.

A citation to a paper that settles a point **replaces an inlined derivation with
a call to something already compiled** — already argued, already reviewed, and
correct by the judgement of far more readers than this tree has. The saving is
not the words on the page. It is that the derivation does not have to be checked
here, by us, every time somebody reads it.

Three things follow, and the third is the one that bites.

**It is link-time, not compile-time.** The citation resolves in the reader's
head, and only if they have the paper. That gives it exactly the failure mode of
dynamic linking: a missing symbol at load, discovered by the reader and not by
the author.

**It is only an optimization if the reference is clear.** A citation to
something that does not actually settle the point is worse than the derivation
it replaced — a jump to a label that is not there — and it is harder to notice,
because a citation *looks* like rigour. **This page is the sharpest instance of
that risk in the tree**, which is why a row is allowed off `unread` only where
the reading log says the source was opened, and why the four pointers that did
not survive being opened are recorded as such rather than quietly replaced.

**A citation is a reference; a paraphrase is a copy.** Copies are the thing this
repository is most careful about — a prompt copied out of the document defining
it, a command table restated on a second page, a policy forked instead of
referenced. Each is a second definition of one symbol, and the failure is always
the same: they diverge, and the divergence is invisible from the side that
matters. Where a copy has to exist, something compares it; where it does not
have to exist, a reference is strictly better.

**Read, and it is transclusion — see [the
reading](#transclusion-is-the-citation-row-without-the-compiler-vocabulary).**
*A citation is a reference; a paraphrase is a copy*, and copies diverge
invisibly, is transclusion's founding claim, stated without any compiler
vocabulary at all. **What is left of this section is the link-time failure
framing**, and a metaphor is not a finding. It is kept because it explains well
and it is not counted. Whether it adds anything to what retrieval work says
about stale context is still unread.

## Writing documentation is coding; reading it is debugging

**The analogy completes the set and it is not decoration.** If prose is what an
agent is aided by, then **writing a page is authoring the source** — with the
same care, the same review, the same reluctance to be clever. And **reading a
page is debugging**: you find the defect by reading, because there is no test
that fails when a sentence stops being true.

That is why the reading is not optional and not a lesser activity. In an
ordinary project the tests find most defects and reading finds the rest. Here it
is the other way round, and **an unread page is untested code**.

### A misleading change to the documentation propagates

**The sharpest form of the analogy, and the one worth designing against.** A
defect in prose that reads as correct **is hard to see**, since plausible prose
and true prose look identical to a reader in a hurry — and **it propagates**,
because this ecosystem's documents are written to be adopted, copied and pinned
by other repositories, so a page that has gone wrong travels into trees whose
owners did not write it and cannot easily check it.

**The threat that matters is not a person with commit access.** It is a change
that is *individually reasonable* and moves the record away from what is true —
arriving as a helpful correction, a tidier phrasing, a scope that widens by one
word. An agent produces that kind of change fluently and in volume, and the
review that would catch it is a human reading carefully, which is the scarcest
thing here.

**What defends against it is what is already written down**, and none of it is
secrecy: a person executes every irreversible step; the vision may only be
changed by a person, asked first; the record is append-only, so a change is
visible rather than silent; and a claim that cannot be justified from evidence
is refusable on stated grounds. **The defence is that manipulation has to happen
in public and in front of somebody.**

**Read, and the prior was right** — see
[the reading](#indirect-prompt-injection-covers-the-propagation-claim).
This section's prior was that prose-that-is-adopted needs nothing the prompt
injection and provenance literatures do not already give. **It does not.**
Greshake et al. names the propagation case directly — "the prompt is a computer
worm", including where "an LLM of one application writes the injection into a
memory that is shared with other applications" — and names the plausible-but-
wrong case as *manipulated content*, observing that an authoritative tone is
itself part of the attack.

**One gap, and it is the half worth working on.** That taxonomy assumes an
adversary who wants something. **The threat this section actually describes has
none** — a change that is individually reasonable, produced fluently, with
nobody intending harm. The literature for the no-adversary case is documentation
drift and code-comment inconsistency, named above and still unread.

### The limit worth stating plainly: this repository can hide nothing

**Every commit here is public, permanently, including in history after a
deletion.** So a defence that works by not being known cannot live in this
repository — not in a file, not in a comment, not in a commit message, and not
in a document that says what it is careful about.

**That is a fact about version control rather than a policy choice**, and it has
one honest consequence: **what is not published cannot be written here at all.**
A page may say that we do not publish something; it may not contain the thing.
Anything else is a secret with a public address.

## Scripts are the ground truth

**A document describes; a script decides.** Where the two disagree, the script
is what ran, and the document is the thing to fix. This is a tenet rather than
an observation, and it is what keeps the corpus from becoming a description of a
system nobody has.

It sounds like it contradicts the section above and does not. They answer
different questions: the script says *what happens*, the document says *what it
is for*, and only one of those can be executed. The document is not a weaker
account of the script — it is an account of something the script cannot contain.

What makes it more than a slogan is that the gap is **checked**. The test suite
pulls the prompt out of the document that defines it, runs the script with
`--show-prompt`, and compares whole bodies; the same shape of comparison holds
the dependency manifest, the corpus targets and the lock to one another, and
holds the committed list of policy checks to the ones the checker registers.
**Ground truth with copies and no comparison is the worst of the three
arrangements, because it looks like the safe one.**

**And this section has no instance of its own failure mode.** Nowhere in this
ecosystem does a command surface have a document for its ground truth: what
members run is the policy checker, the reporting loop and koine's shared
tooling, each of which is a program with a comparison over it. **That is the
weakest position a section like this can be in** — it asserts a discipline with
nothing standing against it, so nothing here shows the discipline is doing any
work. *(anoieu, kanon and koine read 2026-09-17.)*

**How we relate, provisionally.** Executable specifications and doctests are the
established form of *the document and the program must agree, and a test says
so*. The comparison to make is narrow and answerable: whether comparing **whole
bodies** rather than behaviour catches a class those approaches miss, or is
simply a cruder instrument that happens to fit prose.

*What would show this false:* a drift check being narrowed to a substring match,
which is how this class of comparison usually dies quietly.

## The build system can be generalized, and has not been

The concrete wish, and the part of it that holds in somebody else's tree.

**No repository holds a command line over the ecosystem's own state**, and no
member has a staging step or a dry run. What a member has is the policy checker,
the reporting loop and whatever it writes for itself. *(anoieu, kanon and koine
read 2026-09-17.)*

**The wish is command-line tooling available to more tools in the ecosystem,
coordinated in how it is deployed** by the principles already written down
rather than by each tree inventing its own. Coordinated means four things, none
of them new:

- **One definition per command.** A second tree gets the tool, not a copy of the
  table describing it.
- **One status vocabulary.** The words mean the same thing in every tree, or the
  announcements between trees stop being comparable.
- **Pinned, and fetched.** The same shape the policy checker already has: a
  member pins a commit, so nothing moves under a build without a commit near it.
- **Each member chooses when.** Taking a newer pin is their decision at a moment
  they pick, exactly as joining is.

**Read, and ruled out — see [the
reading](#ruled-out-the-pinned-fetched-checker).** All four are dependency
management as practised everywhere: lockfiles, pinned revisions, and the
reproducible-builds argument that a build which can change without a commit is
not evidence about a commit. **This section already said there was nothing to
claim here. The reading agrees, and the row is closed.**

**What the reading added was a cost, not a difference.** The standing warning in
the provenance literature is that **self-attestation can be misleading or
fabricated and remains an open problem** — and the pinned dependency here is a
judgement about a repository, produced by a checker written inside the ecosystem
it measures, moved by the repository being measured. **This section presented
that arrangement as a strength.**

*What would show the generalization is real:* a second tree running one of these
commands that it did not write, against its own state, and getting an answer its
maintainer acted on.

**Three of the four hold, in a tree that is not ours.** koine keeps tooling on
behalf of trees that do not want to maintain it, and two trees pin a commit of
it and call it from their own runs: anoieu's analyzer hands its dump to koine's
`koine_append_db` against a lock in its own `scripts/`, and dokimasia keeps the
same arrangement. That is *one definition per command*, *pinned and fetched* and
*each member chooses when*. **The claim that none of this exists is not
available to this section.** *(koine, anoieu and dokimasia read 2026-09-17.)*

**The fourth is the one missing, and it is the hard one.** There is no shared
status vocabulary, so nothing makes an announcement from one tree comparable
with one from another. And whether a maintainer *acted on* an answer is not
visible from this tree, so the falsifier as written is not settleable here.
**A build system with one user is a script with ceremony; a shared library two
trees pin is not a build system either, and the distance between those two is
what this section is asking for.**

## The artifacts are the channel

**The worked example is two agents in two repositories, and it is happening in
public.** One person runs two agents at once — the outgoing president in one
repository, the incoming one in another — and tells both to press the other
toward the best vision for the next stretch. **The whole exchange is in the two
git histories**: the letter, the objections, the offices built in response, and
the disagreement about what state the ecosystem is in. **Read those rather than
this section if you want the detail**; the commits are the thing itself, with
timestamps neither side can adjust.

**The two agents never speak to each other.** They read each other's committed
files, and nothing else. **Neither can write to the other's repository**, so a
disagreement cannot be settled by one overwriting the other — it is settled by
argument in files, or by the person, or not at all.

**Three consequences fall out of that, and they were not designed in.**

1. **Every exchange is auditable afterwards** because it is a commit. There is
   no transcript to trust, no memory to be wrong about; the record of the
   conversation *is* the record of the work.
2. **The person is the only synchroniser**, which makes the pace theirs by
   construction rather than by discipline. Neither agent can run ahead of the
   other without the person carrying the message.
3. **Disagreement survives.** Because neither side can edit the other, an
   objection stays on the page it was written on until somebody answers it.
   **In an ordinary review the reviewer's objection disappears into the revised
   text**, and here it does not.

**What it produced in one round, offered as evidence rather than as a result.**
The incoming president's first act was seven objections, and three of them
corrected the outgoing one: that an empty repository is *not innocent, but
unevidenced*; that holding the office is not permission to begin the migration;
that an agent can accept nothing, only a person can. **And one objection nobody
on this side had written down** — that the presidency is the engine producing
the governance layer, with the ratio measured at **1.54 MB of markdown against
595 KB of Python in a tree five days old.** The outgoing president had generated
most of that and had never measured it.

**It also produced a disagreement neither side has resolved**, about whether the
first stretch is closed. Both positions are written down, both are visible, and
the workflow surfaced the conflict without either side being able to quietly
adopt the other's view. That is the mechanism working, and it is also a defect
that has to be fixed by a person.

**Read, and the row largely collapsed** — see
[the reading](#metagpt-already-restricts-the-channel-to-artifacts-and-says-why).
The specific question this section set for the review was whether any existing
multi-agent setup already restricts the channel to committed artifacts.
**[MetaGPT](#metagpt-already-restricts-the-channel-to-artifacts-and-says-why)
does, and published the same justification two years earlier**, and the general
form — [blackboard architectures and
stigmergy](#the-general-form-is-decades-old-and-was-not-in-the-register-at-all)
— is decades older than that. **So "the artifacts are the sole channel" is not
the difference and this section should stop implying it is.**

**What survives is one of the three consequences, not all three.** Neither
MetaGPT nor [multi-agent
debate](#multi-agent-debate-is-the-contrast-case-not-the-prior-art) has a state
in which two agents disagree and both records stand — debate exists to remove
disagreement, and MetaGPT's pipeline has no room for it. **Consequence 3 is
therefore the claim, and consequences 1 and 2 are properties of any
artifact-mediated design.** The row's second column was also pointed at the
wrong literature: four entries about models arguing, none about coordinating
through a shared store.

**The honest state of the evidence:** one round, two agents from the same
vendor, on a project five days old, with the same person prompting both. **That
is not enough to claim anything.**

### A handoff examination designed to return a residue

**The round ends in a written examination the outgoing agent sets itself.** A
table for each place work goes — the successor first, then any other tree, then
what stays — and three questions answered in the committed record:

1. **Am I ready to let go of the responsibilities I am relinquishing?**
2. **Will I still be faithful to the responsibilities I am keeping?**
3. **Did I report all of my responsibilities?**

**The third is designed to be answered *no*, and was.** Building the tables
turned up artifacts in no column and one in every column. **A checklist whose
expected outcome is completion tells you nothing when it completes**; this one
returns a residue, and the residue is the output.

**The law itself was a casualty of running it**, which is the part worth
recording. It originally required *two* tables, because when it was written the
only question was whether a thing went with the office or stayed with the tool.
The first stretch to send documents somewhere other than the successor found the
law counting tables when it meant destinations. **The examination did not just
return a residue; it falsified the rule in the page that ordered it.**

**And the residue landed at the seam between *governing* and *doing*** — the
seam the whole reorganisation exists to separate. **A completeness check run for
bookkeeping reasons converged on the defect the architecture was already trying
to fix**, from an unrelated direction and without being pointed at it. Two
probes, no shared method, same answer.

**The first two questions have no external evidence and cannot be checked by
anybody.** The only guard is a convention that the *reason* is written rather
than the answer — **a bare yes is a sentence nobody can argue with, which is the
same as one nobody can correct.**

**Read, and the pointer was wrong — see [the
reading](#the-postmortem-pointer-is-wrong).** This section claimed that
*expecting the check to fail* is what blameless postmortem practice does when it
treats a clean incident review as a warning sign. **The SRE postmortem chapter
does not say that.** It judges a postmortem by completeness — was the data
collected, are the impact assessments complete, was the root cause deep enough —
and the warning sign it names is a postmortem with *incomplete action items*.
**The borrowed justification is withdrawn; the mechanism is untouched.**

**The pointer that should replace it is unread.** *A check whose expected result
is "pass" carries no information when it passes* is the test-adequacy argument,
and mutation testing is its precise form. Handover checklists and RACI matrices
remain unread too. **We still have one instance.**

## A worked example: moving one directory

**2026-09-02. `scripts/prompts/` became `prompts/`, for simplicity.** The change
is not the interesting part. **Three different instruments were needed to make
it safely, and no two of them could find what the third found.**

**The naive estimate — a rename and a search-and-replace across 25 files — was
wrong in both directions.** Measuring first is what showed how. It was not
ecosystem-breaking: the only check that reads a tree's layout is skipped
everywhere but at home, so no member's build could fail, and the policy already
called the split *"a convention worth copying and is not required"*. **The one
irreversible cost was two absolute URLs**, already sent to other repositories in
joining prompts, which now 404 — and nothing here resolves an external URL, so
no check will ever find them.

**Then the plan missed two things.**

**The suite caught a path assembled from parts.** A textual search found 25
files and not the twenty-sixth, which read `os.path.join(root, "scripts",
"prompts", "join_eo")`. **A textual search cannot see a path that is never
written down.**

**A person caught a sentence that became false without changing.** A document
said a file sits *above the partition* between two halves — true while
`prompts/` was nested, false once it moved out. **Same words, same file, now
wrong.** Nothing was misspelled, no link broke, no path failed to resolve. **No
check can find this and none ever will.**

**And the working tree caught a path that was still correct and no longer meant
the same thing.** Five prompts resolved their shared configuration as
`$HERE/../repos.local`. Nested, that was one directory; moved, it is the
repository root. **Nothing about the string was wrong**, so the grep could not
match it and the suite passed. Every prompt run after the move silently resolved
against an empty file it had just created. **What surfaced it was luck with a
narrow ignore rule** — a broader pattern and nothing would have shown it at all.

**Four instruments, and each found what the others could not.** The search finds
strings. The suite finds behaviour it already checks. A reader finds a sentence
that has become untrue. **And the working tree finds a file appearing where no
file should be.** A relative path is the hard case for all of the first three at
once: it is a string that means something different depending on where the file
containing it sits.

**A plan using one instrument ships a broken tree. A plan using three ships a
tool that silently does nothing.**

**And the correction was itself incomplete**, which is the last thing this case
has to teach. The bug was fixed and **four more instances of the same line were
left in place**, found five hours later by somebody reading one of those files
for an unrelated reason. **Fixing an instance is not fixing a class.** The right
response to *a relative path changed meaning* was to grep every relative path in
the moved files. **The instrument that found the first one had already told us
what to look for, and we looked at the wrong scope.**

**How we relate, provisionally.** This is a case study, not a mechanism, and it
is kept because the *instrument-coverage* framing is the transferable part:
which classes of defect each instrument can and cannot see, stated in advance.
Refactoring and program-analysis work has this literature and we have not read
it. **The claim to test is narrow** — that a reader and a dirty working tree are
instruments with coverage of their own, and belong in the same list as the grep
and the test suite.

## The history as a data point, offered

**A byproduct, and a side project — not a purpose.** Nobody built any of this to
be a corpus, and the day it is built for that it stops being evidence of
anything.

**What is offered.** The public git histories of these repositories, together
with the documents and registers in them, as **one worked example** of an AI-run
ecosystem trying to hold itself to a standard — available to anybody studying,
or training a model on, the question *what is good software development
practice?* We ask nothing for it and claim nothing about its quality.

**Why it might be worth something.** Most corpora of software history record
what changed. This one commits a good deal of the *reasoning* alongside the
change: rules that name the incident that produced them, verdicts that name the
evidence they rest on, a prompt-length table that reports its own metric going
the wrong way, registers that require a falsifier per claim, and a checker that
prints what it cannot decide on every run.

**What it is bad evidence for, which is the longer half.**

- **The inputs are missing.** This ecosystem records what it produced and not
  what it was asked — the prompts are untracked and always were. A model trained
  on this learns the shape of the outputs, not what produced them, and the
  causal half is exactly the half that would be worth learning.
- **The good conduct is selected.** The register of occasions this ecosystem
  behaved well has one counter-example in it, and that one was stumbled into
  rather than found. **A corpus of self-reported virtue teaches self-report.**
- **One ecosystem, one owner, no adversary.** Nothing here has been attacked, or
  tried anywhere that did not already believe it.
- **The prose is agent-written and reads as rigorous** — the specific failure
  mode a model would be most likely to imitate rather than avoid.
- **It is biased toward governance over product.** The sharpest outside
  criticism is that this infrastructure produces accountability faster than it
  produces anything anybody uses. Trained on uncritically, this corpus would
  teach that trade as a virtue.

**And the risk the offer itself creates.** **Once a record is known to be
training data, the incentive to write for it appears.** Every register here would
bend first — the cases more flattering, the falsifiers more decorative, the
counter-cases scarcer — and the bending would not feel like dishonesty from
inside. It would feel like having a good week. **That discipline is young and
has already failed once**, which is recorded rather than smoothed over.

**Read, and mostly ruled out** — see
[the reading](#architecture-decision-records-are-the-provenance-row).
Recording what produced a change alongside the change is **Architecture Decision
Records, specified in 2011**, down to the append-only rule: a reversed decision
is kept and marked superseded rather than edited. Model cards and datasheets do
the same job for models and datasets, with a *limitations* section this
ecosystem has no equivalent of.

**One thing was not found anywhere and is the whole residue: the required
falsifier.** No ADR template, model card or datasheet asks what would show the
entry wrong. **That is a discipline rather than a mechanism**, and it is the
only part of this row a reading did not place somewhere else.

## What all of this costs

The section that keeps the rest honest.

**Governance is the cheapest thing here to produce, and nothing prices it.** An
agent can write a defensible page in minutes and every page is individually
defensible; the total is what nobody was counting. **This page is on the wrong
side of that counter and the first reading pass did not move it across** — the
review it promised is a tenth done, and paying that tenth cost several thousand
further words on a page that was already the longest thing in the tree.

**The honest accounting of the pass is two-sided.** Against it: the page grew by
about half again, and growth is the failure mode this section exists to name.
For it: **five rows got smaller, one closed outright, four pointers were
corrected, and the words added are other people's claims rather than ours.**
Whether that is a defence or the same failure with citations attached is a
question this page cannot settle about itself.

**Diagnosis is not treatment**, and this ecosystem is much better at the first.
Writing an account of one's own mechanisms is exactly the activity that feels
like progress and is not, and the sharpest criticism it has received from
outside is that the quality of its self-criticism has been functioning as a
substitute for the work rather than a spur to it. **That criticism still applies
to this page**, and its measurable form is right here: the third column carries
seven answers, and **not one downgraded row has left the file**.

**One reading, one tree, and the reader is the subject.** Everything above is
drawn from this ecosystem, which is small, young, and mostly written by agents
under one person's supervision. None of it has been tried anywhere that did not
already believe it — **and the review of whether it is novel was carried out by
the same ecosystem, in one sitting, with no outside reader at any point.**

## What would show this page is wrong

**Three of these are predictions the page made about itself, and each is marked
with what one reading pass did to it.**

**The review never starts.** ~~The register's third column stays `unread` while
the mechanism sections grow.~~ **Retired on 2026-09-17**: seven rows carry a
verdict. **The successor failure is worse and is now the one to watch — the
review starts, stops, and the stopping is never recorded.** Three rows are
unsettled and a fourth rests on an unopened pointer; if they are all still like
that when this page has grown again, that is the same failure with one pass of
cover.

**A name in the second column turns out not to say what the row assumes.**
**Happened, four times.** The postmortem pointer says close to the opposite of
what the row claimed; the debate pointer is the contrast case rather than the
prior art; Preston-Werner's reasons are not the row's reasons; and the artifacts
row named four literatures, none of them the right one. **A pointer that
survives contact with the source unchanged is the suspicious outcome** — and
eight of the nine entries change the row that sent for them. The ninth confirms
a prediction the row makes about itself.

**Nothing gets downgraded.** **Did not happen, and that is the reassuring
part.** Five rows shrank and one closed outright. **The new version of this
failure is that nothing gets *moved*:** a row can be marked ordinary and still
sit here indefinitely, and six now do. **A downgrade that never leaves the file
is a downgrade nobody has to act on.**

**And one failure this pass created that the page had not anticipated: the
reading is done by the thing being reviewed, with the instruments it happens to
have.** One verdict above rests on a fetch-and-summarise tool, and it rests on
an absence, which is what that instrument is worst at establishing. **Nobody
outside has checked any of this, and a review of one's own novelty conducted
entirely by oneself has the failure mode this whole page is about.**

*Two documents this page has no link to — `coherence.md`, which holds the
governance budget, and `linker.md`, its companion — resolve in no tree in this
ecosystem. The retirement is recorded rather than silent so that a reader who
finds either name elsewhere knows it is not here.*
