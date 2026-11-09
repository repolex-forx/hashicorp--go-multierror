# Repolex Knowledge Graph of hashicorp/go-multierror

RDF knowledge graph data for [hashicorp/go-multierror](https://github.com/hashicorp/go-multierror), parsed by [repolex](https://repolex.ai).

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
rlex download hashicorp/go-multierror
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1fda6a371bee4201492c5a384a44d2726751d81a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1fda6a371bee4201492c5a384a44d2726751d81a
│           └── chunk-001.nq.gz
├── blob
│   ├── 14886b60f41e2228ae19d43d0f71a3328f91aafb.nq.gz
│   ├── 1dbc1e6cf7117ccaf2af5471b4cd5e1f18c393c8.nq.gz
│   ├── 4499bb2dff37775735fbefece29fc49b3252d11a.nq.gz
│   ├── 45e65fc15e4ba33485118b92c1185e3d1098cebd.nq.gz
│   ├── 5cad0a7872e0d78953e559694df27ee11f1d1924.nq.gz
│   ├── 5d2ce53c30d9124b1f1a6532b80286e3f8881264.nq.gz
│   ├── 68f6f02fd1878f96a327788f2a6dbff353e063b7.nq.gz
│   ├── 7b6827800e0e79ded9440ae79d67ea8874f4be4c.nq.gz
│   ├── 7fb1521728b035612c7c233c7457fe72783b0f42.nq.gz
│   ├── 864098152e960f3f9cf4ae3023b3aad6abe6389b.nq.gz
│   ├── 877c03e4bad97ddb95078a714e80d4508c0175b9.nq.gz
│   ├── 8b4ac9effa4c4cfa167553c3a2a44291a396fc12.nq.gz
│   ├── 917da341ec18ec77f52bfbf2a046e927b2c8f208.nq.gz
│   ├── a353f38c815953480fe5b76d96061ecccff9ba39.nq.gz
│   ├── a7032491606179edc20edfd9bac4ef8bb9182258.nq.gz
│   ├── b7bea98354bc6d67a408d0d61e82ffd760c48a94.nq.gz
│   ├── b97cd6ed02b5b67f40119c94a14d7dc2fd44d1e7.nq.gz
│   ├── bb6cd2c1d27f52ab6a879255d037e11911fd7356.nq.gz
│   ├── bfc77887d07f47102fc47f79f968eaeecf855629.nq.gz
│   ├── c78c0abf07638f88516fd655235ed00526c7f39a.nq.gz
│   ├── d9a5c3c25fd6833aeb12837b80b386c04cd8c72a.nq.gz
│   ├── df2b3861313301b8f9f0cb7311a09afe37475962.nq.gz
│   ├── e45ee283166c9be325133fc30a7747623b5bc1e4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fa5421056a569f824cc48f5d8c35faba55a2f860.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1fda6a371bee4201492c5a384a44d2726751d81a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[hashicorp/go-multierror](https://github.com/hashicorp/go-multierror)

---
*Parsed on 2026-11-09 by [repolex](https://repolex.ai)*
