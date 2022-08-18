---
id: 82id6jzpj042obwpg7cjqnu
title: Snippet Guide
desc: ''
updated: 1660824078431
created: 1660824078431
isDir: false
ContentId: 4b24790b-781a-43cc-afe6-58b1d57d6163
DateApproved: 8/4/2022
MetaDescription: >-
  Learn how to bundle snippets into an extension (plug-in) for Visual Studio
  Code
---

# Snippet Guide

The [[vs.1.7.api.references.contribution-points#contributes.snippets]] Contribution Point allows you to bundle snippets into a Visual Studio Code extension for sharing.

The [Creating snippets](https://code.visualstudio.com/docs/editor/userdefinedsnippets#_creating-your-own-snippets) topic contains all information for creating snippets. This guide / sample just shows how you can turn your own snippets into an extension for sharing. The suggested workflow is:

- Create and test your snippets using `Preferences: Configure User Snippets` command
- Once you are happy with the snippets, copy the whole JSON file into an extension folder, such as `snippets.json`
- Add the following snippet contribution to your `package.json`

```json
{
  "contributes": {
    "snippets": [
      {
        "language": "javascript",
        "path": "./snippets.json"
      }
    ]
  }
}
```

You can find the complete source code at: [https://github.com/microsoft/vscode-extension-samples/tree/main/snippet-sample](https://github.com/microsoft/vscode-extension-samples/tree/main/snippet-sample).

**Tip**: Tag your extension as a snippet extension with the following config in your `package.json`:

```json
{
  "categories": ["Snippets"]
}
```

## Using TextMate snippets

You can also add TextMate snippets (.tmSnippets) to your VS Code installation using the [[vs.1.7.api.get-started.your-first-extension]] extension generator. The generator has an option `New Code Snippets` which lets you point to a folder containing multiple .tmSnippets files and they will be packaged into a VS Code snippet extension. The generator also supports Sublime snippets (.sublime-snippets).

The final generator output has two files: an extension manifest `package.json` which has metadata to integrate the snippets into VS Code and a `snippets.json` file which includes the snippets converted to the VS Code snippet format.

```bash
.
├── snippets                    // VS Code integration
│   └── snippets.json           // The JSON file w/ the snippets
└── package.json                // extension's manifest
```

Copy the generated snippets folder to a new folder under your `.vscode/extensions` folder and restart VS Code.
