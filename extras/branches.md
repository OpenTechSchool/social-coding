---

layout: ots
title: Branches

---

Branching is one of the most powerful, and perhaps perplexing, topics
in source control with git. In this section we'll use an example git
repository to play with branches and get a feel for their power.

# As if!

We've created a little git repository with about 500 years of history
called [as-if](https://github.com/stevenfarlie/as-if).

The format is simple. One file per century, with each line starting
with a year and some facts (or, should we say, "facts"?).

> 1625: New Amsterdam founded by the Dutch West India Company in North
> America.

The `master` branch contains the "official" history. This is the plain
normal stuff. But for the "real" history, stuff that we know is true,
we create a topic branch off of `master` and commit there.
