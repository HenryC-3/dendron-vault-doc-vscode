---
id: pbl1110bc4ddr5bwdkzpcb9
title: Command Palette
desc: ''
updated: 1660824078434
created: 1660824078434
isDir: false
ContentId: bf0d9a5e-897b-450a-adf4-3c8ca9b8e9de
DateApproved: 8/4/2022
MetaDescription: UX guidelines for the Command Palette in a Visual Studio Code extension.
---

# Command Palette

The [[vs.1.7.api.references.contribution-points#contributes.commands]] is where all Commands are found. It's important that your command names are labeled appropriately so users can easily find them.

**✔️ Do**

* Add keyboard shortcuts where appropriate
* Use clear names for commands
* Group commands together in the same category

❌ Don't

* Overwrite existing keyboard shortcuts
* Use emojis in command names

![Command Palette](/assets/command-palette-bjtbtjmbb7vt.png)

*This example features commands each displaying a clear `category` prefix, for example "GitHub Issues".*

## Links

* [[vs.1.7.api.references.contribution-points#contributes.commands]]
* [[vs.1.7.api.extension-guides.command]]
* [Hello World extension sample](https://github.com/microsoft/vscode-extension-samples/tree/main/helloworld-sample)
