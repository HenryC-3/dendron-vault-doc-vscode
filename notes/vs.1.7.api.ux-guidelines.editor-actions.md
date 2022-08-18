---
id: op8out2r09q7nhoen6l6ho7
title: Editor Actions
desc: ''
updated: 1660824078434
created: 1660824078434
isDir: false
ContentId: ce5c9fff-df86-454a-b4e8-4ae05c8158e2
DateApproved: 8/4/2022
MetaDescription: UX guidelines for editor actions in a Visual Studio Code extension.
---

# Editor Actions

[[vs.1.7.api.references.contribution-points#contributes.commands]] can appear in the editor toolbar. You can either add an icon as a quick action or add menu item under the overflow menu (**...**).

**✔️ Do**

* Show only when contextually appropriate
* Use icons from the icon library
* Use the overflow menu for secondary actions

❌ Don't

* Add more than one icon
* Add custom colors
* Use emojis

![Editor Actions](/assets/editor-actions-tmsxezgkjweq.png)

*This example from the GitHub Pull Requests and Issues extension opens a diff view and only shows on files with changes.*

## Links

* [[vs.1.7.api.extension-guides.custom-editors]]
* [[vs.1.7.api.references.contribution-points#contributes.customEditors]]
* [Custom Editor extension sample](https://github.com/microsoft/vscode-extension-samples/tree/main/custom-editor-sample)
* [[vs.1.7.api.extension-guides.webview]]
* [Webview extension sample](https://github.com/microsoft/vscode-extension-samples/blob/main/webview-sample)
