# Repolex Knowledge Graph of python-trio/sphinxcontrib-trio

RDF knowledge graph data for [python-trio/sphinxcontrib-trio](https://github.com/python-trio/sphinxcontrib-trio), parsed by [repolex](https://repolex.ai).

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
rlex download python-trio/sphinxcontrib-trio
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cfd44c1658aaee1b2776077dd576dc869be55522
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cfd44c1658aaee1b2776077dd576dc869be55522
│           └── chunk-001.nq.gz
├── blob
│   ├── 12915e54c9355b0a4b076d39c45723830523b6e3.nq.gz
│   ├── 13cbb2820b75260f0855d2de2fb7dedb6bb2139b.nq.gz
│   ├── 142badd73cd7919e19cf1a97c559e164b359ae1a.nq.gz
│   ├── 15b22e6fc82499dac5ea3b4d2b74347afd1e9ed8.nq.gz
│   ├── 19501eb32b37e55ddcfad80956536e4c987ac734.nq.gz
│   ├── 291840cd6ea71b3744e0d0ea29fdbd95bccfc567.nq.gz
│   ├── 34c8eb1b8a395f5bbe178f49de791f0c850f3926.nq.gz
│   ├── 411ffadb9cea7101816745b5cea8e052dca2413e.nq.gz
│   ├── 41811c46d576754974456a0e4999052ef8f218b7.nq.gz
│   ├── 5fa2f81c34e093b7b461f6c88dc3ec49dcdd3970.nq.gz
│   ├── 6966869c7054c18810eb323772b93ba5a42cefc5.nq.gz
│   ├── 6b88fe271019b5aae2a6cdfed2b5556461466a6e.nq.gz
│   ├── 6c8f6c0ac167d79f3c69450708e5adba8400236c.nq.gz
│   ├── 6ff5c25c5a4b77ac9cce49f44778c1585d19133f.nq.gz
│   ├── 850c956e3437b80d81899fe706aaea4babedfe14.nq.gz
│   ├── 85ce602a6278aefcf8183168262d4162741aa127.nq.gz
│   ├── 897eb67919f93dde56923902a63e801a22d10691.nq.gz
│   ├── 96cb2b25afb70c93ce78cde5003ddd0a1247d906.nq.gz
│   ├── b2386d25d831d935aafe15e542a71a11b5b2988f.nq.gz
│   ├── b38f1a56edac686f29b4e1c99c1fa8fe0f488f04.nq.gz
│   ├── b6a6de3fb37f8c0fe34c0e0133eedca11f83abb4.nq.gz
│   ├── b8bb97185926d7daed314609753173945ed4ff1a.nq.gz
│   ├── c0c4077a947625e0642060ad742d24bffda4c18f.nq.gz
│   ├── cec379d89b4831b7e5a0ec1bb914930ae5084141.nq.gz
│   ├── d01e930f244d317bafea7da6789109eb1aaa0ab1.nq.gz
│   ├── d46a9a89a1f3df10d4596e6e089a71ece22fcd12.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── e1708298c3b082400a1e750f5420f3ca27f060ee.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e730df2805d68eade3fd69f2f3543a29a499bd49.nq.gz
│   └── f55f034db6330eb6029974b32627643705657beb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cfd44c1658aaee1b2776077dd576dc869be55522.nq.gz
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

[python-trio/sphinxcontrib-trio](https://github.com/python-trio/sphinxcontrib-trio)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
