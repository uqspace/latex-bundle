# `The Meta` LaTeX Package

A simple package for storing nested meta-data, which can be accessed at any
point in the document using the `\The` macro.

## Usage

Storage of meta-data is done using the `setup` environment.

```latex
\begin{setup}
    foo = {Some data},
    bar = {More text}
\end{setup}
```

This data can then be accessed as `\The{foo}` and `\The{bar}` respectively.
If the given argument does not have data stored, the macro will either expand
to a default, passed as an optional value, or simply `???`.

To check whether the given argument has associated data, use the `\ifThe`
macro. This works similar to `\if`, and takes a single mandatory argument.