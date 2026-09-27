# Repolex Knowledge Graph of asimov-modules/asimov-gemini-module

RDF knowledge graph data for [asimov-modules/asimov-gemini-module](https://github.com/asimov-modules/asimov-gemini-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-gemini-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 130f48d89684590f9dc6f0e889ea9e4d01a1fd9b
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 130f48d89684590f9dc6f0e889ea9e4d01a1fd9b.nq.gz
│   └── repolex
│       └── 130f48d89684590f9dc6f0e889ea9e4d01a1fd9b
│           └── chunk-001.nq.gz
├── blob
│   ├── 105dc52a26a211d63a07c3ef5c2eea811e143add.nq.gz
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 2c56a7ee242e0dfa830e06d5eede125cd08b2a1b.nq.gz
│   ├── 4a6c982c2963120f2aa7df82c1881ca1fd229ffb.nq.gz
│   ├── 4aa672ae575297e617f3d17a6c588d5234a5edf7.nq.gz
│   ├── 4e379d2bfeab6461d0455bf5bbb8792845d9bbea.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6c745cd4a1594ee08f38c53d73165afd294dc5fe.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e2addb0a0b6a1e0e2ef4e103e136cbc7d1658a9e.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f6540cab641aec94fa5e881df1b911de3b711649.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 130f48d89684590f9dc6f0e889ea9e4d01a1fd9b.nq.gz
├── filetree
│   └── 130f48d89684590f9dc6f0e889ea9e4d01a1fd9b.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 27 files
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

[asimov-modules/asimov-gemini-module](https://github.com/asimov-modules/asimov-gemini-module)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
