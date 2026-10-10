# Repolex Knowledge Graph of BerriAI/liteadmin-mcp

RDF knowledge graph data for [BerriAI/liteadmin-mcp](https://github.com/BerriAI/liteadmin-mcp), parsed by [repolex](https://repolex.ai).

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
rlex download BerriAI/liteadmin-mcp
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d35ec9c19c117d4c50cc1eccf6ce1296aac25a1a
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d35ec9c19c117d4c50cc1eccf6ce1296aac25a1a
│           └── chunk-001.nq.gz
├── blob
│   ├── 1ab71155b49d376b6ef48bb5f9745617db9ff0fb.nq.gz
│   ├── 256fb5d74c9beaf828dac2185d51fddc05f12998.nq.gz
│   ├── 304eac333f5555a776c6bd64bc8b93a8dc6a9bd6.nq.gz
│   ├── 358e7bdd9f4ffd78022cf7b6ab7ceb62ab8a4f2f.nq.gz
│   ├── 3a54fa53dfbced3044b9db1299290479fb2ab988.nq.gz
│   ├── 5a49a2ff9da71863a045f43c306c7e799bbc803d.nq.gz
│   ├── 5d6fcb89b7e5b79f022a4e56998ed23c0c52dae4.nq.gz
│   ├── 5dd7d8565d58a67ac1b76738562b6be230c9c407.nq.gz
│   ├── 6268e81d1d05870b84d73a7104703e37d81a6662.nq.gz
│   ├── 6ec758cd6779f179214f740bba6e5fa6fc097210.nq.gz
│   ├── 868cb4fe71ba6ad6778d5566bb301ae375defdac.nq.gz
│   ├── 881340d754c43f8e73c06bd4fd344ed998e47723.nq.gz
│   ├── 884221e30c808ea7bdac63cedc0a2bf1c78f1877.nq.gz
│   ├── 8faf0318073d57c783503b5ca4db29e332612eca.nq.gz
│   ├── 92ddc3b397a143ebc4441096428c6c532f1653fe.nq.gz
│   ├── 956088627260cda4589e607ae2cfdf331df9a8cf.nq.gz
│   ├── a047705c27e243fb78d71bba00311e5353a4f7eb.nq.gz
│   ├── a6776a48cce42100aa6538c2804e9716db53592f.nq.gz
│   ├── a818e16eafdef268ff06a5efb82a461c165f52bc.nq.gz
│   ├── a84e36c3056dae7f6b6565b336ccabde9e8a2819.nq.gz
│   ├── aeb0d60ce5559c15ddaec218a2eb0823d834bc7b.nq.gz
│   ├── b227ae2859262958b3f64eb603db3605061144bd.nq.gz
│   ├── bf1bc22c743298874850f8921dc0555e7c60285a.nq.gz
│   ├── c4d3f2370f69e56dc4b28ec5cb0fa55073014da5.nq.gz
│   └── d290168d841311e50d969818fc03fb7adb35e3a4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d35ec9c19c117d4c50cc1eccf6ce1296aac25a1a.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 32 files
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

[BerriAI/liteadmin-mcp](https://github.com/BerriAI/liteadmin-mcp)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
