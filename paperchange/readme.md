# LaTeX `paperchange` Package

Allows for the changing of the page size and / or orientation in the middle of
a document. This package also is a sister package to the `comments` package, or
any package which uses the margin to add comments, by allowing for an expanded
margin *outside* the standard page size.

### Macros:

- `setpagesize[<geometry options>]{<paper size>}[<orientation>]`

    1. The optional `geometry options` allows extra arguments to be passed into
       the macro which control the page attributes. These are simply passed
       through to the `geometry package` before calculations are made.
    2. `paper size` is the selected paper size, using the standard designation.
       *Currently this is limited to `A3` and `A4`.*
    3. `orientation` allows the paper to be switched between `port` (default)
       and  `land`. Text is always maintained as horizontal when viewing.

- `restorepagesize`

    Resets the page size to the original size when the document began. This
    macro can be called redundantly without slowing down compilation.

### Package options:

- `margin-comments`

    Enables the expanded margin beyond the standard page size.
    `(`**`true`**`|false)`

- `printed`

    Prints landscape pages with headings and footers perpendicular to the
    standard A4 edge, to maintain consistency when printed.


## Roadmap:
- [ ] Package documentation
- [x] Full package options
- [x] Compatibility with ~~margin notes~~ `comments` package
- [ ] Restrictions and options for printed / bound documents
  - `v2.0.0` Added option for rotating compatible with printing / binding
  - [ ] Restrict page sizes when printing / binding
- [ ] Add compatibility for `LuaLaTeX`

> **WARNING** :
> Currently this package is still in development, and as such has certain
> features are missing / incomplete. This package will not be pushed to CTAN
> until it is considered more mature.