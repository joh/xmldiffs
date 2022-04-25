# xmldiffs
Compare XML files semantically, ignoring element and attribute order.

Usage: `xmldiffs [OPTION] FILE1 FILE2`

# How does it work?
xmldiffs first parses each XML file and spits them out sorted by
element (tag) name and attributes. The result is then passed
to `diff` for a semantic XML comparison.

# Command line options

* `-u`, `--unified` - produce unified diff.  This is the default mode.
* `-c`, `--context` - produce context diff.
* `-n`, `--ndiff` - produce Differ-style delta.
* `-t`, `--html` - produce HTML page showing line by line differences.
* `-d`, `--diff` - run the **diff** program to compare normalized texts.
  Any options not described here are added to the diff command line.
* `-l`, `--lines` - Number of the context lines for unified, context,
  and html diffs.  For unified and context diffs, the value defaults to 3.
  For html diff, the value defaults to *None*, which produces
  full output lines.  Pass an integer to produce context lines.
* `-o`, `--output` - Name of the output file.  Default value is
  minus sign, which prints the diff to the *stdout*.
* `-x`, `--xml` - instead of comparing two xml files,
  write sorted contents of `FILE1` to `FILE2`.
  In this mode the `--output` option is ignored.
