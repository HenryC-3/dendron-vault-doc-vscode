---
id: ksdu8sno1r0krnbd1h78a1j
title: Status Bar
desc: ''
updated: 1660824078435
created: 1660824078435
isDir: false
ContentId: 2d16d367-2831-47ca-8f0e-22e3e5fd24bc
DateApproved: 8/4/2022
MetaDescription: >-
  UX guidelines for status bar and status bar items in a Visual Studio Code
  extension.
---

# Status Bar

The [[vs.1.7.api.extension-capabilities.extending-workbench#status-bar-item]] sits at the bottom of the VS Code workbench and displays information and actions that relate to your workspace. Items are placed into two groups: Primary (left) and Secondary (right). Items that relate to the entire workspace (status, problems/warnings, sync) go on the left and items that are secondary or contextual (language, spacing, feedback) go on the right. Limit the number of items added, as other extensions contribute to the same area.

![Status Bar example](/assets/status-bar-vi92ooco82x6.png)

**✔️ Do**

* Use short text labels
* Use icons only when necessary
* Use icons only for clear metaphors
* Place primary (global) items on the left
* Place secondary (contextual) items on the right

**❌ Don't**

* Add custom colors
* Add more than one icon (unless necessary)
* Add more than one item (unless necessary)

## Status Bar Items

![Status Bar Item](/assets/status-bar-item-ej75zl3xtdcs.png)

*This example shows an item contributed by the GitHub Pull Requests and Issues extension. It relates to the entire workspace, so it is placed on the left.*

### Progress Status Bar item

When needing to show discreet progress (progress happening in the background), it's recommended to show a Status Bar item with the loading icon (you can also add spin animation). If progress needs to be elevated for user attention, we recommend moving to a progress notification.

![Status Bar Progress](/assets/status-bar-progress-areyvhgstjp6.png)

*This example shows a progress Status Bar item that is discreet.*


### Error and Warning Status Bar Items

If you need to show an item that is highly visible for warning or error purposes, you can configure a Status Bar Item to use a warning or error background color. Only use this pattern as a last resort and only for special cases given their prominence in the Status Bar.

![Status Bar Error](/assets/status-bar-error-exjwz2z9aytl.png)

*This example uses the error Status Bar Item for showing a blocking error in the file.*

![Status Bar Warning](/assets/status-bar-warning-jth1nmbogaeq.png)

*This example uses the warning Status Bar Item for showing a warning in the file.*

## Links

* [[vs.1.7.api.references.vscode-api#StatusBarItem]]
* [Status Bar extension sample](https://github.com/microsoft/vscode-extension-samples/tree/main/statusbar-sample)
