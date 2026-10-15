# Repolex Knowledge Graph of click-contrib/click-default-group

RDF knowledge graph data for [click-contrib/click-default-group](https://github.com/click-contrib/click-default-group), parsed by [repolex](https://repolex.ai).

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
rlex download click-contrib/click-default-group
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── dfddfd694e365e0b0714e35f9cc2c3097046e169
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── dfddfd694e365e0b0714e35f9cc2c3097046e169
│           └── chunk-001.nq.gz
├── blob
│   ├── 05212f7341bb735f1a2edad3393a4ff1a6bba3cc.nq.gz
│   ├── 23cf6d6941ab6158ff58c51d9b92565a22f46ae8.nq.gz
│   ├── 240b6691608f65bf51084c0e23561dc5bd1ad06a.nq.gz
│   ├── 733bde869d52021d37c940c6e17915eff4b60815.nq.gz
│   ├── 735c54b1354ca6f9d95bce3572f2d45447e21eaa.nq.gz
│   ├── 8f3772d0c823aac7fa43fe022c5f0159be673d46.nq.gz
│   ├── ba74660506d90c514ee1d32bf4eb5ecb0af14075.nq.gz
│   ├── f5ca88bed77414859b64b42a988fa9af7ca014a0.nq.gz
│   └── f90b80dad322195da79d181ee9668447522a0253.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── dfddfd694e365e0b0714e35f9cc2c3097046e169.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 17 files
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

[click-contrib/click-default-group](https://github.com/click-contrib/click-default-group)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
