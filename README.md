# Repolex Knowledge Graph of jshttp/accepts

RDF knowledge graph data for [jshttp/accepts](https://github.com/jshttp/accepts), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download jshttp/accepts
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f69c19e459bd501e59fb0b1a40b7471bb578113a
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── f69c19e459bd501e59fb0b1a40b7471bb578113a.nq.gz
│   └── repolex
│       └── f69c19e459bd501e59fb0b1a40b7471bb578113a
│           └── chunk-001.nq.gz
├── blob
│   ├── 06166077be4d1f620d89b9eb33c76d89e75857da.nq.gz
│   ├── 0bec5c9d7b37ae6cd95d7f32d2b9669a50b2375b.nq.gz
│   ├── 0e8585a65db58b00e56ca8befda1de50336b8566.nq.gz
│   ├── 0f2d15da92b29d328f4da484f494c5442c711b4d.nq.gz
│   ├── 50b66c922b8da273dea988ffbfc4b5a4024324f7.nq.gz
│   ├── 58a0ea1f0018b15d14fa4e6d933e3eaad4868ad2.nq.gz
│   ├── 76b1021d09a5774679c815f83d1c9a4bccf21c28.nq.gz
│   ├── 82680c530c3886540f630f643990e2ec707319d1.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── ba6c9a86b7e7e44f0b922d0534e283a712a32a02.nq.gz
│   ├── bbe91f3793707a34a57d294d08de8b6cf122525f.nq.gz
│   ├── cb5990c7c3620f4936a3ac42b3bf335c95eef7e8.nq.gz
│   ├── cf3015fb3b6ee818a7e76aff5854cde130fc5fe0.nq.gz
│   └── e9b2f63fb16f8ecdeb16c8eced302612794ccf65.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── f69c19e459bd501e59fb0b1a40b7471bb578113a.nq.gz
├── filetree
│   └── f69c19e459bd501e59fb0b1a40b7471bb578113a.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 24 files
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

## Source repository

[jshttp/accepts](https://github.com/jshttp/accepts)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
