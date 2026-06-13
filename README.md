# insight-draft

Starter kit for writing **RodiumAi Insights** articles and importing them into the dashboard via Markdown upload.

| File | Purpose |
| ---- | ------- |
| [template.md](./template.md) | Empty bilingual template with all required markers |
| [example.md](./example.md) | Filled sample article (API quickstart) |
| [AI-PROMPT.md](./AI-PROMPT.md) | Copy-paste prompt for ChatGPT, Claude, Cursor, etc. |
| [README.fr.md](./README.fr.md) | French version of this guide |

Published insights appear on [rodiumai.io/insights](https://rodiumai.io/insights).

---

## What is an Insight?

An **Insight** is a RodiumAi blog article: tutorials, product news, integration guides, model spotlights, community stories, and more.

Instead of typing everything in the dashboard editor, you prepare a **single `.md` file** offline. The dashboard parser reads structured markers (`*Title_EN*`, `*Content_EN*`, etc.) and fills the publish form automatically.

---

## Quick workflow

1. Copy [template.md](./template.md) to `my-article.md`
2. Write your content (English required, French optional)
3. Validate markers and summary length (see below)
4. Sign in to [rodiumai.io](https://rodiumai.io)
5. Go to **Dashboard → Insights → New**
6. Choose **Markdown upload** (or paste the file contents)
7. Review the preview, adjust if needed, then **Publish**

You can also use [AI-PROMPT.md](./AI-PROMPT.md): paste your rough notes into an AI assistant and get back a ready-to-upload file.

---

## File format

The upload parser expects **exact section markers** on their own lines. Do not rename them.

```
*Title_EN*
English title here

*Title_FR*
French title (optional)

*Summary_EN*
English summary (10–500 characters)

*Summary_FR*
French summary (optional)

*Tags*
comma, separated, tags

*Content_EN*
## Your first heading

English Markdown body...

*Content_FR*
## Votre premier titre

French Markdown body (optional)...
```

### Required sections

| Marker | Required | Notes |
| ------ | -------- | ----- |
| `*Title_EN*` | Yes | Main title on the site |
| `*Summary_EN*` | Yes | 10–500 characters; used in cards and SEO |
| `*Tags*` | Yes | Comma-separated, lowercase, no `#` |
| `*Content_EN*` | Yes | Full article in Markdown |
| `*Title_FR*` | No | Shown when user switches to French |
| `*Summary_FR*` | No | French card summary |
| `*Content_FR*` | No | Full French body |

### Header comments (optional)

Lines starting with `#` at the top of the file are ignored by readers but help authors remember the format:

```markdown
# RodiumAi insight — Markdown upload format
# English required. French optional.
```

---

## Writing guidelines

**Branding:** always write **RodiumAi** (not RodiumAI, not Rodium AI).

**Tone:** clear, practical, friendly. Short sections. Avoid walls of text.

**Headings:** prefer `##` and `###`. Keep titles short.

**Links:** use full URLs (`https://rodiumai.io/...`).

**Code:** use fenced blocks with language tags (` ```bash `, ` ```python `).

**Marketing (when relevant):** link to sign-up, billing, models catalogue, API keys, or RODISTAR program. Help readers take the next step.

**Punctuation:** avoid long em dashes (`—`). Use commas, colons, or short sentences instead.

**Summaries:** one or two sentences max. State what the reader will learn and why it matters.

**Tags:** 3–8 tags. Examples: `api`, `integration`, `continue`, `models`, `rodistar`, `getting-started`.

---

## Markdown body tips

Inside `*Content_EN*` and `*Content_FR*`, standard Markdown works:

- **Bold**, *italic*, lists, tables, blockquotes
- Images: `![alt text](https://your-cdn.com/image.png)`
- Internal links to RodiumAi pages

Do **not** wrap the body in extra `*Content_*` markers. One opening marker, then everything until the next section marker.

---

## Bilingual articles

Best practice: write **both** English and French for community reach.

Minimum viable: English only (`*Title_EN*`, `*Summary_EN*`, `*Content_EN*`, `*Tags*`).

French-only content without English is **not** supported for upload.

---

## Validate before upload

Checklist:

- [ ] Every marker spelled exactly (`*Title_EN*`, not `Title_EN` or `*Title_EN*:`)
- [ ] `*Summary_EN*` between 10 and 500 characters
- [ ] `*Tags*` on one line, comma-separated
- [ ] `*Content_EN*` is not empty
- [ ] No API keys or secrets in the file
- [ ] Branding is **RodiumAi**
- [ ] File saved as `.md` UTF-8

---

## Example files in this repo

| File | Description |
| ---- | ----------- |
| [example.md](./example.md) | Short API quickstart (bilingual) |
| [template.md](./template.md) | Blank starting point |

Real published examples live in the RodiumAi docs monorepo under `rodiumai_docs/content/` (integration guides, model spotlights, RODISTAR program, etc.).

---

## Generate with AI

Open [AI-PROMPT.md](./AI-PROMPT.md), copy the prompt block, paste your raw notes or outline, and ask the model to output **only** the final `.md` file.

Then run the checklist above before upload.

---

## Troubleshooting

| Problem | Fix |
| ------- | --- |
| Title not detected | Marker must be exactly `*Title_EN*` on its own line |
| Summary rejected | Shorten or lengthen to 10–500 characters |
| French body missing | Add `*Content_FR*` section or publish English-only |
| Broken formatting | Avoid HTML; stick to Markdown |
| Tags not parsed | Single line, commas, no brackets |

---

## Links

- Insights hub: [rodiumai.io/insights](https://rodiumai.io/insights)
- Dashboard: [rodiumai.io/dashboard](https://rodiumai.io/dashboard)
- Models: [rodiumai.io/models](https://rodiumai.io/models)
- Docs: [rodiumai.io/docs](https://rodiumai.io/docs)

Questions about publishing? Contact the RodiumAi team via [rodiumai.io/contact](https://rodiumai.io/contact).
