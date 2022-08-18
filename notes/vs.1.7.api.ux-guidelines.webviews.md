---
id: oojauu2hgl2uqkk2yc4tivc
title: Webviews
desc: ''
updated: 1660824078435
created: 1660824078435
isDir: false
ContentId: 1c1f6d51-5914-44fa-ae10-0360be0ae2a3
DateApproved: 8/4/2022
MetaDescription: UX guidelines for webviews in a Visual Studio Code extension.
---

# Webviews

If you need to display custom functionality that is beyond what the VS Code API supports, you can use [[vs.1.7.api.extension-guides.webview]], which are fully customizable. It's important to understand that webviews should only be used if you absolutely need them.

**✔️ Do**

* Only use webviews when absolutely necessary
* Activate your extension only when contextually appropriate
* Open webviews only for the active window
* Ensure all elements in the view are themeable (see the [webview-view-sample](https://github.com/microsoft/vscode-extension-samples/blob/main/webview-view-sample/media/main.css) and [[vs.1.7.api.references.theme-color]] documentation)
* Ensure your views follow [[vs.1.7.docs.editor.accessibility]] (color contrast, ARIA labels, keyboard navigation)
* Use the [Webview UI Toolkit for Visual Studio Code](https://github.com/microsoft/vscode-webview-ui-toolkit) to align your extension with VS Code's styling, theme, behavior, and accessibility characteristics.
* Use command actions in the toolbar and in the view

❌ Don't

* Use for promotions (upgrades, sponsors, etc.)
* Use for wizards
* Open on every window
* Open on extension updates (ask via a Notification instead)
* Add functionality that is unrelated to the editor or workspace
* Repeat existing functionality (Welcome page, Settings, configuration, etc.)

## Webview examples

**Simple Browser**

This extension opens a browser preview for the editor to the side.

![Weview sample - Browser](/assets/webview-browser-ij558lyba5us.png)

*This example shows VS Code Web being developed right inside VS Code. A Webview panel is used to render a browser-like window.*

**Pull Request**

This extension shows pull requests for the repository of the workspace in a custom tree view and then uses a webview for a detail view of the pull request.

![Webview sample - Pull Request](/assets/webview-pull-request-2o2sdeqtezec.png)

## Webview views

You can also place webviews into any view container (sidebar or panel) and these elements are called [[vs.1.7.api.references.vscode-api#WebviewView]]. The same webview guidance applies to webview views.

![Webview View](/assets/webview-view-gu1m32561s2x.png)

*This webview view shows content for creating a pull request that uses dropdowns, inputs, and buttons.*

## Links

* [[vs.1.7.api.extension-guides.webview]]
* [Webview extension sample](https://github.com/Microsoft/vscode-extension-samples/tree/main/webview-sample)
* [Webview View extension sample](https://github.com/microsoft/vscode-extension-samples/tree/main/webview-view-sample)
* [Webview UI Toolkit for Visual Studio Code](https://github.com/microsoft/vscode-webview-ui-toolkit)
