# Kyvos Plugin

A plugin for querying and analyzing data through Kyvos semantic models, with built-in anomaly detection. Designed for [Cowork](https://claude.com/product/cowork) and Claude Code.

## Installation

```
claude plugins add kyvos
```

## What It Does

This plugin connects Claude to your Kyvos semantic layer, enabling natural language data querying and analysis. It also includes an anomaly detection skill for identifying outliers and unusual patterns in your data.

### With the Kyvos Connection

Connect to your Kyvos instance via the pre-configured MCP server for the full experience. Claude will:

- List available semantic models and their columns
- Generate optimized queries from natural language questions
- Execute queries directly against Kyvos
- Detect anomalies and outliers in query results
- Provide data insights and summaries

### Without the Kyvos Connection

Upload CSV or Excel files exported from Kyvos for anomaly detection and analysis. Claude can also help you write queries to run manually.

## Commands

| Command | Description |
|---------|-------------|
| `/kyvos-query` | Query a Kyvos semantic model using natural language |

## Skills

| Skill | Description |
|-------|-------------|
| `anomaly-detector` | Detect statistical anomalies, outliers, and unusual patterns in CSV datasets using Z-score, IQR, time-series, and frequency analysis |

## Example Workflows

### Querying Kyvos Data

```
You: /kyvos-query What are the top 10 products by revenue this quarter?

Claude: [Lists semantic models] -> [Gets columns for relevant table]
       -> [Generates Query] -> [Executes query on Kyvos]
       -> [Presents results with insights]
```

### Anomaly Detection on Query Results

```
You: Run anomaly detection on our sales data

Claude: [Queries Kyvos for sales data] -> [Exports to CSV]
       -> [Runs multi-method anomaly detection]
       -> [Reports: "Found 12 anomalies -- 3 high severity spikes in Region West"]
```

## Connecting Your Kyvos Instance

> If you need to check which tools are connected, see [CONNECTORS.md](CONNECTORS.md).

The plugin comes pre-configured to connect to the Kyvos demo server. To point it at your own instance, update the URL in `.mcp.json`:

```json
{
  "mcpServers": {
    "mcp-server": {
      "command": "npx",
      "args": [
        "mcp-remote",
        "http://YOUR-KYVOS-HOST:PORT/sse",
        "--allow-http"
      ]
    }
  }
}
```
