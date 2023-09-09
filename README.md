# CMake Project Template
CMake project template for Vscode with multiple file builds, debugging support and external terminal runs for C++.
## Dependencies
- lldb (debugging)
- alacritty (terminal - can be changed from `/.vscode/tasks.json`)
- clangd (linting)
- clangd-format

## Setup
  1. Copy/paste the following commands in your terminal:
```bash
git clone https://github.com/SaadAhmedGit/CMake-Project-Template/
cd CMake-Project-Template
code
```
  2. Install this vscode settings profile available [here](https://vscode.dev/profile/github/6e9a3a76efe906fd0bac651148779973) for all the extensions and settings.
  3. Open `src/main.cpp` and press `Ctrl+Alt+N` to execute the program.

Optionally, use the **Project Templates** extension that comes with the profile to save current project as a template and create projects in other folders without cloning from github everytime.
