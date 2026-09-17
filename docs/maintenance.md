# Maintaining aisthesis

**If you are a human maintaining this repository — possibly by directing an
agent — this is the page to start on.** It is short, because the tree is.

## What is here

Two written documents and nothing else. [`ai-novelty.md`](ai-novelty.md) sets
out to review the literature on state-of-the-art AI systems and say how this
ecosystem relates to it; its register carries one row per mechanism and the
comparison column is empty, which is the honest state of it.
[`science-fiction.md`](science-fiction.md) is the ceiling on how far ahead this
ecosystem lets itself write, and is marked at the top as agent-written fiction
not to be taken seriously. Both are prose, still being worked on, and neither is
finished.

**The one job worth doing next is the reading**: take a row of that register,
read what is named in it, and write down what the source actually says. Rows
that turn out to describe ordinary practice leave the file, which is the point
of keeping them in one.

## What the person does

Read what is already written before adding to it. There is nothing to build,
nothing to run and no test suite: the work is reading and writing, and it is
committed by hand.

**Written by an agent, directed by one person**, as the front page says. That
person chooses the subject, reads what comes back and decides what is kept, and
every commit here is theirs. Nobody else reviews any of it, nothing here has
been read against the literature, and the two documents say as much about
themselves.

## What this repository is held to

**This repository is a member of the Eunoia ecosystem**, declared on the front
page as the policy asks and backed by the check that runs on every push. That is
the arrangement in one line: **the declaration and the check are one claim, and
either alone is a failure.** A front page that says this and a tree that does
not back it is the thing the check exists to prevent; a tree that would pass and
says nothing has joined nothing.

**What that costs, stated plainly because it is now owed rather than chosen.**
This repository previously carried the `associate` footing — held to the same
policy by its own choice, owing the ecosystem nothing, with the obligation
recorded here instead of on the front page. **That is no longer the arrangement.**
A member's failing check is a shortfall rather than a measurement, it is counted
among the repositories that do not pass, and nobody here gets to say afterwards
that it counted toward nothing.

**The pin is the one lever.** [`.github/workflows/anoieu.yml`](../.github/workflows/anoieu.yml)
names the commit of the checker this tree is measured against. Moving it is a
commit here, it is this repository's decision and nobody else's, and it is only
ever moved to a commit where the checker's own build is green.

**What is not settled from this side.** The ecosystem's register in kanon
records one footing per tool, and `aisthesis` has no entry in it and no name in
the glossary. **Declaring is this repository's half; being recorded is kanon's**,
and the second has not happened.
