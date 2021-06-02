# Port `tmatrix` to 100% Golang CmdBox Utility

I love `tmatrix`. I really do. But the installer is hit or miss and the
documentation is in a (commendable) man page and completion is separate.
I'd love to create an identical version in Go that has all that built
into the command using the CmdBox commander. It would be a really fun
project for someone wanting to get further into Go for terminal. I would
use the `curses` compatibility layers at first, but consider something
else eventually that doesn't depend on it being installed. God knows Go
has the built in Unicode support for the Kanji characters it uses.
