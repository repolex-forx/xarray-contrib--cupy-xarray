# Repolex Knowledge Graph of xarray-contrib/cupy-xarray

RDF knowledge graph data for [xarray-contrib/cupy-xarray](https://github.com/xarray-contrib/cupy-xarray), parsed by [repolex](https://repolex.ai).

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
rlex download xarray-contrib/cupy-xarray
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9f01df09fb23c48d22024404321447c4158e82e8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9f01df09fb23c48d22024404321447c4158e82e8
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b740cd84c9f433639d67a1670e0de52823843bc.nq.gz
│   ├── 14c8b25a22eb6c606c4fd3792c9cbd9eacec31fc.nq.gz
│   ├── 1680a1cada9fc1107de577c230ed47777157aeef.nq.gz
│   ├── 1bb5d4699d32a060be84f5be76199350b919cf32.nq.gz
│   ├── 1d86a4eb3b30a1afcd6e3af9bfdd57966f43b411.nq.gz
│   ├── 2156245ad218240e914c08f107cca3c5acbe06d3.nq.gz
│   ├── 2750edbc1acbf7a34e0104c751fbec2f7ee6ae00.nq.gz
│   ├── 2c074c7060d19b9f84fb1efc9d786f08fe123ebf.nq.gz
│   ├── 3000451df8bfec753020dab796523c63cfc4b1f5.nq.gz
│   ├── 3025717044b68f48108e2ee6593f9bf5d7169399.nq.gz
│   ├── 32bb24529f92346af26219baed295b7488b77534.nq.gz
│   ├── 3677bc240775e4db5f8f37ea5cf9164e37b3d834.nq.gz
│   ├── 445bdcc65c0ba31b460e5bbfec351124b742f8a9.nq.gz
│   ├── 5c3a06c23b94c7e936d83068b1429f7f044e168b.nq.gz
│   ├── 70d22b0d825586d6ad5b859e323825188435d029.nq.gz
│   ├── 7ed214469bab21ef930bc60495fe43e991fd02b3.nq.gz
│   ├── 8a68f8be462838eaa0496484c9df73bc057ea77e.nq.gz
│   ├── 8cef64dbc25195dfb81063c4b0816c13f847b305.nq.gz
│   ├── ab98d057e822a52cd55c187c9755748facfad419.nq.gz
│   ├── addd6d363c2e940176d19bab85cd344df3952e9f.nq.gz
│   ├── b26ee58a11b37a8c9e9ecc08e7dcb4ac6e555f91.nq.gz
│   ├── b329be50482fb388e1d59531dfa66f2b229e79f8.nq.gz
│   ├── b65bc7ec30e6bccccc191a2db2ea781cc2fdf37a.nq.gz
│   ├── c6b2545386c82d32f80665bb4fc8df4240023025.nq.gz
│   ├── d4bb2cbb9eddb1bb1b4f366623044af8e4830919.nq.gz
│   ├── d62ade682260cb28016f3c1b1fcc3d62af52ac2a.nq.gz
│   ├── d67aad851af8e9ab6390db557ac67006dab9e500.nq.gz
│   ├── da853450bc5951318f6dd8ee062e72ea46dc94df.nq.gz
│   ├── e0f649d7d5db26906a26720863d5518eeef9b42b.nq.gz
│   ├── e832bc1a0d10ecd3d1062deb27995a7b2caf2313.nq.gz
│   └── ecd4fb4a24fe319c1bf8df2ee126a3a8b16b87fd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9f01df09fb23c48d22024404321447c4158e82e8.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[xarray-contrib/cupy-xarray](https://github.com/xarray-contrib/cupy-xarray)

---
*Parsed on 2026-10-16 by [repolex](https://repolex.ai)*
