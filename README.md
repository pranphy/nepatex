![](images/logo.png)

# Introduction
This is a very small single file that helps in typesetting documents in Nepali (devanagari in general) with $\LaTeX$ with the latest `lualatex` engine. Various sensible defaults have been used to make the document readable in Nepali.

# Installation

Since this is a single `.sty` file, it can be easily installed by putting the file `package/nepali.sty` into your `texmf` tree. You can either put this into the same directory as your latex document or in any location in the texmf tree. A common location in unix-like os is under `~/texmf/tex/latex`

```bash
$ git clone https://github.com/pranphy/nepatex.git
$ cp nepatex/package/nepali.sty ~/texmf/tex/latex/
```

# Usage

To use the package simply use this in preamble

```latex
\usepackage{nepali}
```

The default date command `\today` is renewed to print date in BS calendar system. It will print current date in the format `२०७८ फागुन ४`. And additionaal command `\nepdate` is available which also prints the current date. So you can use.

```latex
आजको मितिः \nepdate हो।
```

which will produce

> आजको मिति २०७८ फागनु ४ हो।

# Demo

A sample demo is available inside the `demo` directory. To compile it 

```bash
$ cd neplatex/demo
$ lualatex nepali-demo.tex
```

This package uses lua code in lualatex so can only be compiled with lualatex. You should anyway be using `lualatex` for compilation. One more reason to use lualatex if you want to typeset document in nepali using $LaTeX$.

A demo pdf is also included. You can open with your favourite pdf reader

```bash
$ zathura nepali-demo.pdf
```

