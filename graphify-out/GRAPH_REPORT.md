# Graph Report - pre-req-vault  (2026-10-21)

## Corpus Check
- 16 files · ~2,312 words
- Verdict: corpus is large enough that graph structure adds value.
- Unclassified: 4 file(s) not represented in the graph (top: (none) 2, .toml 2)

## Summary
- 104 nodes · 117 edges · 13 communities (9 shown, 4 thin omitted)
- Extraction: 99% EXTRACTED · 1% INFERRED · 0% AMBIGUOUS · INFERRED: 1 edges (avg confidence: 0.85)
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `f9f7ff7c`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- package.json
- VaultState
- lib.rs
- devDependencies
- prelude
- Withdraw
- compilerOptions
- Initialize
- .intialize
- .close
- .deposit
- pre-req-vault

## God Nodes (most connected - your core abstractions)
1. `Withdraw` - 9 edges
2. `VaultState` - 9 edges
3. `Close` - 7 edges
4. `Deposit` - 7 edges
5. `Initialize` - 7 edges
6. `compilerOptions` - 7 edges
7. `initialize()` - 4 edges
8. `scripts` - 3 edges
9. `deposit()` - 3 edges
10. `withdraw()` - 3 edges

## Surprising Connections (you probably didn't know these)
- `Initialize` --references--> `VaultState`  [EXTRACTED]
  programs/pre-req-vault/src/instructions/initialize.rs → programs/pre-req-vault/src/state.rs
- `Withdraw` --references--> `VaultState`  [EXTRACTED]
  programs/pre-req-vault/src/instructions/withdraw.rs → programs/pre-req-vault/src/state.rs
- `Close` --references--> `VaultState`  [EXTRACTED]
  programs/pre-req-vault/src/instructions/close.rs → programs/pre-req-vault/src/state.rs
- `Deposit` --references--> `VaultState`  [EXTRACTED]
  programs/pre-req-vault/src/instructions/deposit.rs → programs/pre-req-vault/src/state.rs

## Import Cycles
- None detected.

## Communities (13 total, 4 thin omitted)

### Community 0 - "package.json"
Cohesion: 0.10
Nodes (20): dependencies, @anchor-lang/core, @solana/web3.js, license, scripts, lint, lint:fix, @anchor-lang/core (+12 more)

### Community 1 - "VaultState"
Cohesion: 0.13
Nodes (15): anchor_lang, cpi, Close, Account, Program, Signer, System, SystemAccount (+7 more)

### Community 2 - "lib.rs"
Cohesion: 0.29
Nodes (9): Context, Result, Withdraw<'info>, close(), deposit(), initialize(), Result, withdraw() (+1 more)

### Community 3 - "devDependencies"
Cohesion: 0.22
Nodes (9): devDependencies, chai, mocha, prettier, ts-mocha, @types/bn.js, @types/chai, @types/mocha (+1 more)

### Community 4 - "prelude"
Cohesion: 0.25
Nodes (5): prelude, COUNTER_SEED, HELLO_WORLD_LAMPORTS, MAX_COUNT, ErrorCode

### Community 5 - "Withdraw"
Cohesion: 0.25
Nodes (8): Account, Program, Signer, System, SystemAccount, Withdraw, Q3PreReqsRs, UncheckedAccount

### Community 6 - "compilerOptions"
Cohesion: 0.25
Nodes (7): compilerOptions, esModuleInterop, lib, module, target, typeRoots, types

### Community 7 - "Initialize"
Cohesion: 0.33
Nodes (6): Initialize, Account, Program, Signer, System, SystemAccount

### Community 8 - ".intialize"
Cohesion: 0.50
Nodes (3): InitializeBumps, Initialize<'info>, Result

## Knowledge Gaps
- **35 isolated node(s):** `license`, `lint:fix`, `lint`, `@anchor-lang/core`, `@solana/web3.js` (+30 more)
  These have ≤1 connection - possible missing edges. (Counts symbols only; 69 node(s) total have ≤1 connection when file, concept and rationale nodes are included.)
- **4 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `VaultState` connect `VaultState` to `prelude`, `Withdraw`, `Initialize`?**
  _High betweenness centrality (0.124) - this node is a cross-community bridge._
- **Why does `Withdraw` connect `Withdraw` to `VaultState`?**
  _High betweenness centrality (0.064) - this node is a cross-community bridge._
- **What connects `license`, `lint:fix`, `lint` to the rest of the system?**
  _35 weakly-connected nodes found - possible documentation gaps or missing edges._
- **Should `package.json` be split into smaller, more focused modules?**
  _Cohesion score 0.09956709956709957 - nodes in this community are weakly interconnected._
- **Should `VaultState` be split into smaller, more focused modules?**
  _Cohesion score 0.13157894736842105 - nodes in this community are weakly interconnected._