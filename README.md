# Ansys Sherlock

> Runs Ansys Sherlock through this assistant instead of you opening the Ansys application by hand — it predicts how likely an electronic assembly is to fail, before it's built. Needs Ansys Sherlock installed and licensed on this computer; the first time you use it, also point it at both the Ansys install folder and the Sherlock install folder.

The bundle zip (**36.8 MB**) is stored in this repository at **`8bf08d41-d858-414d-bdc6-961b9ce46124.zip`**.

This repository is part of the **Forjinn-Desk** MCP bundle collection. An MCP bundle is a self-contained server that a host application launches and communicates with over the MCP (Model Context Protocol) protocol.

## Repo metadata

| Field | Value |
| --- | --- |
| Registry ID | `8bf08d41-d858-414d-bdc6-961b9ce46124` |
| Status in registry | active |
| Bundle size | 36.8 MB |
| Distribution | committed to this repo |

## Environment variables

| Variable | Value / note |
| --- | --- |
| `ANSYS_ROOT` | `C:\ANSYS\v252\ansys_inc` |
| `SHERLOCK_ROOT` | `C:\Program Files\Ansys Inc\v251\sherlock` |

## MCP launch configuration

The host replaces `__INSTALL_DIR__` (install dir) and `__PYTHON__` (bundled Python) at runtime.

```json
{
  "command": "__PYTHON__",
  "args": [
    "server.py"
  ],
  "cwd": "__INSTALL_DIR__",
  "env": {
    "ANSYS_ROOT": "",
    "ANSYS_WORKDIR": "__INSTALL_DIR__",
    "AEDT_NO_GUI": "1",
    "SHERLOCK_ROOT": ""
  }
}
```


## Install / usage

1. Get the bundle:
   - download `8bf08d41-d858-414d-bdc6-961b9ce46124.zip` from this repo (Code → Download ZIP, or `git clone`).
2. Extract to your target installation directory (config paths expect contents at the install-dir root).
3. Set the environment variables listed above.
4. Launch using the MCP config JSON (or let a host client manage it automatically).

> Bundles may include vendored runtimes (bundled Python, Node, or native executables). Builds are Windows x64.
