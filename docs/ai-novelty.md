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

**The literature has not been surveyed yet. This page is one half of a
comparison.** Saying so first is not modesty; it is the difference between a
review and a description of ourselves with the word *review* on it.

**What exists here today:** the ecosystem side, written up mechanism by
mechanism, with each one naming the outside work it would have to be measured
against and what that measurement would have to establish.

**What does not exist:** the reading. No entry below has been checked against a
source. **The names in the *nearest prior art* column are pointers for a review,
not citations** — they say where to look, and a reader should treat any of them
as unverified until somebody reads the thing and writes down what it said.

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

**Nothing has been ruled out yet**, which is a fact about the review not having
started rather than about the contents.

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

One row per mechanism. **The third column is the state of the comparison, and it
reads `unread` everywhere**, which is the accurate summary of this page today.

| mechanism | nearest prior art to read | comparison |
| --- | --- | --- |
| [documentation as the thing you are aided by](#clear-writing-is-what-makes-this-fast) | literate programming; docs-as-code; README-driven development; the *context engineering* line of work on agentic coding systems | unread |
| [a kernel document nothing may check](#visionmd-is-the-kernel) | constitutional and rule-based steering of agents; policy hierarchies in governance; the specification/implementation split | unread |
| [a citation as a compiler optimization](#a-clear-reference-is-a-compiler-optimization) | retrieval over a project corpus; transclusion and single-source publishing; design by contract | unread |
| [prose defects as a propagating hazard](#writing-documentation-is-coding-reading-it-is-debugging) | prompt injection and instruction-shaped input; supply-chain integrity for text; documentation drift studies | unread |
| [scripts are ground truth, and the gap is checked](#scripts-are-the-ground-truth) | executable specifications; doctests and literate testing; drift detection between spec and code | unread |
| [a pinned, fetched, opt-in checker](#the-build-system-can-be-generalized-and-has-not-been) | dependency pinning and lockfiles; reproducible builds; supply-chain provenance frameworks | unread |
| [artifacts as the only channel between agents](#the-artifacts-are-the-channel) | multi-agent debate; self-critique and revision loops; LLM-as-judge; ordinary adversarial review | unread |
| [a completeness check expected to fail](#a-handoff-examination-designed-to-return-a-residue) | handover checklists; RACI matrices; blameless postmortems; incident review practice | unread |
| [recording what produced a change, not only the change](#the-history-as-a-data-point-offered) | commit trailers and sign-off conventions; model cards and datasheets; provenance and attestation work | unread |
| [a checker that prints what it cannot decide](#what-all-of-this-costs) | coverage reporting; known-unknowns in static analysis; model cards' *limitations* sections | unread |

**The last column is the whole point of the page** and it is empty. Every row is
a question, and none is an answer.

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
that risk in the tree**, which is why its register column reads `unread`.

**A citation is a reference; a paraphrase is a copy.** Copies are the thing this
repository is most careful about — a prompt copied out of the document defining
it, a command table restated on a second page, a policy forked instead of
referenced. Each is a second definition of one symbol, and the failure is always
the same: they diverge, and the divergence is invisible from the side that
matters. Where a copy has to exist, something compares it; where it does not
have to exist, a reference is strictly better.

**How we relate, provisionally.** This is single-source publishing and
transclusion, argued in compiler vocabulary. **Retrieval over a project corpus
is the agent-era version of the same trade** — fetch the authoritative text
rather than restating it — and the comparison worth making is whether the
*failure mode* framing (a missing symbol at load, found by the reader) adds
anything to what retrieval work already says about stale and wrong context.

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

**How we relate, provisionally.** This is the same shape as instruction-shaped
input arriving in a system that reads text and acts on it, which the prompt
injection literature has worked on directly and at length; and the *propagates
into trees that pinned us* half is a text supply-chain problem, which provenance
and attestation work addresses for artifacts rather than for prose. **The review
question is whether prose-that-is-adopted needs anything those two do not
already give**, and the honest prior is that it does not.

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
`--show-prompt`, and compares whole bodies; the same comparison runs over the
places that restate the epoch commands and statuses against the tables that
define them. **Ground truth with copies and no comparison is the worst of the
three arrangements, because it looks like the safe one.**

**Where it is not true yet, and this is the honest half.** The epoch system's
commands are not parsed by any program. Nothing rejects a malformed one, nothing
enforces a gate, and the role that holds the front end says so in its own entry.
For that system the ground truth is currently a *document*, which is the
arrangement this tenet exists to warn about. Naming it here does not fix it.

**How we relate, provisionally.** Executable specifications and doctests are the
established form of *the document and the program must agree, and a test says
so*. The comparison to make is narrow and answerable: whether comparing **whole
bodies** rather than behaviour catches a class those approaches miss, or is
simply a cruder instrument that happens to fit prose.

*What would show this false:* a drift check being narrowed to a substring match,
which is how this class of comparison usually dies quietly.

## The build system can be generalized, and has not been

The concrete wish, stated as a wish because nothing has been built.

**Today the epoch commands exist in one repository.** Reaching `staged` is
something only that tree can currently do, because the machinery and the surface
a person types at both live there. Every other member has the policy checker and
the reporting loop and nothing else: no command line of its own, no staging
step, no dry run.

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

**How we relate, provisionally.** All four are dependency management as
practised everywhere: lockfiles, pinned revisions, and the reproducible-builds
argument that a build which can change without a commit is not evidence about a
commit. **There is nothing to claim here and the review should say so plainly.**
The only part that might not be ordinary is that the pinned dependency is a
*judgement about your repository* rather than a library — and the nearest
outside analogue for that is supply-chain attestation, which is worth reading
before claiming a difference.

*What would show the generalization is real:* a second tree running one of these
commands that it did not write, against its own state, and getting an answer its
maintainer acted on. Nothing has done this. **A build system with one user is a
script with ceremony.**

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

**How we relate, provisionally, and this is the row most likely to collapse.**
Multi-agent debate, self-critique and revision loops, and LLM-as-judge are all
established forms of *two model instances disagreeing productively*, and plain
adversarial review is the human version. **The only candidate difference is that
the artifacts are the sole channel** — no shared transcript, no shared memory,
no write access to each other — which makes the disagreement durable and the
audit trivial. The specific question for the review: does any existing
multi-agent setup already restrict the channel to committed artifacts, and if
so, did it report the same three consequences?

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

**How we relate, provisionally.** Handover checklists are ancient and
partitioning responsibility into a table is what a RACI matrix is; *expecting
the check to fail* is the move blameless postmortem practice already makes when
it treats a clean incident review as a warning sign. **The specific things to
test** are whether asking an agent to declare what it is *not ready to release*
produces anything a plain inventory does not, and whether expected-to-fail is
more than honest wording on an ordinary checklist. **We have one instance.**

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

**How we relate, provisionally.** Recording *what produced a change* alongside
the change is what commit trailers and sign-off conventions already do at small
scale, and what model cards and datasheets do for models and datasets: a
structured statement of what a thing is, how it was made, and what it does not
cover. **The review question is whether a repository-scale version of that —
reasoning committed beside the change, with falsifiers required — exists
already**, and if it does, whether anybody found it worth the cost.

## What all of this costs

The section that keeps the rest honest.

**Governance is the cheapest thing here to produce, and nothing prices it.** An
agent can write a defensible page in minutes and every page is individually
defensible; the total is what nobody was counting. **This page is on the wrong
side of that counter** — it is written prose, it displaces nothing yet, and the
thing that has to pay for it is the review it promises and has not done.

**Diagnosis is not treatment**, and this ecosystem is much better at the first.
Writing an account of one's own mechanisms is exactly the activity that feels
like progress and is not, and the sharpest criticism it has received from
outside is that the quality of its self-criticism has been functioning as a
substitute for the work rather than a spur to it. **That criticism applies to
this page more than to most**, and the register's empty third column is the
measurable form of it.

**One reading, one tree.** Everything above is drawn from this ecosystem, which
is small, young, and mostly written by agents under one person's supervision.
None of it has been tried anywhere that did not already believe it.

## What would show this page is wrong

**The review never starts.** The register's third column stays `unread` while
the mechanism sections grow. That is this page becoming the thing it replaced —
a description of ourselves with a comparative title — and it is the most likely
failure by a wide margin.

**A name in the second column turns out not to say what the row assumes.** Each
is an unverified pointer, and the first reading pass should be expected to
correct several of them. **A pointer that survives contact with the source
unchanged is the suspicious outcome, not the reassuring one.**

**Nothing gets downgraded.** If a full reading pass moves no mechanism out of
this file, the filter is not working — the prior is that most of these are
ordinary practice arriving somewhere new, so a review that confirms every row is
measuring the reviewer rather than the rows.

*Two documents referenced by earlier versions of this page — `coherence.md`,
which held the governance budget, and `linker.md`, which this page was once a
companion to — no longer resolve in any tree in this ecosystem. Recorded here
rather than silently dropped: the references were removed on 2026-09-17 and the
pages they pointed at have not been located.*
