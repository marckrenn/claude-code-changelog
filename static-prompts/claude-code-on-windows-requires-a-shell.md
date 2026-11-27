Claude Code on Windows requires a shell tool. The sandbox's MXC backend (sandbox.windows.backend) runs PowerShell commands only, and the PowerShell tool is disabled (CLAUDE_CODE_USE_POWERSHELL_TOOL=0).
  - Remove CLAUDE_CODE_USE_POWERSHELL_TOOL from your environment or settings, or
  - Set sandbox.windows.backend to "sandboxuser" and run claude sandbox install to use the sandbox account backend (needs Git for Windows).
