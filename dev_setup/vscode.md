# Visual Studio Code

## Download

[https://code.visualstudio.com/](https://code.visualstudio.com/)

## Keyboard shortcuts

- [Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
- [Linux](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf)
- [Mac](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)

## Useful plugins

- [Angular 6 Snippets](https://marketplace.visualstudio.com/items?itemName=Mikael.Angular-BeastCode)
- [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template)
- [Angular v6 Snippets](https://marketplace.visualstudio.com/items?itemName=johnpapa.Angular2)
- [angular2-inline](https://marketplace.visualstudio.com/items?itemName=natewallace.angular2-inline)
- [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks)
- [Colonize](https://marketplace.visualstudio.com/items?itemName=vmsynkov.colonize)
  - `Ctrl+K Ctrl+S` to open keyboard shortcuts. Change these three hotkeys to the following:
  
    | | |
    | --- | --- |
    | Colonize and Hold Position | `Ctrl+;` |
    | Colonize and Jump to End | (just delete this one for now) |
    | Colonize and Jump to Newline | `Ctrl+Shift+;` |
- [Debugger for Chrome](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-chrome)
  - [Chrome debugging with Angular CLI](https://github.com/Microsoft/vscode-recipes/tree/master/Angular-CLI)
- [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [HTML CSS Support](https://marketplace.visualstudio.com/items?itemName=ecmel.vscode-html-css)
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
- [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
- [npm](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)
- [Python](https://marketplace.visualstudio.com/items?itemName=donjayamanne.python)
- [SVN](https://marketplace.visualstudio.com/items?itemName=johnstoncode.svn-scm)
- [SVN Gutter](https://marketplace.visualstudio.com/items?itemName=beaugust.blamer-vs)
- [TSLint](https://marketplace.visualstudio.com/items?itemName=eg2.tslint)

## Change shell type

The first time you open the terminal with ``Ctrl+` `` it will ask if you want to change the terminal type. Choose "Customize", then select WSL Bash or whichever you want.

If this prompt does not appear, type `Ctrl+Shift+P` and start typing "select default shell". Press enter and select your desired shell type.

## Useful Settings

### User Settings

Type `Ctrl+Shift+P` and open User Settings. Here are some of mine:

```json
{
  "files.autoSave": "off",
  "terminal.integrated.shell.windows": "C:\\WINDOWS\\System32\\bash.exe",
  "git.enableSmartCommit": true,
  "editor.quickSuggestions": {
    "strings": true // Enables autocomplete in strings
  },
  "files.associations": {
    "*.styl": "css"
  },
  "window.title": "${rootName}${separator}${activeEditorShort} ${dirty}",
  "files.exclude": {
    "**/nbproject": true,
    "**/.idea": true,
    // "**/node_modules": true,
    "**/build": true,
    "**/dist": true,
    "**/.vscode": true
  },
  "npm.enableScriptExplorer": true,
  "extensions.showRecommendationsOnlyOnDemand": true,
  "editor.renderWhitespace": "all"
}
```

### Workspace Settings

Type `Ctrl+Shift+P` and open Workspace Settings. Here is a potential one:

```json
{
  // give window title more meaningful name than "trunk" or "src"
  "window.title": "CUSTOM_PROJECT_NAME — ${separator}${activeEditorShort} ${dirty}"
}
```
