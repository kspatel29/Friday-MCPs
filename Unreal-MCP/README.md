## Unreal MCP — Quick Setup

### Prerequisites
- Unreal Engine installed (project open in editor)
- Python 3.10 or newer
- uv package manager (required)
  - macOS: `brew install uv`
  - Windows: `powershell -c "irm https://astral.sh/uv/install.ps1 | iex"`

### Folder to Use
- Use the Python servers located at: `Unreal-MCP/Python`

### Configure MCP servers in Friday
Set up each server with uv pointing to the Python folder. Update the path to match your environment.

```json
{
  "mcpServers": {
    "blueprintMCP": {
      "command": "uv",
      "args": ["--directory", "E:\\code\\unreal-mcp\\Python", "run", "blueprint_mcp_server.py"]
    },
    "editorMCP": {
      "command": "uv",
      "args": ["--directory", "E:\\code\\unreal-mcp\\Python", "run", "editor_mcp_server.py"]
    },
    "umgMCP": {
      "command": "uv",
      "args": ["--directory", "E:\\code\\unreal-mcp\\Python", "run", "umg_mcp_server.py"]
    },
    "nodeMCP": {
      "command": "uv",
      "args": ["--directory", "E:\\code\\unreal-mcp\\Python", "run", "node_mcp_server.py"]
    },
    "datatableMCP": {
      "command": "uv",
      "args": ["--directory", "E:\\code\\unreal-mcp\\Python", "run", "datatable_mcp_server.py"]
    },
    "projectMCP": {
      "command": "uv",
      "args": ["--directory", "E:\\code\\unreal-mcp\\Python", "run", "project_mcp_server.py"]
    },
    "blueprintActionMCP": {
      "command": "uv",
      "args": ["--directory", "E:\\code\\unreal-mcp\\Python", "run", "blueprint_action_mcp_server.py"]
    }
  }
}
```

Notes
- Replace the `E:\\code\\unreal-mcp\\Python` path with your local path to `Unreal-MCP/Python`.
- Start only the servers you need, or all of them.
- Ensure Unreal Editor is open with your project when issuing editor/blueprint/UMG commands.
- Screenshots coming soon.

