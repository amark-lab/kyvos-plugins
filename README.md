# Kyvos Plugins - Marketplace

Official marketplace for Kyvos-enhanced plugins.

## What's Included

This marketplace contains the **kyvos** - a data analysis plugin customized for Kyvos analytics platforms with:

- SQL query generation from natural language
- Semantic model integration
- Business intelligence workflows
- Statistical analysis capabilities

## Installation

### For Users

```bash
# Add the Kyvos marketplace
claude plugin marketplace add ki-kyvos/kyvos-plugins

# Install the plugin
claude plugin install kyvos-plugins@kyvos
```

## Structure

```
kyvos-plugins/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace catalog
├── plugins/
│   └── kyvos/
│       ├── .claude-plugin/
│       │   └── plugin.json       # Plugin manifest
│       ├── skills/               # Your skill files go here
│       ├── commands/             # Your command files go here
│       └── .mcp.json            # (Optional) MCP server connections
└── README.md
```



## Support

For issues or questions, please open an issue on GitHub or contact support@kyvos.io
