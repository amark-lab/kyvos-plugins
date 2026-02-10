# Kyvos Cowork Plugins

Official marketplace for Kyvos-enhanced Claude Cowork plugins.

## What's Included

This marketplace contains the **kyvos-cowork-plugin** - a data analysis plugin customized for Kyvos analytics platforms with:

- SQL query generation from natural language
- Semantic model integration
- Business intelligence workflows
- Statistical analysis capabilities

## Installation

### For Users

```bash
# Add the Kyvos marketplace
claude plugin marketplace add your-org/kyvos-cowork-plugins

# Install the plugin
claude plugin install kyvos-cowork-plugin@kyvos-plugins
```


## Structure

```
kyvos-cowork-plugins/
├── .claude-plugin/
│   └── marketplace.json          # Marketplace catalog
├── plugins/
│   └── kyvos-cowork-plugin/
│       ├── .claude-plugin/
│       │   └── plugin.json       # Plugin manifest
│       ├── skills/               # Your skill files go here
│       ├── commands/             # Your command files go here
│       └── .mcp.json            # (Optional) MCP server connections
└── README.md
```



## License

Specify your license here (e.g., MIT, Apache 2.0, Proprietary, etc.)

## Support

For issues or questions, please open an issue on GitHub or contact support@kyvos.io