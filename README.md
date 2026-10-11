# Repolex Knowledge Graph of aio-libs/aioodbc

RDF knowledge graph data for [aio-libs/aioodbc](https://github.com/aio-libs/aioodbc), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/aioodbc
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 62069a2ecbbc284af75a5d6cf91a1fc4a505f20b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 62069a2ecbbc284af75a5d6cf91a1fc4a505f20b
│           └── chunk-001.nq.gz
├── blob
│   ├── 017f7485fb7f35c7edca16576101861e941eebd2.nq.gz
│   ├── 02c30de02f0002a2436352cbe2531e2bf56e0bfd.nq.gz
│   ├── 13c1ad6e054abeaa92e45fed33d852405ea7d7f2.nq.gz
│   ├── 1ceacd84c8cdf25987d2b402d71b4366d1bbb086.nq.gz
│   ├── 216527a247581ad2d30ea8b8321921c9e04a3c57.nq.gz
│   ├── 2a14965cd81a81c1d4191ddf4c1beb302f379eb2.nq.gz
│   ├── 2da00be943628ccab347af55aca37b361e47e3e5.nq.gz
│   ├── 309eb2590ffba908f0d7bd2d629ddc3ebc62d3c3.nq.gz
│   ├── 325c7a27608bf6a3bfe4753ab376f366d438f14b.nq.gz
│   ├── 39a9e8dca465c054cf5faca16041892866374792.nq.gz
│   ├── 4228041966cabc645f6f3a41ac29429ca0fde9dd.nq.gz
│   ├── 4a5d01862109b0bee151fd7b28051ea736a25e68.nq.gz
│   ├── 52c58811c3d6dd20a8c127c196f03ecd0675da15.nq.gz
│   ├── 58999fd0643c3d65cba90739cef950b1705d96de.nq.gz
│   ├── 6e1d7dcc62aafe3ded699ad3a326b16cefd911f9.nq.gz
│   ├── 72cea777091dc4b108483e171e87f705f60821e5.nq.gz
│   ├── 7e02cd2fbac201cafd685fa1b6b31d6a11c85ad9.nq.gz
│   ├── 8e7ccabb984bd3c86bf2075afb7811daa48951ef.nq.gz
│   ├── 94443ebe483ca01d55eab00ae9c94059a782a0f2.nq.gz
│   ├── 9be1d470f3ceef80bd71f0741cad591b1c4de169.nq.gz
│   ├── 9c202ddb0036ae3e7d455a040caa42650e5d3675.nq.gz
│   ├── a436d4973e5b47736e7a8be05b0cca97954acca5.nq.gz
│   ├── a9680b9da30290b3d115a647574c9134ca49f98a.nq.gz
│   ├── b542c5eb0416de4a67737c7ae2b5d70a95567e29.nq.gz
│   ├── b83261b056f260013c5106169e8c429323b9b781.nq.gz
│   ├── be0ea0f0d491ad8da29b0f238a6737543efb9f8e.nq.gz
│   ├── bec254fee62519516e62adfc8c076d89c71fb07b.nq.gz
│   ├── c11c76cff5a86974cee312bd79b9c7007daf8725.nq.gz
│   ├── c3c25e76be3bbcf7a986755674b6204ada270215.nq.gz
│   ├── c4374d4eead9bfa8ffacf78399d817a5ba388efb.nq.gz
│   ├── cfcb10e282d9311e73d421023d521e6ac44c17df.nq.gz
│   ├── d6ef24e0bb092db6974b9fc1771246ba20c6db65.nq.gz
│   ├── de9aa0f82bb7cd8873ee3874659ad082d58f8908.nq.gz
│   ├── e0cfdb1bee708bf4163ae8bf4f3aa40892a84599.nq.gz
│   ├── e653de75e31d3535836177f19f80533c654cc3f9.nq.gz
│   ├── e826dc3e804a652573ebe5c419dc31236b87acc9.nq.gz
│   ├── ea19cc52e7833d9030c71b059869e69b8d8f32e7.nq.gz
│   ├── ed79ca2dff40f939b6b110d5862484555095e1b7.nq.gz
│   ├── ef5cffe824db994a217e7cb3bdeeefbc044213e5.nq.gz
│   └── fca761ccb0a00167da246bf1eaa338d8df495243.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 62069a2ecbbc284af75a5d6cf91a1fc4a505f20b.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
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

[aio-libs/aioodbc](https://github.com/aio-libs/aioodbc)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
