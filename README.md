# Repolex Knowledge Graph of executablebooks/sphinx-comments

RDF knowledge graph data for [executablebooks/sphinx-comments](https://github.com/executablebooks/sphinx-comments), parsed by [repolex](https://repolex.ai).

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
rlex download executablebooks/sphinx-comments
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 28b946ea9dc52f8ef87b4428ff59aea4224d639a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 28b946ea9dc52f8ef87b4428ff59aea4224d639a
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c9e0fc1447e98b7f63ae8c9eb552c2af7b83f45.nq.gz
│   ├── 47459f4969d9cbaf5e5efbff7a7e295b7aee7482.nq.gz
│   ├── 5d4bb8fe47092f3d996a550455a6f0a813902f02.nq.gz
│   ├── 6df78f4861c75a280bf1edfa5d3a89e32cf46da4.nq.gz
│   ├── 70b97444ac006ea972ff7cb91f4e30147bb1ca40.nq.gz
│   ├── 72a3896155d43a98bfd2ce842d3012203f1d82d7.nq.gz
│   ├── 735f51d4693c4e5d07c33b9b94e48618b487c854.nq.gz
│   ├── 8d0d7e10f2f518d539ca7d7d12cd97a9912ae8e0.nq.gz
│   ├── 9faeff140639a31ec32a7ad63abdf09000903848.nq.gz
│   ├── a9ef4b366335bd8d8bb4495351710855182e0834.nq.gz
│   ├── b0d5b8dc8ada83c9fa745b6c2ecd0b016a1de6b8.nq.gz
│   ├── c1b33392c53b0af31ccff05d8ee969ee5234dda0.nq.gz
│   ├── c2a4555d556915bfa928c457436c8d4828f64128.nq.gz
│   ├── cb8c8f886494e70eb0b7e1e026b91d86f5775d85.nq.gz
│   ├── dab6dc50f5445e17f42a1e8d3c52b2fb874e8fe5.nq.gz
│   ├── e3da228ec9499f5b45088279a0306ed56a2bacf1.nq.gz
│   ├── e5583af64c675fba12d2442a0f403d2fefbd7aaf.nq.gz
│   ├── fcbd90aaa8e6fc1e84bfb171a895b37fc89f7fb3.nq.gz
│   └── fce797365c29d3d3eb33a2284fe2487fb1fc348f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 28b946ea9dc52f8ef87b4428ff59aea4224d639a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[executablebooks/sphinx-comments](https://github.com/executablebooks/sphinx-comments)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
