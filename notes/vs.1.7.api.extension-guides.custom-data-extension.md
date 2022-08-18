---
id: fu7sosmxz2r0m5xt36kcjch
title: Custom Data Extension
desc: ''
updated: 1660824078426
created: 1660824078426
isDir: false
ContentId: d40b8849-6a4e-428c-b463-c8d61f18136f
DateApproved: 8/4/2022
MetaDescription: Learn how to extend Visual Studio Code's HTML and CSS language support.
---

# Custom Data Extension

[Custom Data format](https://github.com/microsoft/vscode-custom-data) allows extension authors to easily extend VS Code's HTML / CSS language support without having to write code.

The two [[vs.1.7.api.references.contribution-points]] for using custom data in an extension are:

- `contributes.html.customData`
- `contributes.css.customData`

For example, by including this section in an extension's `package.json`:

```json
{
  "contributes": {
    "html": {
      "customData": ["./html.html-data.json"]
    },
    "css": {
      "customData": ["./css.css-data.json"]
    }
  }
}
```

VS Code will load the HTML/CSS entities defined in both files and provide language support such as auto-completion and hover information for those entities.

You can find the [custom-data-sample](https://github.com/microsoft/vscode-extension-samples/tree/main/custom-data-sample) at [microsoft/vscode-extension-samples](https://github.com/microsoft/vscode-extension-samples).
