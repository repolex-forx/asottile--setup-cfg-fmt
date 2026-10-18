# Repolex Knowledge Graph of asottile/setup-cfg-fmt

RDF knowledge graph data for [asottile/setup-cfg-fmt](https://github.com/asottile/setup-cfg-fmt), parsed by [repolex](https://repolex.ai).

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
rlex download asottile/setup-cfg-fmt
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6343732185b0a49e2324e6555329ff4711782cb5
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6343732185b0a49e2324e6555329ff4711782cb5
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c5a37eb0adeb312718e533d0a4fbcbea6880056.nq.gz
│   ├── 1a93617d3989ec0e98744d87e53a9b5a5906819e.nq.gz
│   ├── 3d93aefb2da505dba9c0114404cfaaeee5ad0d3f.nq.gz
│   ├── 3e0a6560f9027acdfb362844d2c933df2db1c74a.nq.gz
│   ├── 5370c9485451439199ab7ab9ba30c95d9a046275.nq.gz
│   ├── 5a4128de7f16972c216a66cf8d9b13716c1b6111.nq.gz
│   ├── 8b59cac5b8857be8fea9b2e7eecaab1c033aad50.nq.gz
│   ├── aa7a0d9be64b2fb88c998e9e5ef090953f072ee7.nq.gz
│   ├── b1447c3015af9511f2dee402ca4b5ad62adf5dce.nq.gz
│   ├── c7f69a3b98830c6a0a56ee791c15b55d967d71f8.nq.gz
│   ├── ca1d90ea180858ae143c0e62d920e350d3acc62d.nq.gz
│   ├── e3c45e369338e3a2eb1ed011e48db4bdc4643094.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6343732185b0a49e2324e6555329ff4711782cb5.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[asottile/setup-cfg-fmt](https://github.com/asottile/setup-cfg-fmt)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
