# Repolex Knowledge Graph of postcss/postcss-scss

RDF knowledge graph data for [postcss/postcss-scss](https://github.com/postcss/postcss-scss), parsed by [repolex](https://repolex.ai).

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
rlex download postcss/postcss-scss
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 028380809e01f5f40367464524b64f1101ae270f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 028380809e01f5f40367464524b64f1101ae270f
│           └── chunk-001.nq.gz
├── blob
│   ├── 00196ae3e94d2f259b80a404359bfb9d82409132.nq.gz
│   ├── 117e7c5b47f2ed88bc8ef833ec46b3d6892a1361.nq.gz
│   ├── 148a38ae4585acb3e1478f14a52c43e2fdb700f3.nq.gz
│   ├── 2116506f55899db0aba84c92dc868788548fe9c0.nq.gz
│   ├── 240a2d91eab32b1928b931ca57a8683ceb394c3f.nq.gz
│   ├── 2f124eb94169b0103758d179cb6eb7f3f7ab1bda.nq.gz
│   ├── 3337cabb7f4c1fc60403e420419f658ecf59fa46.nq.gz
│   ├── 40e4504c6190ce83399a494ac527eb4c653bdabc.nq.gz
│   ├── 450d2d018119ef92550d52832f3afc26d795f037.nq.gz
│   ├── 621faf319ddfb9eb6284bfefc5bc11bc9c7bcb9c.nq.gz
│   ├── 65e3ba2edadd2c591f7f522c571cc89fb72473f0.nq.gz
│   ├── 6c174a9de2a644e204f89e425c80ffc0084ffc28.nq.gz
│   ├── 76bf902231b3d6f6138607e026e7dbacc1f46962.nq.gz
│   ├── 8f244e044a51020fe8a5d6169b6f90205aa3ec86.nq.gz
│   ├── 92d296b789fa7c6603ab9798c7be98671a8f44dc.nq.gz
│   ├── a1ef3d2c942e20504024a1b6614b9389fb636031.nq.gz
│   ├── b770b6cc015a55b07a80955fe89d67221b359139.nq.gz
│   ├── c2658d7d1b31848c3b71960543cb0368e56cd4c7.nq.gz
│   ├── c6c8b3621938a4691225a870a59bf382af1883dd.nq.gz
│   ├── caf638bd48b79676678e75a394c4111a6cd1fc3c.nq.gz
│   ├── da057b4562a8b8fcd8ef3898f795cd08aa412ab4.nq.gz
│   ├── f1c5a2a6ce4604242039e41fb0fd0381a03970a8.nq.gz
│   └── fc45fdb8ea0f53ce57a04fc3a8353aa9ef2aeb0a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 028380809e01f5f40367464524b64f1101ae270f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[postcss/postcss-scss](https://github.com/postcss/postcss-scss)

---
*Parsed on 2026-11-10 by [repolex](https://repolex.ai)*
