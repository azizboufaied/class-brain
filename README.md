# Instructor Wiki

A personal teaching knowledge base built and maintained by Claude. Drop your course materials in — Claude reads them and compiles a structured wiki that captures your explanations, analogies, and teaching patterns. Query it and get answers in your voice.

Requires [Claude Code CLI](https://docs.anthropic.com/en/docs/claude-code) and an Anthropic API key.

---

## Setup

```bash
# 1. Create a folder and copy SKILL.md into it
mkdir my-wiki && cd my-wiki
cp /path/to/teaching-wiki-skill.md .

# 2. Open Claude Code
claude

# 3. Initialize the project structure
/wiki init

# 4. Drop your course materials into raw/
#    (lectures, exams, slides, notes — PDF, DOCX, PPTX, MD, TXT)

# 5. Build the wiki
/wiki ingest
```

---

## Commands

| Command | What it does |
|---|---|
| `/wiki init` | Create folder structure, CLAUDE.md, and starter files (run once) |
| `/wiki ingest` | Read all files in `raw/` and build the wiki from scratch |
| `/wiki absorb` | Update wiki after adding new files to `raw/` |
| `/wiki query <question>` | Ask anything — answered in your teaching style |
| `/wiki cleanup` | Audit and fix thin, generic, or broken articles |
| `/wiki status` | Article count, topics covered, gaps |

---

## Folder structure

```
my-wiki/
  raw/        ← your source files (never modified)
  wiki/       ← Claude builds and maintains this
    index.md
    concepts/
    teaching-style/
    mistakes/
    analogies/
    questions/
    assessments/
    resources/
  CLAUDE.md   ← agent instructions (don't edit)
  teaching-wiki-skill.md    ← defines the /wiki commands
```

> Tip: Open `wiki/` in [Obsidian](https://obsidian.md) to browse articles and follow backlinks.
