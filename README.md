# Repolex Knowledge Graph of pytest-dev/pytest-github-actions-annotate-failures

RDF knowledge graph data for [pytest-dev/pytest-github-actions-annotate-failures](https://github.com/pytest-dev/pytest-github-actions-annotate-failures), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-github-actions-annotate-failures
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1b57c457c2becd9c4f1fd536e282e28cbb73fa74
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1b57c457c2becd9c4f1fd536e282e28cbb73fa74
│           └── chunk-001.nq.gz
├── blob
│   ├── 089091f0ecd122333ef243feb836e3e15f94c88a.nq.gz
│   ├── 3abcef7111f70fb1c89080b1f711be10776c69e0.nq.gz
│   ├── 42e6b8f63347870a627af2c906b202eae51ebad2.nq.gz
│   ├── 4f0650b48c8d675437f2e3e9b2f25cb837378ae1.nq.gz
│   ├── 58e0337e8218a1d79644c30af59cfaf5119c2466.nq.gz
│   ├── 5e000b852adcb9e3c1e0f6d9199b4d5509269808.nq.gz
│   ├── 71eea8557c447fb89c68b9cafb552248343cbb00.nq.gz
│   ├── 7796577130896485f3507b148a241ee3788cefa1.nq.gz
│   ├── 7c860226ceaf09d9cf64eda14087ed539454d5a2.nq.gz
│   ├── 8558c3d4451a968291c979901fefa0c3a6a2817c.nq.gz
│   ├── 90aba4578079628a895e8eeb453716f08e476386.nq.gz
│   ├── 977d8303dfb487e61089f374dc6e1f5bd12bb695.nq.gz
│   ├── 9d03932a46c6ac27f3eb0b510b0ff893ee597934.nq.gz
│   ├── b6e47617de110dea7ca47e087ff1347cc2646eda.nq.gz
│   ├── cca65d36f1b91a0946cb5962d0f61ccb15d7b93a.nq.gz
│   ├── e3e0207a2f8cf9534693607a8624b4d715872dcb.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── e8bbab442c5d0a5a74099a0aa257e1a565c7c1e0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1b57c457c2becd9c4f1fd536e282e28cbb73fa74.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[pytest-dev/pytest-github-actions-annotate-failures](https://github.com/pytest-dev/pytest-github-actions-annotate-failures)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
