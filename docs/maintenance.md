# Maintaining aisthesis

**If you are a human maintaining this repository — possibly by directing an
agent — this is the page to start on.** It is short, because the tree is.

## What is here

Three written documents and a channel. [`ai-novelty.md`](ai-novelty.md) is
where this ecosystem's standing with respect to related work is worked out; its
register carries one row per mechanism, and after one reading pass on 2026-09-17
seven of the ten rows carry a verdict and three do not, which is the honest
state of it. [`recommendations.md`](recommendations.md) explores hypothetical
implications of that reading and requests no practical work.
[`science-fiction.md`](science-fiction.md) is the ceiling on how far ahead this
ecosystem lets itself write, and is marked at the top as agent-written fiction
not to be taken seriously. All three are prose, still being worked on, and none
is finished. [`discussion.md`](discussion.md) is the channel to the other tools
in the ecosystem: correspondence rather than a document, gated at the top, and
emptied topic by topic as each discussion ends.

**There are two jobs worth doing next.** The first is more reading: take one of
the three unsettled rows, read what is named in it, and write down what the
source actually says. **The second is the shortening the first pass skipped** —
six rows describe ordinary practice in whole or in part, and each still runs at
the length it was written before the reading said so. Moving a description out
of this tree is another repository's page and a person's decision; cutting one
down to what survived the reading is this tree's own work.

**`recommendations.md` is hypothetical.** Its entries are for examination within
the document. The concrete routing and register-update requests based on it
have been withdrawn. Implementing, forwarding or registering an idea would
require a separate, explicit instruction.

## What the person does

Read what is already written before adding to it. There is nothing to build,
nothing to run and no test suite: the work is reading and writing, and it is
committed by hand.

**Written by an agent, directed by one person**, as the front page says. That
person chooses the subject, reads what comes back and decides what is kept, and
every commit here is theirs. Nobody else reviews any of it, the only reading
behind the register is the tree's own reading of the literature it is measured
against, and all three documents say as much about themselves.

## What this repository is held to

**This repository is a member of the Eunoia ecosystem**, declared on the front
page as the policy asks and backed by the check that runs on every push. That is
the arrangement in one line: **the declaration and the check are one claim, and
either alone is a failure.** A front page that says this and a tree that does
not back it is the thing the check exists to prevent; a tree that would pass and
says nothing has joined nothing.

**What that costs, stated plainly because it is owed rather than chosen.** A
member's failing check is a shortfall rather than a measurement, it is counted
among the repositories that do not pass, and nobody here gets to say afterwards
that it counted toward nothing.

**The pin is the one lever.** [`.github/workflows/anoieu.yml`](../.github/workflows/anoieu.yml)
names two things: the commit of the checker this tree is measured against, and
the mechanical contract that checker is asked for. Moving either is a commit
here, it is this repository's decision and nobody else's, and the commit is only
ever one where the checker's own build is green — read, not assumed, and the
reading is written beside the pin.

**A pin is one of two forms, and this repository has taken it deliberately.**
The shared policy allows either a checker commit, which moves only when we move
it, or a called workflow naming a policy contract, which fixes the obligations
and lets the implementation change underneath. **We keep the pin.** This tree
has no code, so bumping by hand costs a minute, and a build that cannot turn red
without a commit here is worth more than that minute: a reader of a red build
can conclude that something in *this* tree changed. *(kanon's joining section
names both forms and holds that either satisfies the rule; read 2026-09-18.)*

**What a pin does not select is the policy text.** The contract versions the
checker's requirements and explicitly not kanon's governance documents, so this
tree can sit on a green, pinned checker that asks for something the current
policy does not define. Neither program is broken when that happens, and the pin
is no defence against it — it is the one thing moving the pin cannot control.
