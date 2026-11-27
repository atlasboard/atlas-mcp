# ATLAS MCP

Six read-only tools for **Robinhood Chain mainnet** (chain 4663), for Claude, Cursor and any MCP client. No key, no account, nothing to sign.

| Tool | What it reads |
| --- | --- |
| `latest_block` | the latest block and its time (UTC) |
| `wallet_balance` | ETH and USDG of a wallet |
| `token_info` | symbol, decimals, total supply |
| `token_price` | live USDG price from a KyberSwap route quote |
| `contract_verified` | Sourcify verification and state-changing functions |
| `stock_drift` | stock token price on chain versus its oracle |

## Use it

Claude Desktop, Cursor or any MCP client:

```json
{
  "mcpServers": {
    "atlas": { "command": "npx", "args": ["-y", "github:atlasboard/atlas-mcp"] }
  }
}
```

Claude Code:

```bash
claude mcp add atlas -- npx -y github:atlasboard/atlas-mcp
```

Needs Node 18 or newer. Set `ATLAS_RPC` to use your own Robinhood Chain RPC.

Part of [ATLAS](https://atlasboard.dev). MIT license.
