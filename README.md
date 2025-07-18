# Copilot Dotfiles Template

A dual-purpose repository that serves as both a **personal dotfiles collection** and a **GitHub template** for setting up GitHub Copilot with optimized configurations.

## Dual Usage Modes

### 🏠 As Personal Dotfiles
Clone this repository to set up your development environment:
```bash
git clone https://github.com/your-username/copilot-dotfiles-template.git ~/.dotfiles
cd ~/.dotfiles
./install.sh
```

### 📋 As a GitHub Template
1. Click "Use this template" to create a new repository
2. Customize configurations for your project
3. Team members can clone and run `./install.sh`

## What's Included

### Core Configuration
- **`.copilot-instructions.md`** - Comprehensive default instructions for GitHub Copilot
- **`.vscode/settings.json`** - VS Code settings optimized for Copilot usage
- **`.vscode/mcp.json`** - Model Context Protocol configuration
- **`.devcontainer/devcontainer.json`** - Dev container setup with MCP servers

## Quick Start

### Install Everything
```bash
# Clone the repository
git clone https://github.com/your-username/copilot-dotfiles-template.git ~/.dotfiles
cd ~/.dotfiles

# Run the installer
./install.sh
```

### Manual Installation
If you prefer to install components individually:
```bash
# VS Code settings only
cp .vscode/settings.json "$HOME/.config/Code/User/" # Linux
cp .vscode/mcp.json "$HOME/.config/Code/User/"      # Linux

```

## Features

### GitHub Copilot Optimizations
- **Enhanced Context**: Temporal context and code search integration
- **Advanced Features**: Thinking tool, test generation, notebook support
- **MCP Integration**: Extended capabilities through Model Context Protocol
- **Agent Support**: GitHub Pull Request coding agent integration

### Development Environment
- **Cross-Platform**: Works on Linux, macOS, and Windows
- **Shell Agnostic**: Configurations for both Bash and Zsh
- **Git Integration**: VS Code as default editor, helpful aliases
- **Modern Workflow**: Auto-stash, auto-fetch, and intelligent defaults

### MCP Servers Included
- **context7**: Documentation search across libraries
- **playwright**: Browser automation capabilities
- **microsoft.docs.mcp**: Direct Microsoft documentation access
- **sequential-thinking**: Advanced problem-solving tool
- **grep**: GitHub repository code search
- **nx-mcp**: Nx workspace management

## Customization

### For Team/Project Templates
1. Fork or use as template
3. Update `.github/copilot-instructions.md` with project architecture
4. Modify MCP server configurations for project needs
5. Share with team members

## Requirements

### Essential
- **Git** - For version control functionality
- **VS Code** - For Copilot integration (recommended)

### Optional but Recommended
- **Node.js** - For MCP servers (context7, playwright, nx-mcp)
- **Docker** - For sequential-thinking MCP server
- **GitHub CLI** - Enhanced git credential management

## File Structure
```
├── install.sh                 # Automated setup script
├── .copilot-instructions.md    # General Copilot guidelines
├── .github/
│   └── copilot-instructions.md # Project-specific AI guidance
├── .vscode/
│   ├── settings.json           # Copilot feature enablement
│   └── mcp.json               # MCP server configs
├── .devcontainer/
    └── devcontainer.json      # Dev container setup
```

## Troubleshooting

### VS Code Settings Not Applied
- Ensure VS Code is closed during installation
- Check that the settings path is correct for your OS
- Restart VS Code after installation

### MCP Servers Not Working
- Verify Node.js is installed: `node --version`
- Check Docker availability: `docker --version`
- Install missing packages: `npm install -g @upstash/context7-mcp`

### Shell Configuration Issues
- Restart your terminal
- Check for syntax errors in the config files

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License - see LICENSE file for details
