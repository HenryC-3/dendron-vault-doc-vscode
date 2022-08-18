---
id: 1nbnztbzv6r0fuh8yhxdt4y
title: Overview
desc: ''
updated: 1660824078434
created: 1660824078434
isDir: false
ContentId: 5b4962ff-2dc9-4201-aa95-46edb5a575b6
DateApproved: 8/4/2022
MetaDescription: >-
  Guidelines that showcase best practices for creating Visual Studio Code
  extensions.
---

# UX Guidelines

These guidelines cover the best practices for creating extensions that seamlessly integrate with VS Code's native interface and patterns. In these guidelines, you can expect to find:

- An outline of VS Code's overall UI architecture and elements
- Recommendations and examples for UI contributed by an extension
- Links to relevant guides and samples

Before diving into the details, it's important to understand how the various architectural UI parts of VS Code fit together and how and where your extension could contribute.

## Containers

The VS Code interface can roughly be divided into two main concepts: **containers** and **items**. Generally speaking, containers can be considered the larger sections of the VS Code interface that render one or more items:

[![Overview of Visual Studio Code containers elements](/assets/architecture-containers-a9afce94dzfd.png)](/assets/api/ux-guidelines/examples/architecture-containers.png)

### Activity Bar

The [[vs.1.7.api.ux-guidelines.activity-bar]] is a core navigation surface in VS Code. Extensions can contribute items to the Activity Bar that function as [[vs.1.7.api.references.contribution-points#contributes.viewsContainers]] that render [[vs.1.7.api.ux-guidelines.views]] in the Primary Sidebar.

### Primary Sidebar

The [[vs.1.7.api.ux-guidelines.sidebars#primary-sidebar]] renders one or more [[vs.1.7.api.ux-guidelines.views]]. The Activity Bar and the Primary Sidebar are tightly coupled. Clicking on a contributed Activity Bar Item (read: View Container) opens up the Primary Sidebar where one or more View associated with that View Container will be rendered. A concrete example would be the Explorer. Clicking on the Explorer Item will open up the Primary Sidebar where the Folder(s), Timeline, and Outline Views are visible.

### Secondary Sidebar

The [[vs.1.7.api.ux-guidelines.sidebars#secondary-sidebar]] also functions as a surface for rendering a View Container with Views. Users can drag views like the Terminal or the Problems view to the Secondary Sidebar to customize their layout.

### Editor

The Editor area contains one or more Editor Groups. Extensions can contribute [[vs.1.7.api.references.contribution-points#contributes.customEditors]] or [[vs.1.7.api.extension-guides.webview]] to open in the Editor area. They can also contribute [[vs.1.7.api.ux-guidelines.editor-actions]] to expose additional icon buttons in the Editor Toolbar.

### Panel

The [[vs.1.7.api.ux-guidelines.panel]] is another area for exposing View Containers. By default, Views like the Terminal, Problems, and Output can be viewed in a single tab at a time in the Panel. Users can also drag views into a split layout much like they can do in the Editor. Additionally, extensions can choose to add View Containers specifically to the Panel instead of the Activity Bar/Primary Sidebar.

### Status Bar

The [[vs.1.7.api.ux-guidelines.status-bar]] provides contextual information about the workspace and currently active file. It renders two groups of [[vs.1.7.api.ux-guidelines.status-bar#status-bar-items]].

## Items

Extensions can add items to the various containers listed above.

[![Overview of Visual Studio Code containers elements](/assets/architecture-sections-pljzpmeqlcwq.png)](/assets/api/ux-guidelines/examples/architecture-sections.png)

### View

[[vs.1.7.api.ux-guidelines.views]] can be contributed in the form of a [[vs.1.7.api.ux-guidelines.views#tree-views]], [[vs.1.7.api.ux-guidelines.views#welcome-views]], or [[vs.1.7.api.ux-guidelines.webviews#webview-views]] and can be dragged around to other areas of the interface.

### View Toolbar

Extensions can expose View-specific [[vs.1.7.api.ux-guidelines.views#view-actions]] that appear as buttons on a View Toolbar.

### Sidebar Toolbar

Actions scoped to an entire View Container can also be exposed in the [[vs.1.7.api.ux-guidelines.sidebars#sidebar-toolbars]].

### Editor Toolbar

Extensions can contribute [[vs.1.7.api.ux-guidelines.editor-actions]] scoped to an editor directly in the Editor Toolbar.

### Panel Toolbar

The [[vs.1.7.api.ux-guidelines.panel#panel-toolbar]] can expose options scoped to the currently selected View. For example the Terminal view exposes actions to add a new terminal, split the view layout, and more. Switching to the Problems view exposes a different set of actions.

### Status Bar Item

On the left, [[vs.1.7.api.ux-guidelines.status-bar#status-bar-items]] are scoped to the entire Workspace. On the right, items are scoped to the active file.

## Common UI Elements

### Command Palette

Extensions can contribute Commands that appears in the [[vs.1.7.api.ux-guidelines.command-palette]] to quickly execute some functionality.

[![Overview of the Command Palette element](/assets/command-palette-bjtbtjmbb7vt.png)](/assets/command-palette-bjtbtjmbb7vt.png).png)

### Quick Pick

[[vs.1.7.api.ux-guidelines.quick-picks]] capture a user's input in several different ways. They can ask for a single selection, multiple selections, or even freeform text input.

![Overview of the Quick Pick element](/assets/quick-pick-3zf081tib7ej.png)

### Notifications

[[vs.1.7.api.ux-guidelines.notifications]] are used to communicate information, warning, and error messages to users. They can also be used to indicate progress.

![Overview of the Notification element](/assets/notification-kpbt5k41cdvb.png)

### Webviews

[[vs.1.7.api.ux-guidelines.webviews]] can be used to display custom content and functionality for use cases that go beyond VS Code's "native" API.

![Overview of the Webview element](/assets/webview-gsto8tiae4nv.png)

### Context Menus

In contrast to the Command Palette's consistent location, [[vs.1.7.api.ux-guidelines.context-menus]] give users the ability to perform actions or configure something from a specific location.

![Overview of the Context Menu element](/assets/context-menu-z4q6j9xtii72.png)

### Walkthroughs

[[vs.1.7.api.ux-guidelines.walkthroughs]] provide a consistent experience for onboarding users to an extension via a multi-step checklist featuring rich content.

![Overview of the Walkthrough API](/assets/walkthrough-3jq198cr4733.png)

### Settings

[[vs.1.7.api.ux-guidelines.settings]] enable users to configure options relevant to the extension.

![Overview of the Settings page](/assets/settings-jh7gwt07gzy5.png)
