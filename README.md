# Repolex Knowledge Graph of sphinx-contrib/sqltable

RDF knowledge graph data for [sphinx-contrib/sqltable](https://github.com/sphinx-contrib/sqltable), parsed by [repolex](https://repolex.ai).

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
rlex download sphinx-contrib/sqltable
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 24f68db5624297cf768ddba457088b709a8b3313
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 24f68db5624297cf768ddba457088b709a8b3313
│           └── chunk-001.nq.gz
├── blob
│   ├── 1aba38f67a2211cf5b09466d7b411206cb7223bf.nq.gz
│   ├── 35d34fc53bde73a52472b7e1cfce9b183d7aaa66.nq.gz
│   ├── 3b993fa2660a9738823bfad9a522686a33b8f439.nq.gz
│   ├── 42defe3808769de8145f5b3cada2bfabd453db31.nq.gz
│   ├── 5b368685016be8a3bd85df54a270f5b036bddc0a.nq.gz
│   ├── 64290d435d49095430ca8617f4c3acfca77fd83b.nq.gz
│   ├── 817969e6f7542007e4dd7efdac3c553e4b3f74c8.nq.gz
│   ├── 82fc5bf0e6110b04a835c763f5298f16c1908812.nq.gz
│   ├── 8587118a277ab266e0bfb9a1e76ba8bd220e5a12.nq.gz
│   ├── 894b8ffb14bbf232aafeb89909b694d2151a51cf.nq.gz
│   ├── 8c5e45b17016fb1d97af77d86ab346451e468ea5.nq.gz
│   ├── 948837b2ec741394e2950ebd81533e95170b6c77.nq.gz
│   ├── ab10f94affe067abc878951bbab50901b0732376.nq.gz
│   ├── abd472d7969cd6f3f51e932e1fa5c173bdbe257d.nq.gz
│   ├── b1a8db535028985e9c08058e37fffdd6fa9749da.nq.gz
│   ├── b51965fe13984324cf507a75b1d87ea609e3f73f.nq.gz
│   ├── b7f0f921e9f6d7eea98131d8a5147bf4df6bfdb1.nq.gz
│   ├── cc1820e58ab598768584956b2e036f610fb9cda7.nq.gz
│   ├── d137fac8deb4abada3c59a9e3b25f783bcf27d58.nq.gz
│   ├── daa414699132edcfb22d0249ff6be7642e6fe929.nq.gz
│   ├── df179f6146fb436f8953380239e471100892b814.nq.gz
│   ├── e192e9b4aeab150add0a9e7199624acd68661725.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ef5d5d798f057a551c614af2414172c14c39d87c.nq.gz
│   ├── f0caa1cb9f3d9b3c686a408f3ec173e6f0403a5b.nq.gz
│   ├── f5c09e4214162a9521041c6cf88bdb85d1f4f657.nq.gz
│   ├── fc006096ae8961160197959ef7aad424e977e805.nq.gz
│   └── ff0c368f3e79906f8d644afbf84b6455351d35db.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 24f68db5624297cf768ddba457088b709a8b3313.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[sphinx-contrib/sqltable](https://github.com/sphinx-contrib/sqltable)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
