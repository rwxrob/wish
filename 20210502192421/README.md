# JSON Schema to Protobuf Converter

The world (since 2019) is apparently going all gaga for gRPC and
its Protocol Buffer interface definition language (IDL), and, I'm
thinking, for good reason. I have *really* enjoyed working with it, much
more than I would have imagined having PTSD for all things RPC from
previous decades. In fact, I plan on doing everything in Protobuf for
new projects now because it generates the most important code in a
code-agnostic.

That said, there is a bunch of stuff already specified in JSON-Schema
that would be really nice to just convert over to `.proto` files. Such a
tool does not exist so far that I can find.
