# Copilot Dotfiles Template - AI Agent Instructions

## Project Overview
This is a **dual-purpose repository** that serves as both a personal dotfiles collection and a GitHub template for setting up optimized development environments with GitHub Copilot integration.

## Dual Architecture

### 1. Dotfiles Repository Mode
When used as personal dotfiles:
- **`install.sh`** - Cross-platform setup script that symlinks configurations
- **`git/`** - Git configuration with VS Code integration and helpful aliases
- **`shell/`** - Bash and Zsh configurations optimized for development
- **Backup system** - Automatic backup of existing configurations before installation

### 2. Template Repository Mode
When used as a GitHub template:
- **`.copilot-instructions.md`** - General development guidelines (customizable per project)
- **`.github/copilot-instructions.md`** - Project-specific AI agent guidance
- **`.vscode/`** and **`.devcontainer/`** - VS Code and container configurations

## Key Components & Architecture

### Configuration Files
- **`.copilot-instructions.md`** - Root-level comprehensive Copilot guidelines (general software development best practices)
- **`.vscode/settings.json`** - VS Code settings optimized for Copilot features
- **`.vscode/mcp.json`** - Model Context Protocol server configurations
- **`.devcontainer/devcontainer.json`** - Dev container with MCP servers and extensions

### MCP (Model Context Protocol) Integration
This template heavily leverages MCP for enhanced AI capabilities:
- **context7**: Documentation search across libraries
- **playwright**: Browser automation for testing
- **microsoft.docs.mcp**: Microsoft documentation access
- **sequential-thinking**: Complex problem-solving tool
- **grep**: Code search across GitHub repositories
- **nx-mcp**: Nx workspace management

## Project-Specific Patterns

### Template Usage Pattern
This is designed as a **GitHub template repository**:
1. Users click "Use this template" to create new repos
2. Customize `.copilot-instructions.md` for their specific project needs
3. Inherit the MCP configuration and VS Code optimizations

### Configuration Layering
- **Root `.copilot-instructions.md`**: General development guidelines
- **`.github/copilot-instructions.md`** (this file): Project-specific AI agent guidance
- **`.vscode/settings.json`**: Editor-level Copilot feature enablement

### MCP Server Configuration Duplication
Note: MCP servers are defined in BOTH `.devcontainer/devcontainer.json` and `.vscode/mcp.json`:
- Dev container config enables MCP in Codespaces/dev containers
- VS Code config enables MCP in local development
- Keep both files synchronized when adding new MCP servers

## Developer Workflows

### Dotfiles Installation Workflow
When setting up a development environment:
1. Clone repository to `~/.dotfiles`
2. Run `./install.sh` for automated setup
3. Script creates backups of existing configurations
4. Symlinks are created for all configuration files
5. Dependencies are checked and installed where possible

### Template Customization Workflow
When using as a project template:
1. Fork/use template to create new repository
2. Edit `.copilot-instructions.md` to match project-specific needs
3. Update this file (`.github/copilot-instructions.md`) with actual project patterns
4. Optionally modify MCP server configurations based on project requirements
5. Team members can run `./install.sh` to adopt team configurations

### Cross-Platform Considerations
The `install.sh` script handles OS-specific paths:
- **Linux**: `~/.config/Code/User/`
- **macOS**: `~/Library/Application Support/Code/User/`
- **Windows**: `~/AppData/Roaming/Code/User/`

### MCP Server Management
To add new MCP servers:
1. Add to `.vscode/mcp.json` for local development
2. Add to `.devcontainer/devcontainer.json` under `customizations.vscode.mcp.servers`
3. Consider adding corresponding VS Code extensions if needed

## File Structure Conventions
```
├── install.sh                 # Cross-platform setup script
├── .copilot-instructions.md    # General dev guidelines (modify per project)
├── .github/
│   └── copilot-instructions.md # Project-specific AI guidance (this file)
├── .vscode/
│   ├── settings.json           # Copilot feature enablement
│   └── mcp.json               # MCP server configs (local)
├── .devcontainer/
│   └── devcontainer.json      # MCP servers + extensions (containers)
├── git/
│   ├── .gitconfig             # Git config with VS Code integration
│   └── .gitignore_global      # Global ignore patterns
├── shell/
│   ├── .bashrc                # Bash config with dev shortcuts
│   └── .zshrc                 # Zsh config with modern features
└── README.md                  # Dual-purpose documentation
```

## AI Agent Guidelines

### When Working on This Template
- Maintain the minimal, configuration-focused nature
- Keep MCP server definitions synchronized between `.vscode/mcp.json` and `.devcontainer/devcontainer.json`
- Update documentation when adding new MCP servers or VS Code settings
- Preserve the template's flexibility - avoid overly specific configurations

### When This Template is Used for New Projects
- Replace this file's content with actual project-specific patterns
- Customize `.copilot-instructions.md` to match the project's technology stack
- Add project-specific MCP servers that enhance development for that domain
- Update VS Code settings to enable relevant language/framework extensions

## Integration Points
- **VS Code Extensions**: `GitHub.copilot-chat`, `ms-windows-ai-studio.windows-ai-studio`
- **Container Runtime**: Universal dev container image with Node.js, Python, and development tools
- **MCP Protocols**: HTTP and stdio-based integrations for enhanced AI capabilities
