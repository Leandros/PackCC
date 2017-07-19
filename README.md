# PackCC

PackCC is a packrat parser generator for C. Its defining features are:

- Generates your parser in C from a grammar described in a PEG
- Gives your parser great efficiency by packrat parsing
- Supports direct and indirect left-recursive grammar rules

Some additional features include:

- Thread-safe and reentrant
- Generates compact and readable source
- Consists of just a single compact source file
- Licensed under MIT


The algorithm is based on the paper "Packrat Parsers Can Support Left Recursion"
authored by A. Warth, J. R. Douglass, and T. Millstein.


# Installation

PackCC consists of just a single compact source file `packcc.c`.
To create the executable, just compile it:

```
cc -o packcc src/packcc.c
```

# Usage

You must prepare a PEG source file (see the documentation).
In our example the file is named `example.peg`:

```
packcc example.peg
```

By running this, the files `example.h` and `example.c` are generated.

If no PEG file name is specified, the PEG source is read from the standard
input, and `-.h` and `-.c` are generated.

The base name of the parser source files can be changed by -o option.

```
packcc -o parser example.peg
```

By running this, the files `parser.h` and `parser.c` are generated.


# Documentation

The `docs/` directory contains the full documentation.
Alternative, it's accessible at https://leandros.github.io/packcc

# License

MIT License

Copyright (c) 2014 Arihiro Yoshida
Copyright (c) 2017 Arvid Gerstmann

