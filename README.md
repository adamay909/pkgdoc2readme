## Overview

Pkgdoc2readme turns the package comment into a README.md file. In general, the package comment should be in a single file, like doc.go, but if there are multiple files with package comments, the comments will be concatenated in the default sort order of the file names.

The only comment included in the README.md file is the package comment (the part that godoc shows under  the heading 'Overview'). Exported identifiers and stuff are left to godoc and pkgsite.

Unlike other more capable tools, pkgdoc2readme only inspects the go sources in the current directory (no subdirectories).  Nor does pkgdoc2readme add any functionality to what is available in go/doc/comment or offer any control over the output. If you need those more advanced features, do use another tool. Googling will find you plenty.

The best way to use this tool is to add a go:generate directive in one of the source files and to run go generate. Look at the source file of this tool for an example.


