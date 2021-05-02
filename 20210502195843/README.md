# Better PEG Grammar Notation and Tooling

[[*Hey look! We actually made this!*]](https://pegn.dev)

PEG ([Parser Expression Grammar](https://duck.com/lite?kae=t&q=Parser
Expression Grammar)) is by far the most important advance in language
grammar development in the last 20 years (even though many CS
departments still don't even talk about it in their curriculum). The
ecosystem around PEG is fractured and full of over-engineered code
generators that are implementation language specific. What we need is a
standardized notation based on Bryan Ford's original (but incomplete)
"example" in his paper that started it all. Then we need to show that
tooling can exist --- including code generators --- that simply use the
grammar and don't intermix PEG with additional syntax to render in a
specific language. That way the same grammar files can be used to
generate parsers of different kinds in different languages. The same
grammar file could be used to generate a highly optimized parser within
a single file or another that uses very flexible AST approach and parse
function library.

PEG is particularly useful in computer science education not only to
create grammars, but to document existing ones and get the mind to
understand what syntax is as well as any specific syntax. Capturing an
existing language in PEG is a great educational exercise.

