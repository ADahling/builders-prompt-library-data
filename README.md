# The Builder's Prompt Library, as data

3,323 rubric-graded AI prompts for every stage of shipping software, from idea to launch. This is the open data behind [buildersprompt.com](https://buildersprompt.com), exported from the live catalog so you can grep it, vendor it, load it into your own tools, or point an agent at it.

Built by Alicia Dahling and Peter Lowe. Free to read, copy and adapt under CC BY 4.0 (see LICENSE): keep the attribution, do what you like with the prompts.

## What is in here

| Path | What it is |
|---|---|
| `data/prompts.json` | Every published prompt as one JSON array (title, summary, stage, category, difficulty, tags, variables, tips, prompt text, writing score and grade, hand-reviewed flag, canonical URL). |
| `data/by-stage/*.json` | The same rows split by delivery stage: idea, design, build, test, secure, ship. |
| `data/index.tsv` | One line per prompt: stage, category, grade, score, slug, title. Good for `grep` and `awk`. |
| `prompts/<stage>/<slug>.md` | One Markdown file per prompt with YAML front matter, for editors, static-site generators and retrieval pipelines. |

Fill-in fields look like `{{project_name}}`. Replace them before you paste.

## How the grades work

Every prompt is scored 0 to 100 on a five-part writing rubric (clarity, specificity, format, variables, actionability) and stamped A+ (90+), A (80 to 89), B (70 to 79) or C (60 to 69). Anything below 60 is not published. The grade describes how well the prompt is written, not how well a model answered it. Prompts that were actually run in ChatGPT, Claude and Gemini, with the graded answers, are shown on their pages at buildersprompt.com under "Tested in real AI models". Twenty-two prompts were read line by line by a human and carry `hand_reviewed: true`.

## Use it from an AI assistant instead

The library is also a public MCP server. Point Claude, Cursor, ChatGPT or any MCP client at `https://buildersprompt.com/mcp` (Streamable HTTP, JSON-RPC 2.0, no key) and you get three read tools: `search_prompts`, `get_prompt` and `list_stages`.

## Freshness

This export is regenerated from the live database. Each prompt's `updated_at` is the last edit on the site. If you need a specific prompt's current text, its `url` is the source of truth.

## Attribution

Please credit "The Builder's Prompt Library, buildersprompt.com" and link back when you republish prompts from this set. That is the whole license.
