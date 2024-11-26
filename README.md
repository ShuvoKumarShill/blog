# Blog - Visual Studio Code (VS Code) for the first time

### 1. **Install VS Code**

-   Download from the [official website](https://code.visualstudio.com/).
-   Choose the appropriate version for your OS (Windows, macOS, Linux).

----------

### 2. **Essential Extensions**

Install these extensions to enhance functionality:

-   **Code Formatters**:
    -   Prettier - Code formatter
    -   ESLint (JavaScript/TypeScript linting)
-   **Language Support**:
    -   Python
    -   C/C++ IntelliSense
    -   Java Extension Pack
    -   Live Server (for web development)
-   **Version Control**:
    -   GitLens
-   **Productivity Tools**:
    -   Path Intellisense (autocompletes file paths)
    -   Bracket Pair Colorizer 2
    -   Auto Rename Tag
    -   IntelliCode
-   **Themes**:
    -   One Dark Pro or Material Theme
-   **Markdown**:
    -   Markdown All in One

----------

### 3. **Keyboard Shortcuts**

-   Customize shortcuts in **File → Preferences → Keyboard Shortcuts**.
-   Examples:
    -   Quickly comment: `Ctrl + /` (Windows/Linux) or `Cmd + /` (Mac)
    -   Duplicate line: `Shift + Alt + Down`
    -   Open terminal: `Ctrl + \` (split terminal)

----------

### 4. **Set Up the `settings.json`**

Open settings: **File → Preferences → Settings**, and click the JSON icon to edit `settings.json`. Example:

json

Copy code

`{
  "editor.fontFamily": "Fira Code, Consolas, 'Courier New', monospace",
  "editor.fontLigatures": true,
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "editor.minimap.enabled": true,
  "workbench.colorTheme": "One Dark Pro",
  "files.autoSave": "onFocusChange",
  "terminal.integrated.fontSize": 14,
  "editor.formatOnSave": true,
  "eslint.alwaysShowStatus": true,
  "explorer.compactFolders": false,
  "workbench.editor.enablePreview": false
}` 

----------

### 5. **Configure Terminal**

-   Go to **Settings → Terminal → Integrated → Default Profile**.
-   Set your preferred shell: Bash, Zsh, PowerShell, etc.
-   For Linux/macOS: Add aliases to `~/.bashrc` or `~/.zshrc`.
-   Install **Oh My Zsh** for better terminal customization (Zsh users).

----------

### 6. **Git Integration**

-   Sign in with GitHub/GitLab/Bitbucket in **Source Control → Accounts**.
-   Configure Git:
    
    bash
    
    Copy code
    
    `git config --global user.name "Your Name"
    git config --global user.email "youremail@example.com"
    git config --global core.editor "code --wait"` 
    
-   Use the **GitLens** extension for advanced insights and history.

----------

### 7. **Debugging**

-   Set up launch configurations:
    -   Go to **Run and Debug → Create a launch.json file**.
    -   Example for Node.js:
        
        json
        
        Copy code
        
        `{
          "version": "0.2.0",
          "configurations": [
            {
              "type": "node",
              "request": "launch",
              "name": "Launch Program",
              "skipFiles": ["<node_internals>/**"],
              "program": "${workspaceFolder}/app.js"
            }
          ]
        }` 
        

----------

### 8. **Workspace Settings**

-   Organize projects using **Workspaces**:
    -   Go to **File → Add Folder to Workspace**.
    -   Save workspace configurations for shared settings.

----------

### 9. **Snippets**

-   Create custom code snippets:
    -   Go to **File → Preferences → User Snippets → Select Language**.
    -   Example for Python:
        
        json
        
        Copy code
        
        `{
          "Print to Console": {
            "prefix": "print",
            "body": ["print('$1')"],
            "description": "Print to console"
          }
        }` 
        

----------

### 10. **Advanced Tools**

-   Integrate Docker: Use the **Docker** extension.
-   Use Remote Development extensions for SSH, WSL, or Containers.
-   Integrate Jupyter for Data Science workflows.
-   Leverage Task Runner for automated builds:
    -   Add a `tasks.json` file in `.vscode/`:
        
        json
        
        Copy code
        
        `{
          "version": "2.0.0",
          "tasks": [
            {
              "label": "Build",
              "type": "shell",
              "command": "npm run build"
            }
          ]
        }` 
        

----------

### 11. **Sync Settings**

-   Use **Settings Sync** (native in VS Code):
    -   Go to **File → Preferences → Turn on Settings Sync**.
    -   Sign in with your Microsoft/GitHub account.

----------

### 12. **Performance Tweaks**

-   Disable unnecessary extensions.
-   Increase memory by adding the `--max-memory` flag when launching VS Code.

With these configurations, you’ll have a robust and efficient setup tailored for advanced use cases.
