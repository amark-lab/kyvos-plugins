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

### For Developers/Contributors

1. **Extract your existing plugin:**
   - Unzip your `kyvos-cowork-plugin.zip` file
   - Copy the entire plugin folder into `plugins/kyvos-cowork-plugin/`
   - Make sure your skills and commands are in the right folders

2. **Update the plugin.json:**
   - Edit `plugins/kyvos-cowork-plugin/.claude-plugin/plugin.json`
   - Add/update the `commands` and `skills` sections to match your actual files

3. **Push to GitHub:**
   ```bash
   git init
   git add .
   git commit -m "Initial Kyvos plugin marketplace"
   git remote add origin https://github.com/your-org/kyvos-cowork-plugins.git
   git push -u origin main
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
│       │   ├── sql-generation/
│       │   │   └── SKILL.md
│       │   └── data-analysis/
│       │       └── SKILL.md
│       ├── commands/             # Your command files go here
│       │   ├── write-query/
│       │   │   └── COMMAND.md
│       │   └── analyze-data/
│       │       └── COMMAND.md
│       └── .mcp.json            # (Optional) MCP server connections
└── README.md
```

## Where to Put Your Files

After extracting this template:

1. **Put your existing plugin folder here:**
   - Replace everything in `plugins/kyvos-cowork-plugin/` with your unzipped plugin contents

2. **Make sure you have:**
   - All your SKILL.md files in `skills/` subdirectories
   - All your COMMAND.md files in `commands/` subdirectories
   - Any .mcp.json if you use MCP servers

3. **Update plugin.json:**
   - List all your actual commands and skills in `plugin.json`

## Updating the Plugin

When you make changes:

1. Increment the `version` in both:
   - `.claude-plugin/marketplace.json`
   - `plugins/kyvos-cowork-plugin/.claude-plugin/plugin.json`

2. Commit and push to GitHub

3. Users will get automatic updates on their next Claude startup

## Available Commands

Once installed, users can access:

- `/kyvos-cowork-plugin:write-query` - Generate SQL queries
- `/kyvos-cowork-plugin:analyze-data` - Perform data analysis

(Update this list based on your actual commands)

## License

Specify your license here (e.g., MIT, Apache 2.0, Proprietary, etc.)

## Support

For issues or questions, please open an issue on GitHub or contact support@kyvos.io
>>>>>>> fc06d8b (Initial Kyvos plugin marketplace)
