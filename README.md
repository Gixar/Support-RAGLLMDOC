# LLM Support Pack Builder

A **single-file**, offline, dependency-free web app to collect, organize, and export support records (Incidents, Cases, Tasks) into JSONL, CSV, and Markdown — including **RAG-ready chunked JSONL**.

> Open `index.html` in any modern browser. No server, no build steps, no network calls.

---

## Features
- Add/Edit/Delete records with accessible form UI
- Filter by client, tool, environment, id, tags, summary
- Exports:
  - **JSONL (records)** — one record per line
  - **JSONL (chunks)** — configurable max chars + overlap, with metadata
  - **CSV** — flat tabular export
  - **Markdown** — with YAML front-matter
- Runs **100% client-side** with the Blob download API
- Works offline (no deps)
- Example data button

## Schema
See form fields; derived field `text` concatenates `summary`, `steps_to_reproduce`, and `solution`.

## How to Use
1. Double-click `index.html` to open in your browser.
2. Create records (or click **Load Example Data**).
3. Filter if needed.
4. Choose an export format (JSONL, JSONL chunks, CSV, Markdown).
5. Files download locally.

## RAG Chunking
- Configure **Max characters** and **Overlap** under *Advanced Options*.
- Chunk export includes metadata: `record_id`, `chunk_index`, `total_chunks`, `start`, `end`, `segment`, and record attributes.

## Development
- All code is inline in `index.html` (HTML, CSS, JS).
- No tooling needed. Just edit and refresh.

## Notes
- Optional localStorage persistence hooks can be added later.
- Tested on Chrome, Firefox, Safari, Edge.

---

**PRD Reference:** Implemented per "LLM Support Pack Builder" requirements.
