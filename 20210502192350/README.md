# Protobuf Vim Plugin That is Syntax Aware

Currently, the Vim file type of `proto` is supported out of the box, but
the syntax is not using an AST of any kind (it appears) so it can't do
things like line up in-line comments and stuff I've come to love about
`vim-go`. This is probably the type of project I want to work on *after*
finishing PEGN so that I can define the grammar of the syntax in PEGN
and auto-generate a Vim plugin in Go that handles the AST.

