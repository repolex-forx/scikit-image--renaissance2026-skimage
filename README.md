# Repolex Knowledge Graph of scikit-image/renaissance2026-skimage

RDF knowledge graph data for [scikit-image/renaissance2026-skimage](https://github.com/scikit-image/renaissance2026-skimage), parsed by [repolex](https://repolex.ai).

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
rlex download scikit-image/renaissance2026-skimage
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 190a1229823acc915ca52e1d269ba5d60399f2d2
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 190a1229823acc915ca52e1d269ba5d60399f2d2
│           └── chunk-001.nq.gz
├── blob
│   ├── 41eb7b24767fa880bdf8ffa45c421432402ce4ff.nq.gz
│   ├── 45ddbf026348b6c58900fd0ec3caee5376bdbf5b.nq.gz
│   ├── 53246580887f7e2b26d377f96ec9c9fbba0f62a0.nq.gz
│   ├── 5a4146cdd8e53aaa9edeba2b2152b458858694a1.nq.gz
│   ├── 5aeeebb992337caf20fb74784e93ca59eff0c07a.nq.gz
│   ├── 5f8afd05ceab6f111b21659a22861d89f7092beb.nq.gz
│   ├── 6be944d71e7760ba64cb1ce50ed66657b719c533.nq.gz
│   ├── 951b00a00231d004f4171b3d4dd9cb42cb1975b1.nq.gz
│   ├── aa6f990475fa7c6bfbee6984fa98d85dc15ba496.nq.gz
│   ├── d2c129853d771794c0c6078b20b10d84287c146d.nq.gz
│   ├── d44df71435e5ff5792f1ba868230e909631cab3c.nq.gz
│   ├── ed39071e726e3bf6c78aed5886abd1ee0c5db2ac.nq.gz
│   └── f94fae5d102525abc8764d3678dc98eccc8360ba.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 190a1229823acc915ca52e1d269ba5d60399f2d2.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 19 files
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

[scikit-image/renaissance2026-skimage](https://github.com/scikit-image/renaissance2026-skimage)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
