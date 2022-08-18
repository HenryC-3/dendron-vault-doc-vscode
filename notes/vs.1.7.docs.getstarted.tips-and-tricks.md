---
id: rmukyvofqz7oxp1bgyfu2tq
title: Tips and Tricks
desc: ''
updated: 1660824078448
created: 1660824078448
isDir: false
Order: 3
Area: getstarted
TOCTitle: Tips and Tricks
ContentId: 9bbbe55d-cf81-428f-8a9f-4f60280cb874
PageTitle: Visual Studio Code Tips and Tricks
DateApproved: 8/4/2022
MetaDescription: Visual Studio Code Tips and Tricks for power users.
---
# Visual Studio Code Tips and Tricks

"Tips and Tricks" lets you jump right in and learn how to be productive with Visual Studio Code. You'll become familiar with its powerful editing, code intelligence, and source code control features and learn useful keyboard shortcuts. This topic goes pretty fast and provides a broad overview, so be sure to look at the other in-depth topics in [[vs.1.7.docs.getstarted.userinterface]] and the [[v[[vs.1.7.docs.editor.codebasics]] learn more.

> If you don't have Visual Studio Code installed, go to the [[vs.1.7.download]] page. You can find platform specific setup instructions at [[vs.1.7.docs.setup.linux]], [[v[[vs.1.7.docs.setup.mac]]nd [[vs.1[[vs.1.7.docs.setup.windows]]

Prefer a video? You can watch a recent Microsoft Build talk [Visual Studio Code tips and tricks](https://aka.ms/Build2020AppDev-VSCodeTips), which describes 20 tips and tricks for working productively with VS Code.

## Basics

### Getting started

The best way of exploring VS Code hands-on is to open the **Get Started** page. You will get an overview of VS Code's customizations and features. **Help** > **Get Started**.

![Get Started page](/assets/getstarted_page-d6wkasw835sf.png)

Pick a **Walkthrough** for a self-guided tour through the setup steps, features, and deeper customizations that VS Code offers. As you discover and learn, the walkthroughs track your progress.

If you are looking to improve your code editing skills open the **Interactive Editor Playground**. Try out VS Code's [[vs.1.7.docs.editor.codebasics]], like multi-cursor editing, [[v[[vs.1.7.docs.editor.intellisense]]nippets, [[vs.1[[vs.1.7.docs.editor.emmet]]many more. **Help** > **Editor Playground**.

![Interactive editor playground](/assets/interactive_playground-afstx2wllcn7.png)

### Command Palette

Access all available commands based on your current context.

Keyboard Shortcut: `kb(workbench.action.showCommands)`

![Command Palette](/assets/opencommandpalatte-wau2cq4bleb1.gif)

### Default keyboard shortcuts

All of the commands are in the **Command Palette** with the associated key binding (if it exists). If you forget a keyboard shortcut, use the **Command Palette** to help you out.

![keyboard references](/assets/keyboard-references-01d80xcyzkke.png)

### Keyboard reference sheets

Download the keyboard shortcut reference sheet for your platform ([macOS](https://go.microsoft.com/fwlink/?linkid=832143), [Windows](https://go.microsoft.com/fwlink/?linkid=832145), [Linux](https://go.microsoft.com/fwlink/?linkid=832144)).

![Keyboard Reference Sheet](/assets/keyboardreferencesheet-78p2yvm0p34a.png)

### Quick Open

Quickly open files.

Keyboard Shortcut: `kb(workbench.action.quickOpen)`

![Quick Open](/assets/quickopen-86hyevppw4pc.gif)

**Tip:** Type `kbstyle(?)` to view commands suggestions.

![Quick Open command list](/assets/quick-open-command-dropdown-jquftj6rmrbp.png)

Typing commands such as `edt` and `term` followed by a space will bring up dropdown lists.

![term command in Quick Open](/assets/term-quick-open-i6i4w3gwxzkz.png)

### Navigate between recently opened files

Repeat the **Quick Open** keyboard shortcut to cycle quickly between recently opened files.

### Open multiple files from Quick Open

You can open multiple files from **Quick Open** by pressing the Right arrow key. This will open the currently selected file in the background and you can continue selecting files from **Quick Open**.

### Navigate between recently opened folders and workspaces

Open Recent

Keyboard Shortcut: `kb(workbench.action.openRecent)`

Displays a Quick Pick dropdown with the list from **File** > **Open Recent** with recently opened folders and workspaces followed by files.

## Command line

VS Code has a powerful command line interface (CLI) which allows you to customize how the editor is launched to support various scenarios.

> Make sure the VS Code binary is on your path so you can simply type 'code' to launch VS Code. See the platform specific setup topics if VS Code is added to your environment path during installation ([[vs.1.7.docs.setup.linux]], [[v[[vs.1.7.docs.setup.mac]][vs.1[[vs.1.7.docs.setup.windows]]

```bash
# open code with current directory
code .

# open the current directory in the most recently used code window
code -r .

# create a new window
code -n

# change the language
code --locale=es

# open diff editor
code --diff <file1> <file2>

# open file at specific line and column <file:line[:character]>
code --goto package.json:10:5

# see help options
code --help

# disable all extensions
code --disable-extensions .
```

### .vscode folder

Workspace specific files are in a `.vscode` folder at the root. For example, `tasks.json` for the Task Runner and `launch.json` for the debugger.

## Status Bar

### Errors and warnings

Keyboard Shortcut: `kb(workbench.actions.view.problems)`

Quickly jump to errors and warnings in the project.

Cycle through errors with `kb(editor.action.marker.nextInFiles)` or `kb(editor.action.marker.prevInFiles)`

![errors and warnings](/assets/errors_warnings-a4a4lf59635o.gif)

You can filter problems either by type ('errors', 'warnings') or text matching.

### Change language mode

Keyboard Shortcut: `kb(workbench.action.editor.changeLanguageMode)`

![change syntax](/assets/change_syntax-62sz4n2zz16f.gif)

If you want to persist the new language mode for that file type, you can use the **Configure File Association for** command to associate the current file extension with an installed language.

## Customization

There are many things you can do to customize VS Code.

* Change your theme
* Change your keyboard shortcuts
* Tune your settings
* Add JSON validation
* Create snippets
* Install extensions

### Change your theme

Keyboard Shortcut: `kb(workbench.action.selectTheme)`

You can install more themes from the VS Code extension [Marketplace](https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs).

![Preview themes](/assets/previewthemes-wjyv31svqj76.gif)

Additionally, you can install and change your File Icon themes.

![File icon themes](/assets/previewfileiconthemes-i20dwd3olpt1.gif)

### Keymaps

Are you used to keyboard shortcuts from another editor? You can install a Keymap extension that brings the keyboard shortcuts from your favorite editor to VS Code. Go to **Preferences** > **Migrate Keyboard Shortcuts from...** to see the current list on the [Marketplace](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Installs). Some of the more popular ones:

* [Vim](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim)
* [Sublime Text Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings)
* [Emacs Keymap](https://marketplace.visualstudio.com/items?itemName=hiro-sun.vscode-emacs)
* [Atom Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.atom-keybindings)
* [Brackets Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.brackets-keybindings)
* [Eclipse Keymap](https://marketplace.visualstudio.com/items?itemName=alphabotsec.vscode-eclipse-keybindings)
* [Visual Studio Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vs-keybindings)

### Customize your keyboard shortcuts

Keyboard Shortcut: `kb(workbench.action.openGlobalKeybindings)`

![keyboard shortcuts](/assets/keyboard-shortcuts-mxp0jbr1vult.png)

You can search for shortcuts and add your own keybindings to the `keybindings.json` file.

![customize keyboard shortcuts](/assets/keyboardshortcuts-a0zpq8z6qqm8.gif)

See more in [[vs.1.7.docs.getstarted.keybindings]].

### Tune your settings

By default VS Code shows the Settings editor, you can find settings listed below in a search bar, but you can still edit the underlying `settings.json` file by using the **Open Settings (JSON)** command or by changing your default settings editor with the `workbench.settings.editor` setting.

Open User Settings `settings.json`

Keyboard Shortcut: `kb(workbench.action.openSettings)`

Change the font size of various UI elements

```json
// Main editor
"editor.fontSize": 18,
// Terminal panel
"terminal.integrated.fontSize": 14,
// Output panel
"[Log]": {
    "editor.fontSize": 15
}
```

Change the zoom level

```json
"window.zoomLevel": 5
```

Font ligatures

```json
"editor.fontFamily": "Fira Code",
"editor.fontLigatures": true
```

> **Tip:** You will need to have a font installed that supports font ligatures. [FiraCode](https://github.com/tonsky/FiraCode) is a popular font on the VS Code team.

![font ligatures](/assets/font-ligatures-annotated-ya7mx3wi3wr6.png)

Auto Save

```json
"files.autoSave": "afterDelay"
```

You can also toggle Auto Save from the top-level menu with the **File** > **Auto Save**.

Format on save

```json
"editor.formatOnSave": true
```

Format on paste

```json
"editor.formatOnPaste": true
```

Change the size of Tab characters

```json
"editor.tabSize": 4
```

Spaces or Tabs

```json
"editor.insertSpaces": true
```

Render whitespace

```json
"editor.renderWhitespace": "all"
```

Whitespace characters are rendered by default in text selection.

Ignore files / folders

Removes these files / folders from your editor window.

```json
"files.exclude": {
    "somefolder/": true,
    "somefile": true
}
```

Remove these files / folders from search results.

```json
"search.exclude": {
    "someFolder/": true,
    "somefile": true
}
```

And many, many [[vs.1.7.docs.getstarted.settings]].

### Language specific settings

You can scope the settings that you only want for specific languages by the language identifier. You can find a list of commonly used language IDs in the [[vs.1.7.docs.languages.identifiers]] reference.

```json
"[languageid]": {

}
```

> **Tip:** You can also create language specific settings with the **Configure Language Specific Settings** command.

![language based settings](/assets/lang-based-settings-xbvqho9qtgi8.png)

### Add JSON validation

Enabled by default for many file types. Create your own schema and validation in `settings.json`

```json
"json.schemas": [
    {
        "fileMatch": [
            "/bower.json"
        ],
        "url": "https://json.schemastore.org/bower"
    }
]
```

or for a schema defined in your workspace

```json
"json.schemas": [
    {
        "fileMatch": [
            "/foo.json"
        ],
        "url": "./myschema.json"
    }
]
```

or a custom schema

```json
"json.schemas": [
    {
        "fileMatch": [
            "/.myconfig"
        ],
        "schema": {
            "type": "object",
            "properties": {
                "name" : {
                    "type": "string",
                    "description": "The name of the entry"
                }
            }
        }
    }
]
```

See more in the [[vs.1.7.docs.languages.json]] documentation.

## Extensions

Keyboard Shortcut: `kb(workbench.view.extensions)`

### Find extensions

1. In the VS Code [Marketplace](https://marketplace.visualstudio.com/vscode).
2. Search inside VS Code in the **Extensions** view.
3. View extension recommendations
4. Community curated extension lists, such as [awesome-vscode](https://github.com/viatsko/awesome-vscode).

### Install extensions

In the **Extensions** view, you can search via the search bar or click the **More Actions** (...) button to filter and sort by install count.

![install extensions](/assets/show-popular-extensions-qudtkp5kiely.png)

### Extension recommendations

In the **Extensions** view, click **Show Recommended Extensions** in the **More Actions** (...) button menu.

![show recommended extensions](/assets/show-recommended-extensions-mxmcshz49npi.png)

### Creating my own extension

Are you interested in creating your own extension? You can learn how to do this in the [[vs.1.7.api]], specifically check out the [[vs.1.7.api.references.contribution-points]].

* configuration
* commands
* keybindings
* languages
* debuggers
* grammars
* themes
* snippets
* jsonValidation

## Files and folders

### Integrated Terminal

Keyboard Shortcut: `kb(workbench.action.terminal.toggleTerminal)`

![Integrated terminal](/assets/integrated_terminal-i0009q2v6cqv.png)

Further reading:

* [[vs.1.7.docs.terminal.basics]] documentation
* [Mastering VS Code's Terminal article](https://www.growingwiththeweb.com/2017/03/mastering-vscodes-terminal.html)

### Toggle Sidebar

Keyboard Shortcut: `kb(workbench.action.toggleSidebarVisibility)`

![toggle side bar](/assets/toggle_side_bar-z530xz1qdp4c.gif)

### Toggle Panel

Keyboard Shortcut: `kb(workbench.action.togglePanel)`

### Zen mode

Keyboard Shortcut: `kb(workbench.action.toggleZenMode)`

![zen mode](/assets/zen_mode-9zdvfz3d07w2.gif)

Enter distraction free Zen mode.

Press `kbstyle(Esc)` twice to exit Zen Mode.

### Side by side editing

Keyboard Shortcut: `kb(workbench.action.splitEditor)`

You can also drag and drop editors to create new editor groups and move editors between groups.

![split editors](/assets/split_editor-nmmr4jmkhfi7.gif)

### Switch between editors

Keyboard Shortcut: `kb(workbench.action.focusFirstEditorGroup)`, `kb(workbench.action.focusSecondEditorGroup)`, `kb(workbench.action.focusThirdEditorGroup)`

![navigate editors](/assets/navigate_editors-eun2c0wpel85.gif)

### Move to Explorer window

Keyboard Shortcut: `kb(workbench.view.explorer)`

### Create or open a file

Keyboard Shortcut: `kbstyle(Ctrl+click)` (`kbstyle(Cmd+click)` on macOS)

You can quickly open a file or image or create a new file by moving the cursor to the file link and using `kbstyle(Ctrl+click)`.

![create and open file](/assets/create_open_file-ecswutuqiuva.gif)

### Close the currently opened folder

Keyboard Shortcut: `kb(workbench.action.closeFolder)`

### Navigation history

Navigate entire history: `kb(workbench.action.quickOpenPreviousRecentlyUsedEditorInGroup)`

Navigate back: `kb(workbench.action.navigateBack)`

Navigate forward: `kb(workbench.action.navigateForward)`

![navigate history](/assets/navigate_history-0jbliuw1hg0h.gif)

### File associations

Create language associations for files that aren't detected correctly. For example, many configuration files with custom file extensions are actually JSON.

```json
"files.associations": {
    ".database": "json"
}
```

### Preventing dirty writes

VS Code will show you an error message when you try to save a file that cannot be saved because it has changed on disk. VS Code blocks saving the file to prevent overwriting changes that have been made outside of the editor.

In order to resolve the save conflict, click the **Compare** action in the error message to open a diff editor that will show you the contents of the file on disk (to the left) compared to the contents in VS Code (on the right):

![dirty write](/assets/dirty-write-vfdluiuxcym3.png)

Use the actions in the editor toolbar to resolve the save conflict. You can either **Accept** your changes and thereby overwriting any changes on disk, or **Revert** to the version on disk. Reverting means that your changes will be lost.

**Note:** The file will remain dirty and cannot be saved until you pick one of the two actions to resolve the conflict.

## Editing hacks

Here is a selection of common features for editing code. If the keyboard shortcuts aren't comfortable for you, consider installing a [keymap extension](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Installs) for your old editor.

**Tip**: You can see recommended keymap extensions in the **Extensions** view by filtering the search to `@recommended:keymaps`.

### Multi cursor selection

To add cursors at arbitrary positions, select a position with your mouse and use `kbstyle(Alt+Click)` (`kbstyle(Option+Click)` on macOS).

To set cursors above or below the current position use:

Keyboard Shortcut: `kb(editor.action.insertCursorAbove)` or `kb(editor.action.insertCursorBelow)`

![multi cursor](/assets/multicursor-d6ppdhtawoeg.gif)

You can add additional cursors to all occurrences of the current selection with `kb(editor.action.selectHighlights)`.

![add cursor to all occurrences of current selection](/assets/add_cursor_current_selection-tvkq24gq0vr9.gif)

> Note: You can also change the modifier to `kbstyle(Ctrl/Cmd)` for applying multiple cursors with the `editor.multiCursorModifier` [[vs.1.7.docs.getstarted.settings]] . See [[v[[vs.1.7.docs.editor.codebasics.md#multicursor-modifier]]r details.

If you do not want to add all occurrences of the current selection, you can use `kb(editor.action.addSelectionToNextFindMatch)` instead.
This only selects the next occurrence after the one you selected so you can add selections one by one.

![add cursor to next occurrences of current selection one by one](/assets/add_cursor_current_selection_one_by_one-luwd5je95int.gif)

### Column (box) selection

You can select blocks of text by holding `kbstyle(Shift+Alt)` (`kbstyle(Shift+Option)` on macOS) while you drag your mouse. A separate cursor will be added to the end of each selected line.

![Column text selection](/assets/column-select-jj0prspdp8fr.gif)

You can also use [[vs.1.7.docs.editor.codebasics.md#column-box-selection]] to trigger column selection.

### Vertical rulers

You can add vertical column rulers to the editor with the `editor.rulers` setting, which takes an array of column character positions where you'd like vertical rulers.

```json
{
    "editor.rulers": [
        20, 40, 60
    ]
}
```

![Editor rulers in the editor](/assets/editor-rulers-nyiyef53rp0l.png)

### Fast scrolling

Pressing the `kbstyle(Alt)` key enables fast scrolling in the editor and Explorers. By default, fast scrolling uses a 5X speed multiplier but you can control the multiplier with the **Editor: Fast Scroll Sensitivity** (`editor.fastScrollSensitivity`) setting.

### Copy line up / down

Keyboard Shortcut: `kb(editor.action.copyLinesUpAction)` or `kb(editor.action.copyLinesDownAction)`

> The commands **Copy Line Up/Down** are unbound on Linux because the VS Code default keybindings would conflict with Ubuntu keybindings, see [Issue #509](https://github.com/microsoft/vscode/issues/509). You can still set the commands `editor.action.copyLinesUpAction` and `editor.action.copyLinesDownAction` to your own preferred keyboard shortcuts.

![copy line down](/assets/copy_line_down-ob8fpfr6ayua.gif)

### Move line up and down

Keyboard Shortcut: `kb(editor.action.moveLinesUpAction)` or `kb(editor.action.moveLinesDownAction)`

![move line up and down](/assets/move_line-52fxv6iqmx5p.gif)

### Shrink / expand selection

Keyboard Shortcut: `kb(editor.action.smartSelect.shrink)` or `kb(editor.action.smartSelect.expand)`

![shrink expand selection](/assets/shrink_expand_selection-bqvczl8weyom.gif)

You can learn more in the [[vs.1.7.docs.editor.codebasics.md#shrinkexpand-selection]] documentation.

### Go to Symbol in File

Keyboard Shortcut: `kb(workbench.action.gotoSymbol)`

![Find by symbol](/assets/find_by_symbol-561f78i3hevr.gif)

You can group the symbols by kind by adding a colon, `@:`.

![group symbols by kind](/assets/group_symbols_by_kind-ct2canoauwx9.png)

### Go to Symbol in Workspace

Keyboard Shortcut: `kb(workbench.action.showAllSymbols)`

![go to symbol in workspace](/assets/go_to_symbol_in_workspace-1a6gf26fkpxe.png)

### Outline view

The Outline view in the File Explorer (default collapsed at the bottom) shows you the symbols of the currently open file.

![Outline view](/assets/outline-view-f0lgdufa23l3.png)

You can sort by symbol name, category, and position in the file and allows quick navigation to symbol locations.

### Navigate to a specific line

Keyboard Shortcut: `kb(workbench.action.gotoLine)`

### Undo cursor position

Keyboard Shortcut: `kb(cursorUndo)`

### Trim trailing whitespace

Keyboard Shortcut: `kb(editor.action.trimTrailingWhitespace)`

![trailing whitespace](/assets/trim_whitespace-tdmwows50q6k.gif)

### Transform text commands

You can change selected text to uppercase, lowercase, and title case with the **Transform** commands from the Command Palette.

![Transform text commands](/assets/transform-text-commands-l9ask4vunlwf.png)

### Code formatting

Currently selected source code: `kb(editor.action.formatSelection)`

Whole document format: `kb(editor.action.formatDocument)`

![code formatting](/assets/code_formatting-ju7vhbi8aa7n.gif)

### Code folding

Keyboard Shortcut: `kb(editor.fold)` and `kb(editor.unfold)`

![code folding](/assets/code_folding-2wz375rqra8h.gif)

You can also fold/unfold all regions in the editor with **Fold All** (`kb(editor.foldAll)`) and **Unfold All** (`kb(editor.unfoldAll)`).

You can fold all block comments with **Fold All Block Comments** (`kb(editor.foldAllBlockComments)`).

### Select current line

Keyboard Shortcut: `kb(expandLineSelection)`

### Navigate to beginning and end of file

Keyboard Shortcut: `kb(cursorTop)` and `kb(cursorBottom)`

### Open Markdown preview

In a Markdown file, use

Keyboard Shortcut: `kb(markdown.showPreview)`

![Markdown preview](/assets/markdown-preview-s8f3vfc5cfez.png)

### Side by side Markdown edit and preview

In a Markdown file, use

Keyboard Shortcut: `kb(markdown.showPreviewToSide)`

The preview and editor will synchronize with your scrolling in either view.

![side by side Markdown preview](/assets/markdown-preview-side-by-side-6no48ed2jwdp.png)

## IntelliSense

`kb(editor.action.triggerSuggest)` to trigger the Suggestions widget.

![intellisense](/assets/intellisense-u3qkf7o9mm3o.gif)

You can view available methods, parameter hints, short documentation, etc.

### Peek

Select a symbol then type `kb(editor.action.peekDefinition)`. Alternatively, you can use the context menu.

![peek](/assets/peek-0vyf2qm10a92.gif)

### Go to Definition

Select a symbol then type `kb(editor.action.revealDefinition)`. Alternatively, you can use the context menu or `kbstyle(Ctrl+click)` (`kbstyle(Cmd+click)` on macOS).

![go to definition](/assets/goto_definition-yjlm37unxdil.gif)

You can go back to your previous location with the **Go** > **Back** command or `kb(workbench.action.navigateBack)`.

You can also see the type definition if you press `kbstyle(Ctrl)` (`kbstyle(Cmd)` on macOS) when you are hovering over the type.

### Go to References

Select a symbol then type `kb(editor.action.goToReferences)`. Alternatively, you can use the context menu.

![peek references](/assets/find_all_references-86wizv3rkw3q.gif)

### Find All References view

Select a symbol then type `kb(references-view.findReferences)` to open the References view showing all your file's symbols in a dedicated view.

### Rename Symbol

Select a symbol then type `kb(editor.action.rename)`. Alternatively, you can use the context menu.

![rename symbol](/assets/rename_symbol-3drjhivjn2rb.gif)

### Search and modify

Besides searching and replacing expressions, you can also search and reuse parts of what was matched, using regular expressions with capturing groups. Enable regular expressions in the search box by clicking the **Use Regular Expression** `.*` button (`kb(toggleSearchRegex)`) and then write a regular expression and use parenthesis to define groups. You can then reuse the content matched in each group by using `$1`, `$2`, etc. in the Replace field.

![search and modify](/assets/search_and_modify-lkn0jpysbkzd.png)

### .eslintrc.json

Install the [ESLint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint). Configure
your linter however you'd like. Consult the [ESLint specification](https://eslint.org/docs/user-guide/configuring) for details on its linting rules and options.

Here is configuration to use ES6.

```json
{
    "env": {
        "browser": true,
        "commonjs": true,
        "es6": true,
        "node": true
    },
    "parserOptions": {
        "ecmaVersion": 6,
        "sourceType": "module",
        "ecmaFeatures": {
            "jsx": true,
            "classes": true,
            "defaultParams": true
        }
    },
    "rules": {
        "no-const-assign": 1,
        "no-extra-semi": 0,
        "semi": 0,
        "no-fallthrough": 0,
        "no-empty": 0,
        "no-mixed-spaces-and-tabs": 0,
        "no-redeclare": 0,
        "no-this-before-super": 1,
        "no-undef": 1,
        "no-unreachable": 1,
        "no-use-before-define": 0,
        "constructor-super": 1,
        "curly": 0,
        "eqeqeq": 0,
        "func-names": 0,
        "valid-typeof": 1
    }
}
```

### package.json

See IntelliSense for your `package.json` file.

![package json intellisense](/assets/package_json_intellisense-aqwymyzwzd3f.gif)

### Emmet syntax

[[vs.1.7.docs.editor.emmet]].

![emmet syntax](/assets/emmet_syntax-ibhuzrtir5c8.gif)

## Snippets

### Create custom snippets

**File** > **Preferences** > **User Snippets** (**Code** > **Preferences** > **User Snippets** on macOS), select the language, and create a snippet.

```json
"create component": {
    "prefix": "component",
    "body": [
        "class $1 extends React.Component {",
        "",
        "\trender() {",
        "\t\treturn ($2);",
        "\t}",
        "",
        "}"
    ]
},
```

See more details in [[vs.1.7.docs.editor.userdefinedsnippets]].

## Git integration

Keyboard Shortcut: `kb(workbench.view.scm)`

Git integration comes with VS Code "out-of-the-box". You can install other SCM providers from the Extension Marketplace. This section describes the Git integration but much of the UI and gestures are shared by other SCM providers.

### Diffs

From the **Source Control** view, select a file to open the diff.

![git diff from source control](/assets/msee-changes-i7uerxoa3ea6.gif)

Alternatively, click the **Open Changes** button in the top right corner to diff the current open file.

**Views**

The default view for diffs is the **side by side view**.

Toggle **inline view** by clicking the **More Actions** (...) button in the top right and selecting **Toggle Inline View**.

![git switch to inline diff](/assets/mdiff-switch-to-inline-tzsg7wkqap8m.png)

If you prefer the inline view, you can set `"diffEditor.renderSideBySide": false`.

**Review pane**

Navigate through diffs with `kb(editor.action.diffReview.next)` and `kb(editor.action.diffReview.prev)`. This will present them in a unified patch format.
Lines can be navigated with arrow keys and pressing `kbstyle(Enter)` will jump back in the diff editor and the selected line.

![diff_review_pane](/assets/diff_review_pane-ovppsu75t0nf.png)

**Edit pending changes**

You can make edits directly in the pending changes of the diff view.

### Branches

Easily switch between Git branches via the Status Bar.

![switch branches](/assets/mswitch-branch-fg0xxle2a1ti.gif)

### Staging

**Stage file changes**

Hover over the number of files and click the plus button.

Click the minus button to unstage changes.

![git stage all](/assets/mstage-unstage-bdvsoosoxhcg.gif)

**Stage selected**

Stage a portion of a file by selecting that file (using the arrows) and then choosing **Stage Selected Ranges** from the **Command Palette**.

### Undo last commit

Click the (...) button and then select **Undo Last Commit** to undo the previous commit. The changes are added to the Staged Changes section.

![undo last commit](/assets/mundo-last-commit-2t66381imscs.gif)

### See Git output

VS Code makes it easy to see what Git commands are actually running. This is helpful when learning Git or debugging a difficult source control issue.

Use the **Toggle Output** command (`kb(workbench.action.output.toggleOutput)`) and select **Git** in the dropdown.

### Gutter indicators

View diff decorations in editor. See [[vs.1.7.docs.editor.versioncontrol.md#gutter-indicators]] for more details.

![git gutter indicators](/assets/mgutter_icons-pb9nmzm6q2v0.gif)

### Resolve merge conflicts

During a merge, go to the **Source Control** view (`kb(workbench.view.scm)`) and make changes in the diff view.

You can resolve merge conflicts with the inline CodeLens which lets you **Accept Current Change**, **Accept Incoming Change**, **Accept Both Changes**, and **Compare Changes**.

### Set VS Code as default merge tool

```bash
git config --global merge.tool vscode
git config --global mergetool.vscode.cmd 'code --wait $MERGED'
```

### Set VS Code as default diff tool

```bash
git config --global diff.tool vscode
git config --global difftool.vscode.cmd 'code --wait --diff $LOCAL $REMOTE'
```

## Debugging

### Configure debugger

From the Run and Debug view (`kb(workbench.view.debug)`), select **create a launch.json file**, which will prompt you to select the environment that matches your project (Node.js, Python, C++, etc). This will generate a `launch.json` file. Node.js support is built-in and other environments require installing the appropriate language extensions. See the debugging [[vs.1.7.docs.editor.debugging]] for more details.

![configure debugging](/assets/configure-debug-66zosdq89noe.png)

### Breakpoints and stepping through

Place breakpoints next to the line number. Navigate forward with the Debug widget.

![debug](/assets/node_debug-g299dayzqq44.gif)

### Data inspection

Inspect variables in the **Run** panels and in the console.

![data inspection](/assets/debug_data_inspection-8gaft786lgrr.gif)

### Logpoints

Logpoints act much like breakpoints but instead of halting the debugger when they are hit, they log a message to the console. Logpoints are especially useful for injecting logging while debugging production servers that cannot be modified or paused.

Add a logpoint with the **Add Logpoint** command in the left editor gutter and it will be displayed as a "diamond" shaped icon. Log messages are plain text but can include expressions to be evaluated within curly braces ('{}').

![Logpoint set in the editor](/assets/logpoint-7sgou7v2uh5h.png)

## Task runner

### Auto detect tasks

Select **Terminal** from the top-level menu, run the command **Configure Tasks**, then select the type of task you'd like to run.
This will generate a `tasks.json` file with content like the following. See the [[vs.1.7.docs.editor.tasks]] documentation for more details.

```json
{
    // See https://go.microsoft.com/fwlink/?LinkId=733558
    // for the documentation about the tasks.json format
    "version": "2.0.0",
    "tasks": [
        {
            "type": "npm",
            "script": "install",
            "group": {
                "kind": "build",
                "isDefault": true
            }
        }
    ]
}
```

There are occasionally issues with auto generation. Check out the documentation for getting things to work properly.

### Run tasks from the Terminal menu

Select **Terminal** from the top-level menu, run the command **Run Task**, and select the task you want to run. Terminate the running task by running the command **Terminate Task**

![task runner](/assets/task_runner-1d7rlv9i9gas.gif)

### Define keyboard shortcuts for tasks

You can define a keyboard shortcut for any task. From the **Command Palette** (`kb(workbench.action.showCommands)`), select **Preferences: Open Keyboard Shortcuts File**, bind the desired shortcut to the `workbench.action.tasks.runTask` command, and define the **Task** as `args`.

For example, to bind `kbstyle(Ctrl+H)` to the `Run tests` task, add the following:

```json
{
    "key": "ctrl+h",
    "command": "workbench.action.tasks.runTask",
    "args": "Run tests"
}
```

### Run npm scripts as tasks from the Explorer

![Filter problems](/assets/script_explorer-i0214nx8e9cj.png)

From the explorer you can open a script in the editor, run it as a task, and launch it with the node debugger (when the script defines a debug option like `--inspect-brk`). The default action on click is to open the script. To run a script on a single click, set `npm.scriptExplorerAction` to "run". Use the setting `npm.exclude` to exclude scripts in `package.json` files contained in particular folders.

With the setting `npm.enableRunFromFolder`, you can enable to run npm scripts from the File Explorer's context menu for a folder. The setting enables the command **Run NPM Script in Folder...** when a folder is selected. The command shows a Quick Pick list of the npm scripts contained in this folder and you can select the script to be executed as a task.

## Portable mode

VS Code has a [[vs.1.7.docs.editor.portable]] which lets you keep settings and data in the same location as your installation, for example, on a USB drive.

## Insiders builds

The Visual Studio Code team uses the Insiders version to test the latest features and bug fixes of VS Code. You can also use the Insiders version by [[vs.1.7.insiders]].

* For Early Adopters - Insiders has the most recent code changes for users and extension authors to try out.
* Frequent Builds - New builds every day with the latest bug fixes and features.
* Side-by-side install - Insiders installs next to the Stable build allowing you to use either independently.
