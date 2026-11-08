# Repolex Knowledge Graph of langchain-ai/simple-agent-template

RDF knowledge graph data for [langchain-ai/simple-agent-template](https://github.com/langchain-ai/simple-agent-template), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download langchain-ai/simple-agent-template
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bc464b5a860f32fa67e1c1ad171bd817f27518c5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── bc464b5a860f32fa67e1c1ad171bd817f27518c5
│           └── chunk-001.nq.gz
├── blob
│   ├── 00924bb3d9ca5f08a3b9c9dd3dcd50b2143af928.nq.gz
│   ├── 2645a131fd8edeea3b2b58a3a9b5db9084f97dd8.nq.gz
│   ├── 5ac2988050848b46d392560454ff2db8d76d4044.nq.gz
│   ├── 62c6bf5503ee4d980c7d785d1646ae2cf537d34d.nq.gz
│   ├── 6aa2e3eab33641d3b5e3369e39613265ede6c3ae.nq.gz
│   ├── 9f2b8a3077d6136a461c7deef520cc95dc23c71b.nq.gz
│   ├── a1d5d82d65d727a27ab87d8976c07988915ad5d7.nq.gz
│   ├── a8622d402e94241153536f503973b9f95c4c4c0c.nq.gz
│   ├── c0ffb7b02df6e4492b1caf9f2299a6e8e9cc04f4.nq.gz
│   ├── ce32eb96966d04aa176caa1be8a98b3e78cc85c4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── efd1f8aa2b7921ca87c5fce48982c04c64c58f85.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bc464b5a860f32fa67e1c1ad171bd817f27518c5.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 19 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[langchain-ai/simple-agent-template](https://github.com/langchain-ai/simple-agent-template)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
