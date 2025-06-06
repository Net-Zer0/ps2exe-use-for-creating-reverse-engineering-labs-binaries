# PS2EXE - PowerShell to Executable Conversion

## Overview
This project utilizes **PS2EXE** to convert **.ps1** scripts into **.exe** binaries, enabling a controlled lab environment for foundational reverse engineering exercises. By converting scripts to executables, researchers can explore binary analysis, obfuscation, and sandbox evasion techniques.

Additionally, this project includes **binary analysis** using **Binary Ninja**, allowing deeper inspection of how the compiled `.exe` translates from PowerShell logic. Researchers can evaluate obfuscation layers, inspect system calls, and study execution behavior in a controlled environment.

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

### Binary Ninja Analysis
https://binary.ninja/

1. **Open the Compiled Executable**  
   - Load `shutdown.exe` into **Binary Ninja** for analysis.

2. **Inspect the Disassembly & Decompiled Code**  
   - Examine **syscalls**, function calls, and PowerShell behavior translated into executable format.

3. **Evaluate Obfuscation & Execution Patterns**  
   - Identify obfuscation layers added during conversion.
   - Check for potential sandbox evasion indicators.

4. **Analyze Strings & Imports**  
   - Extract embedded strings to reveal PowerShell execution logic.
   - Review imported libraries to understand system interaction.

5. **Compare Against the Original Script**  
   - Map decompiled functions back to PowerShell commands.
   - Assess execution flow differences introduced in conversion.

---
In the examples provided strings will show the execution chain!
![Code in Strings](code-in-strings.png)
---
Disclaimer
This project is intended solely for educational and research purposes in a controlled environment. Misuse of executable conversion techniques for unauthorized access, obfuscation, or malicious activities is strictly prohibited. Users are expected to adhere to ethical cybersecurity practices and comply with all applicable laws and regulations.
When working with executable files, always validate scripts before execution, use virtualized testing environments, and ensure full transparency in research documentation.
---
