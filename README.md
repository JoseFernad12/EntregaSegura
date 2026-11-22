# Stellar workshop setup

Workspace: `C:\Users\Admin\Documents\Estellar`.

## Installed

- Stellar CLI 30.0.1
- Rust stable 1.100.0, target `wasm32v1-none`
- Go 1.27.4
- Visual Studio Build Tools C++ and Windows SDK
- gentle-ai 4.1.1, Codex minimal preset (Engram integration)
- Official Stellar skills: smart-contracts, dapp, assets, data, agentic-payments, zk-proofs, standards, cross-chain
- MCP: stellar-docs (initialize verified), stellar-raven (OAuth confirmed)
- Testnet identity `alice`, funded using the testnet faucet

## Sample contract

The untouched CLI sample is in `soroban-hello-world`.

Open a new PowerShell after installation so it inherits the updated PATH:

```powershell
cd C:\Users\Admin\Documents\Estellar\soroban-hello-world
cargo test
stellar contract build
```

## Authentication

Restart Codex to load installed skills, Engram plugin and MCP servers.
Raven OAuth login has been completed and verified. To authenticate again if needed:

```powershell
codex mcp login stellar-raven
```

Follow the fresh URL printed by that command. Existing authorization links expire.

## Verification results

Visual Studio C++ prerequisites are installed. Contract WebAssembly build passed (633-byte optimized WASM); cargo test passed (1 passed, 0 failed). Native Rust linker probe passed in fresh processes.
Engram 3.7.2 is installed and its MCP initialize handshake passed. `gentle-ai doctor`: 7 passed, 1 failed (GGA is absent; this component is not selected by the minimal preset).
The current chat does not expose Engram tools; memory persistence must wait until MCP reload.

See `odd/tasks/stellar-environment.md` for the current setup log.





