## Blender MCP — Quick Setup

### Prerequisites
- Blender 3.0 or newer
- Python 3.10 or newer
- uv package manager (required)
  - macOS:
    ```bash
    brew install uv
    ```
  - Windows:
    ```powershell
    powershell -c "irm https://astral.sh/uv/install.ps1 | iex"

    rem If needed, add uv to PATH (adjust username as needed)
    set Path=C:\Users\nntra\.local\bin;%Path%
    ```
- ⚠️ Do not proceed before installing uv

### Install the Blender Add-on
1. Download `addon.py` from this repo (Blender-MCP/addon.py)
2. Open Blender
3. Edit → Preferences → Add-ons
4. Click "Install..." and select the downloaded `addon.py`
5. Enable the add-on: check the box next to "Interface: Blender MCP"

### Start and Connect
1. In Blender, open the 3D View sidebar (press `N` if not visible)
2. Go to the "BlenderMCP" tab
3. Optional: enable the Poly Haven checkbox for asset/HDRI access
4. Click "Start MCP server"

### Configure in Friday
Add a new MCP server with the following command configuration:

```json
{
  "command": "cmd",
  "args": ["/c", "uvx", "blender-mcp"]
}
```

Notes
- Make sure the MCP server is running in a terminal when connecting.
- The first run may download/setup the tool via uv.
- Screenshots coming soon.

