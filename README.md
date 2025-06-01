```markdown
# PS2EXE - PowerShell to Executable Conversion

## Overview
This project utilizes **PS2EXE** to convert **.ps1** scripts into **.exe** binaries, enabling a controlled lab environment for foundational reverse engineering exercises. By converting scripts to executables, researchers can explore binary analysis, obfuscation, and sandbox evasion techniques.

### Steps to Convert PowerShell Scripts to Executables
1. **Install PS2EXE** (if not already installed):
   ```powershell
   Install-Module -Name ps2exe -Scope CurrentUser
   ```
2. **Ensure the correct execution policy** to allow script execution:
   ```powershell
   Set-ExecutionPolicy RemoteSigned
   ```
3. **Run PS2EXE with the desired script and output filename**:
   ```powershell
   Invoke-PS2EXE -InputFile "shutdown.ps1" -OutputFile "shutdown.exe"
   ```
---

