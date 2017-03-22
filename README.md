# xmldiffs
Compare two XML files, ignoring element and attribute order.

Usage: `xmldiffs [OPTION] FILE1 FILE2`

Any extra options are passed to the `diff` command.

# How does it work?
xmldiffs first parses each XML file and spits them out sorted by
element (tag) name and attributes. The result is then passed
to `diff` for a semantic XML comparison.
