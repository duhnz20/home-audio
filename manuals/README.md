# Manuals — local storage

This directory holds **PDF manuals, spec sheets, and setup guides** for the home audio equipment. The PDFs themselves are gitignored (`manuals/*.pdf`) and exist only on the local clone — they are **not** pushed to Gitea or mirrored to the public GitHub repo.

## Why PDFs are gitignored

- **Copyright:** redistributing manufacturer PDFs in a public repo (GitHub mirror) is a grey area
- **Repo size:** AVR + amp + speaker manuals can total 100+ MB; bloats clone time and exceeds GitHub's recommended repo size

The **index** of which manual goes where, plus links to each manufacturer's official PDF source, lives in [`../manuals.md`](../manuals.md) at the repo root.

## File-naming convention

Use the format used in `manuals.md`'s "Local filename" column:

```
<vendor>-<model>-<doc-type>.pdf

Examples:
  marantz-sr5014-owners-manual.pdf
  marantz-sr5014-quick-start.pdf
  emotiva-basx-a7plus-manual.pdf
  kef-r3-spec-sheet.pdf
  kef-r3-quick-start.pdf
  furman-p1800-pfr-owners-manual.pdf
  bic-formula-f12-manual.pdf
  apple-tv-4k-2nd-gen-setup.pdf
  lg-75un7370pue-owners-manual.pdf
  isoacoustics-gaia-iii-install.pdf
  svs-soundpath-subwoofer-isolation-install.pdf
```

Lowercase, hyphenated, no spaces. Doc-type suffix indicates whether it's `owners-manual`, `quick-start`, `spec-sheet`, `service-manual`, etc.

## Adding a new manual

1. Download the PDF from the manufacturer's official support / downloads page (use the URL listed in `manuals.md`).
2. Save it to this directory using the convention above.
3. Update the **"Local file"** column in `manuals.md` to reflect the actual filename.
4. If the equipment isn't yet in `manuals.md`, add a row with vendor, model, doc type, and source URL.

## Pulling manuals to a fresh clone

The PDFs are not in git. To populate this directory on a new machine, work down `manuals.md` and `wget` / browser-download each from the listed source URL.
