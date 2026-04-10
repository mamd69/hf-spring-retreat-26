# Building a Searchable Knowledge Base from Your Business Files

Turn your documents, transcripts, and financial data into a semantic knowledge base you can search by meaning.

---

## What You Need

1. An AI coding assistant (Claude Code, Cursor, etc.)
2. A folder of business documents — transcripts, meeting notes, slide decks, financials, whatever you've got
3. The ruvector submodule: https://github.com/ruvnet/ruvector

## Setup

### 1. Add the ruvector submodule to your project

```
add ruvnet/ruvector upstream submodule to this project
```

This gives the AI the vector database, embedding engine, and search infrastructure it needs.

### 2. Copy your source files into the project

Organize your files into folders by type. Transcripts, documents, financials — whatever you have. Examples:

```
copy only the transcripts from [PATH TO RECORDINGS] into [PROJECT]/transcripts
```

If your files live in Google Drive, Dropbox, or another cloud folder, point the AI at the local sync path. It will walk the directories and find everything.

### 3. Create architecture decision records

Reference the ruvector setup skill, your project goals, and your source folders. Ask the AI to plan before building:

```
use the '[PROJECT]/.claude/skills/ruvector-setup' to figure out the right
setup that allows me to achieve my '[PROJECT]/project-goals'.

All of the context needs to be loaded in, including everything in
[PATH TO DOCS], [PATH TO TRANSCRIPTS], and [PATH TO MORE DOCS]
(many different kinds of files).

First create ADR(s) and DDD(s). Don't implement yet. Put planning files
in '[PROJECT]/docs/adr' and '[PROJECT]/docs/ddd'.
```

> **What the AI does:** Reads the ruvector skill to understand the technology. Surveys all your content directories — counts files, identifies types (VTT transcripts, CSV financials, Markdown docs, plain text). Maps each directory to a category. Designs the chunking strategy for each file type. Produces 4 ADRs (technology choice, phased plan, ingestion strategy, tech stack) and 2 DDDs (domain model, glossary of terms).

### 4. Implement

Once the ADRs look right, tell it to build everything:

```
implement ADRs [X-Y], reference DDDs [X-Y]. spawn swarm, implement
completely, test, validate, benchmark, optimize, document.
continue until complete.
```

> **What the AI does:** Creates the full application — package.json, TypeScript source files, parsers for each file type, chunking logic, vector database wrapper, embedding engine, ingestion pipeline, search engine, CLI interface, and tests. Installs dependencies. Runs tests. Ingests all your files. Runs benchmarks. Reports results.

### 5. Verify search quality

Once ingestion completes, test it:

```
bun run search
```

Type natural language queries at the `search>` prompt. Try questions like:
- "What did [person] say about [topic]?"
- "affiliate partnerships and referrals"
- "revenue from last quarter"

You should see results ranked by relevance with source attribution (file, category, date, speakers).

---

## What You Get

A local, semantic knowledge base with three commands:

| Command | What It Does |
|---------|-------------|
| `bun run ingest` | Parse, chunk, embed, and store all your files |
| `bun run search` | Interactive search — ask questions in plain language |
| `bun run benchmark` | Run 10 sample queries and report latency stats |

The knowledge base:
- Runs entirely on your laptop — no cloud, no API costs
- Understands meaning, not just keywords ("cost structure" matches "pricing")
- Stores everything in a single 50MB file (`data/hfg-brain.db`)
- Searches in ~200ms per query

### File types it handles

| Type | How It Chunks |
|------|--------------|
| `.vtt` / `.srt` transcripts | Groups 3-5 speaker turns per chunk, preserves who said what |
| `.md` documents | Splits on headings — each section becomes a chunk |
| `.csv` financials | One row per chunk, generates a plain-English summary |
| `.txt` files | Sliding window (~250 words, 50-word overlap) |

### How it categorizes

Categories are assigned automatically from directory names — no manual tagging. Put your sales call transcripts in `transcripts/Sales Calls/` and they get tagged `sales-call`. Put coaching sessions in `transcripts/Coaching/` and they get tagged `coaching`.

---

## If Something Goes Wrong

### "ONNX WASM files not found" or "falling back to hash-based embeddings"

The AI embedding model needs to load from the ruvector submodule. Make sure the submodule is cloned and present. The runtime must be `node` (not `bun`) because bun's WASM support doesn't handle wasm-bindgen initialization. The AI will set this up automatically, but if you see this error, check that:
- `ruvector/` directory exists with source code in it
- Scripts in `package.json` use `node --import tsx` (not `bun run`)

### "Search results don't seem relevant"

If results are keyword-level (only matching exact words), the ONNX embedder didn't load. Check the startup message — you should see `ONNX embedder ready: 384d semantic embeddings`. If you see `Falling back to hash-based embeddings`, the embedding model isn't loading.

### Re-ingesting after adding new files

Delete the database and re-run:
```
rm data/hfg-brain.db
bun run ingest
```

---

## Tips

- **Start with transcripts.** They're the richest source of context — hours of conversation chunked into searchable pieces.
- **Financial CSVs are surprisingly useful.** Each transaction becomes a searchable sentence like "$1,499 payment from Jane Doe for Mastermind Pro on Mar 8, 2026."
- **Ingestion is a one-time cost.** ~200ms per chunk with semantic embeddings. 9,000 chunks takes ~30 minutes. After that, search is instant.
- **The database file is portable.** Copy `data/hfg-brain.db` to another machine and search works immediately — no re-ingestion needed.
- **Categories come from folders.** Organize your source files into meaningful directories and you get free metadata for filtering.
