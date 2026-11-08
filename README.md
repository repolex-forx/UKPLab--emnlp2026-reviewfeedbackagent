# Repolex Knowledge Graph of UKPLab/emnlp2026-reviewfeedbackagent

RDF knowledge graph data for [UKPLab/emnlp2026-reviewfeedbackagent](https://github.com/UKPLab/emnlp2026-reviewfeedbackagent), parsed by [repolex](https://repolex.ai).

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
rlex download UKPLab/emnlp2026-reviewfeedbackagent
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 847fcb70d2eaf817dd9e50472943e1c57f630885
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 847fcb70d2eaf817dd9e50472943e1c57f630885
│           └── chunk-001.nq.gz
├── blob
│   ├── 214fd946e84cfa23a7427db750942225a0f3cc9d.nq.gz
│   ├── 27f7e2bd2219a5cb8813606c7ab715a954005b7b.nq.gz
│   ├── 33d1d0b3a3a97f54718f19bbc52e87cc6aa3877d.nq.gz
│   ├── 37e03eb3343608883f37aa3365718c2247440b9d.nq.gz
│   ├── 40a4fe66d53ce7ac6493473d10b612784fac3ba6.nq.gz
│   ├── 4494992e95a890d760734ccf84e8f96ba53b132e.nq.gz
│   ├── 5123d8ab09b1a5d2062125417d1d7c77593775c5.nq.gz
│   ├── 72d0e99fe566abeeb5562010315d44abcaf9905f.nq.gz
│   ├── 74fe77331bec21050d0de9008f05f372daa2fe71.nq.gz
│   ├── 7b0f92ec8297dbd28e0d12ce891429b322dd7c1b.nq.gz
│   ├── 89f79d04b69ed907c42ae436aa16e9cfa7cfd9bf.nq.gz
│   ├── 8a93e954dbeae1ae84b481ca6d40366583f77b04.nq.gz
│   ├── 8ac366009619b5ec63cb8edf82b07e01a2c0fb66.nq.gz
│   ├── a63f2d8a0a7439de204a4df165b81dab12e57729.nq.gz
│   ├── b2e04d2ea9a8d570947940ccf060e50994c09a47.nq.gz
│   ├── bb2bf6c208788bbef0bc7f0e452baa318b942fdf.nq.gz
│   ├── c78879e003012c19b2229db28f4217d5a63a174e.nq.gz
│   ├── ea6d05ea8f9d193059c6b06318dbcc5229e7b33a.nq.gz
│   ├── f448d15df02f86bd95ed3d9d00a4c6b9342956a8.nq.gz
│   └── f5cb21dded1238253a9c0f9bde06470217a58d44.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 847fcb70d2eaf817dd9e50472943e1c57f630885.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 27 files
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

[UKPLab/emnlp2026-reviewfeedbackagent](https://github.com/UKPLab/emnlp2026-reviewfeedbackagent)

---
*Parsed on 2026-11-08 by [repolex](https://repolex.ai)*
