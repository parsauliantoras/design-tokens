# @torasparsaulian/tokens

The base layer of the design tokens shared by torasparsaulian.com and Pipeline Lab: raw values
with neutral names (greys, font families with measured fallback faces, weights, a type scale,
spacing, motion, sizes) and the font files.

## Base and semantic

Tokens come in two layers:

1. **Base (this package)** holds raw values with neutral names, such as `--grey-600` or
   `--space-4`. It says nothing about what a value is for.
2. **Semantic (in each site)** gives roles to base tokens, such as `--color-text`. A semantic
   token refers to base tokens only; it never holds a raw value.
3. **Light and dark** are set in each site's semantic layer, not here.

## Install

Pin one tag in the site's `package.json`, so a token change reaches a site only when that site
moves its pin:

```json
"@torasparsaulian/tokens": "github:parsauliantoras/design-tokens#v0.1.0"
```

Import `@torasparsaulian/tokens/base.css` once, before the site's semantic layer. Load the fonts
from `@torasparsaulian/tokens/fonts/` (in Next.js with `next/font/local`).

## What a site must set

`base.css` declares each font stack with a `--font-*-loaded` variable first. A site's font
loader sets these variables on the root `<html>`, because a token is resolved where it is
declared:

| Variable | Face | Stack |
|---|---|---|
| `--font-display-loaded` | Bricolage Grotesque | `--font-family-display`, `--font-family-display-text` |
| `--font-body-loaded` | Geist | `--font-family-body` |
| `--font-mono-loaded` | Geist Mono (400) or JetBrains Mono (400); both files ship, a site loads one | `--font-family-mono` |

A site that loads the body font on one page only may set `--font-body-loaded` on a wrapper with
`data-body-font` instead; `base.css` redeclares the body stack there.

## How to add a token

- One line per token in `base.css`, with a neutral name.
- Give the reason in the commit message, and add a line to `CHANGELOG.md`.
- Release it as a new minor tag (`v0.2.0`). Renaming or removing a token is a new major tag.

## Licence

The CSS is under the MIT licence (`LICENSE`). Each font file keeps its own SIL Open Font
License; see `fonts/README.md`.
