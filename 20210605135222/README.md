# Direct Port of `jq` to `yq`

The `yq` project is definitely a step in the right direction but has
over 500 issues currently and really no sign of significant activity. It
also has made a number of very dubious design decisions fro the start
and does not appear to have been coded by someone who has core knowledge
of Go. Many of the idioms used are anti-patterns. Currently, it is the
only other than that God-aweful Python variant. But we can do better, a
lot better. The question is putting in the time to do it.

## 100% `jq` Compatibility

The `jq` utility is clearly the leader in this space. Millions of lines
of production software depend on it. One for one compatibility with `jq`
is therefore the goal. There is nothing stopping us from porting the
`jq` C source *directly* instead of trying to emulate it. That would
make it much easier to keep up with the `jq` project and keep the ports
one-to-one as we maintain it. 

The current version of `yq` has little annoyances like requiring `e`
instead of just using the default.

## Probably Coded in C, not Go (Definitely NOT Rust)

This is a tough one. The entire Kubernetes world depends on the same
stuff that `yq` uses. The `yqlib` is not directly used by `kubectl` but
it could be.

The Go version might have been faster to write, but it has several major
design flaws:

1. Multiple layers of package dependency and indirection
1. Depends on JSON reflection
1. Way slower on every level than `jq`
1. Unnecessary support for *full* YAML instead of just JSON

Someone needs to write a baseline YAML (compatible with JSON) parser in
C. Perhaps one that could be documented in [PEGN](pegn.dev). Then all
the translation between JSON and such could go away. But, since YAML
is required to be compatible with JSON we already have the start of
that parser written within the `jq` project. That core library is what
the world really needs. Then, one that parses the syntax of filters
would be next.

## I Really Want to Write This

This is an idea project for me to really put PEGN to the test. I could
even implement a parser and compiler in C for PEGN to go with the one
we have in Go already. That would put PEGN on par with the `pegleg`
project. I wish I had time to work on all this. Maybe over the Christmas
holidays. God knows I need to get my C skills back up to par. It's been
more than 10 years.
