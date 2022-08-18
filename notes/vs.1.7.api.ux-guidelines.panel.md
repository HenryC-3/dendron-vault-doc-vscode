---
id: 8mlga7y8nd1iy1l1b2rngco
title: Panel
desc: ''
updated: 1660824078434
created: 1660824078434
isDir: false
ContentId: 06ce3b57-9fd5-428a-98aa-d730edbd2728
DateApproved: 8/4/2022
MetaDescription: UX guidelines for the Panel Bar in a Visual Studio Code extension.
---

# Panel

The Panel functions as another main area to display [[vs.1.7.api.references.contribution-points#contributes.viewsContainers]].

**✔️ Do**

- Render Views in the Panel that benefit from more horizontal space
- Use for Views that provide supporting functionality

**❌ Don't**

- Use for Views that are meant to be always visible since users often minimize the Panel
- Render custom Webview content that fails to resize/reflow properly when dragged to other View Containers (like the Primary or Secondary Sidebars).

![Example of a panel](/assets/panel-xb3hcyobn0v0.png)

## Panel Toolbar

The Panel Toolbar can expose options scoped to the currently selected View. For example the Terminal view exposes [[vs.1.7.api.extension-guides.tree-view#view-actions]] to add a new terminal, split the view layout, and more. Switching to the Problems view exposes a different set of actions. Similar to the [[vs.1.7.api.ux-guidelines.sidebars#sidebar-toolbar]], the toolbar will only render if there is just a single View. If more than one View is used, each View will render its own toolbar.

**✔️ Do**

- Use an existing [[vs.1.7.api.references.icons-in-labels#icon-listing]] if available
- Provide clear, useful tooltips

**❌ Don't**

- Don't add an excessive number of icon buttons. Consider using a [[vs.1.7.api.references.contribution-points#contributes.menus]] if more options are needed for a specific button.
- Don't duplicate the default Panel icons (collapse/expand, close, etc.)

![Example of a panel toolbar with a single view](/assets/panel-toolbar-ffliq2wwjm1e.png)

*In this example, the single View rendered in the Panel renders its View Actions in the main Panel Toolbar.*

![Example of a panel toolbar with multiple views](/assets/panel-toolbar-multiple-views-9ihl4v34un3q.png)

*In this example, multiple Views are used, so each View exposes its own specific View Actions.*

## Links

- [[vs.1.7.api.references.contribution-points#contributes.viewsContainers]]
- [[vs.1.7.api.references.contribution-points#contributes.views]]
- [[vs.1.7.api.extension-guides.tree-view#view-actions]]
