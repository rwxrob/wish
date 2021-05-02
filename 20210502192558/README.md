# Go Template Utility `gotmpl`

[[*Here look I even started the repo for you.*]][gotmpl]

[gotmpl]: <https://github.com/rwxrob/gotmpl>

It occurred to me that Go is actually the perfect language to write a
little `gotmpl` utility that reads from a collection of cached templates
(both `text` and `html`). Sometimes all I want is the lower of Go's
templating system for random things and usually just want to combine
them with some YAML or JSON or just a list of stuff on the command line.

I could use it to manage snippets from within a `vi` session. Some of my
my favorite methods to add to a simple data struct:

* `String() string` - the `Stringer` interface as JSON
* `JSON() []byte` - compressed JSON buffer
* `Print()` - `fmt.Println()` of the string JSON
* `Parse(jsn64 []byte) error` - JSON (optionally base64 encoded)
* `Load(path string) error` - `ioutil.ReadFile()` then `Parse()`
* `Base64() []byte` - `JSON()` in base64 encoding

I should probably also make something that creates the `Example*` test
cases as well. Actually, I should just do one `ExampleData()` (or
whatever) and then just include a bunch of examples of using all the
related methods.

