# Repolex Knowledge Graph of modelcontextprotocol/progressive-disclosure-wg

RDF knowledge graph data for [modelcontextprotocol/progressive-disclosure-wg](https://github.com/modelcontextprotocol/progressive-disclosure-wg), parsed by [repolex](https://repolex.ai).

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
rlex download modelcontextprotocol/progressive-disclosure-wg
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9f43bd79c54c386982d341d5a911be5fe171b252
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9f43bd79c54c386982d341d5a911be5fe171b252
│           └── chunk-001.nq.gz
├── blob
│   ├── 1d87cd2b55c137424ec9741a879ecf8adc9cb621.nq.gz
│   ├── 2b30d75ffa92038138e11b76bc4f117cf5551eac.nq.gz
│   ├── 346fb2853e7d5cf96f8e0ad38ce290ff4478bdad.nq.gz
│   ├── 412e88078a9c756569c16ae101ade88f93f47132.nq.gz
│   ├── 4722f944d24c0fbe6c4dbd588f148a55e68f6a35.nq.gz
│   ├── 4e78ad17f482b1d31dc7fd473b32ffb0c27e3788.nq.gz
│   ├── 5fbd03453a431d4ba45ddb54b90887644c89c490.nq.gz
│   ├── 7511a279b201793c77b05209ea15a1cce1f04c72.nq.gz
│   ├── 7e1eff0ebcb012e2a63c8aeaa263fb2f7fe1560b.nq.gz
│   ├── 81308a8cf18895b214688367f87488c7ac055fc2.nq.gz
│   ├── 840a2c6b0be0621dd03ccc938cec54f230835c53.nq.gz
│   ├── 948116ea34d7fa8658757067bde4bf3c68d959df.nq.gz
│   ├── a42a70518cfc65c5dec351ffce9e69746d10a8a0.nq.gz
│   ├── c391d9008bd1c3ddadcb9ec3220ad72af3f12bbb.nq.gz
│   ├── da2a6a0f4c47d185d8cb0b8d4ff94c3c3e6b6748.nq.gz
│   ├── e0ec63f63ac3cc80ed64eec77bb2163e0d84d54f.nq.gz
│   ├── efb9a185c66173a945ca8cbcdf03cc39a5a09379.nq.gz
│   └── f3b265ad864475c060d8c6570359d2bbab42ecc7.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9f43bd79c54c386982d341d5a911be5fe171b252.nq.gz
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

[modelcontextprotocol/progressive-disclosure-wg](https://github.com/modelcontextprotocol/progressive-disclosure-wg)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
