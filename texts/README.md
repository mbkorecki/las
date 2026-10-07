# Texts

Every text is a separate Markdown file. The page reads `texts/texts.json` to build the list of
titles; a title expands into the text when clicked. Files are fetched only when a text is opened.

## Adding a text
1. Put the text in one or two files, e.g. `texts/my-essay.en.md` and `texts/moj-esej.pl.md`.
2. Add an entry to `texts.json` (the order in the file is the order on the page):

```json
{
  "id": "my-essay",
  "author": "MBK",
  "title": { "en": "My Essay", "pl": "Mój esej" },
  "file":  { "en": "texts/my-essay.en.md", "pl": "texts/moj-esej.pl.md" }
}
```
`author` is shown under the title. `id` appears in the address (`#text/my-essay`) and must be unique. If a language is missing, the
page shows the other version with a short note.

## Markdown that is understood
- Paragraphs are separated by a blank line.
- `*italic*`, `**bold**`, `[link text](https://…)`, bare `https://…` links.
- `## Heading`, `> quotation`, `---` line.
- Footnotes: mark the place with `[^name]` and define it anywhere in the file with
  `[^name]: Footnote text.` Notes are numbered automatically in order of appearance.
