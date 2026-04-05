# lecture-brain

A Claude Code skill that turns your course materials into a curriculum-aware teaching knowledge base. Concepts, prerequisites, explanation variants, misconceptions, and semester evidence — all in one place, queryable in your voice.

Requires [Claude Code](https://docs.anthropic.com/en/docs/claude-code) (Pro or Max plan).

---

## Setup

**1. Download `teaching-wiki-skill.md` and install it as a Claude Code skill**

```bash
# Create the skills directory if it doesn't exist
mkdir -p ~/.claude/skills/wiki

# Place the file there, renamed to SKILL.md
cp teaching-wiki-skill.md ~/.claude/skills/wiki/SKILL.md
```

**2. Create a folder for your wiki and open Claude Code in it**

```bash
mkdir my-wiki && cd my-wiki
claude
```

**3. Initialize everything**

```
/wiki init
```

This creates `raw/`, `wiki/`, `CLAUDE.md`, and all subdirectories. Everything is built from scratch — nothing else needed.

**4. Drop your course materials into `raw/` and build**

```
/wiki ingest
```

---

## Commands

| Command | What it does |
|---|---|
| `/wiki init` | Set up the full project structure (run once per project) |
| `/wiki ingest` | Read all files in `raw/` and build the wiki |
| `/wiki absorb` | Update wiki after adding new files to `raw/` |
| `/wiki semester` | Start or close a semester record |
| `/wiki evidence <file>` | Ingest exam results or feedback — updates concept and explanation ratings |
| `/wiki explain <concept>` | Get explanation variants for a concept |
| `/wiki explain <concept> for <student type>` | Get the right explanation for a specific student profile |
| `/wiki prereqs <concept>` | Show the full prerequisite chain back to foundational concepts |
| `/wiki query <question>` | Ask anything — answered in your teaching style |
| `/wiki gap-check` | Find concepts with no explanations, no evidence, or missing prerequisites |
| `/wiki cleanup` | Audit and fix thin, generic, or broken articles |
| `/wiki status` | Articles by type, semester sequence, evidence coverage, gaps |

---

Inspired by [Andrej Karpathy's LLM Wiki pattern](https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f).
