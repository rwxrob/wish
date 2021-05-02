# Replacement for Find with a Good Query Language

The `find` command is an essential tool for system administration ---
particularly for disk usage and security audits --- but the syntax of
the arguments has always been ridiculously difficult to remember
requiring multiple references to the man page.

Wouldn't it be cool if we came up with `find` replacement that has a
drop-dead simple query language (maybe even just SQL) that it read
either as a single string or passed into standard output, or just placed
in a file with a she-bang line pointing to it. It would be an *actual*
language for finding things on your system (no not like `awk` or `sed`).

One approach would be simply to create temporary SQLite flat-database
files on the fly and a light-weight interface to them so that existing
SQL tools could be used. This is something that could be done rather
quickly. By having different SQLite files created queries could be made
across databases to determine changes in the file system.

