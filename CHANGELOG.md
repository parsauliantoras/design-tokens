# Changelog

## 0.1.0 (2026-10-17)

- `base.css` moved from torasparsaulian.com, from commit
  8869549c8cf5c004052d48d5eca56be4f827e03b (the last commit that changed its `tokens/`
  folder). Values unchanged; comments now say what a site must set instead of naming the
  sibling's files.
- New: `--font-family-mono` with "Mono Fallback", `--space-1` to `--space-8`,
  `--duration-step-min`, `--duration-step-min-reduced`, `--duration-ui`, `--size-hit-min`.
- Fonts: Bricolage Grotesque and Geist moved (OFL); JetBrains Mono 400 added (OFL), the monospace
  face chosen for Pipeline Lab (its ADR-0023).
- New: `--size-border`, `--size-hairline`, `--size-focus-ring`, `--radius-1`, `--radius-2`,
  `--radius-round`, `--grey-950-scrim`.
- New: `--size-list-max`.
- New: `--measure-wide` (a wider column for two-column pages on desktop).
- New: `--white`, `--grey-500`, `--grey-550`, and the ramps `--blue-*`, `--green-*`, `--red-*`,
  `--amber-*` (100–900; red also 200 and 800).
