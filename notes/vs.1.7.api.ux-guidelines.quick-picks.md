---
id: hvku5ajuhadd8j6jxi2c4wi
title: Quick Picks
desc: ''
updated: 1660824078434
created: 1660824078434
isDir: false
ContentId: 85918f63-ff5d-4ab8-8a18-26ad00618eff
DateApproved: 8/4/2022
MetaDescription: UX guidelines for quick picks used in a Visual Studio Code extension.
---

# Quick Picks

[[vs.1.7.api.extension-capabilities.common-capabilities#quick-pick]] are an easy way to perform actions and receive input from the user. This is helpful when selecting a configuration option, needing to filter content, or picking from a list of items.

![Quick Pick example](/assets/quick-pick-3zf081tib7ej.png)

**✔️ Do**

* Use icons for clear metaphors
* Use the description for displaying the current items (if applicable)
* Use the detail for providing (brief) additional context
* Use the multi-step pattern for a series of basic inputs
* Provide an option to create a new item when picking from a list (if applicable)

❌ Don't

* Repeat existing functionality
* Use the same icon for multiple items
* Use more than six icons in a list

## Multiple Steps

Quick Picks can be configured to feature multiple steps. Use these when you need to capture related-but-separate selections in a single flow. Avoid using quick picks for long flows with many steps—they aren't well suited to function as a wizard or similarly complex experience.

![Multi-step Quick Pick example](/assets/quick-pick-multi-step-exc53f0j8vyl.png)

## Multiple Selections

Use a multi-select quick pick for closely-related selections that need to be selected in one step.

![Multi-step Quick Pick example](/assets/quick-pick-multi-select-3z90mwzpzlt4.png)

*Notes the "1/3" text in the Quick Pick title that indicates the current and total number of steps in the flow.*

## Title

Quick Picks can be also be configured to show a title bar above the main input and selection UI. Use a title when the user needs more context for the selection being made. Avoid using a title that uses a label already used in the Quick Pick's input placeholder.

![Multi-step Quick Pick example](/assets/quick-pick-title-j2p8f62bcqa3.png)

## Using Separators

Quick Pick Items can be grouped into clear sections using Quick Pick Separators. These feature a divider and label to clearly show the section. Use separators if the extension features a quick pick containing multiple obvious groups of selections.

![Quick Pick with separators](/assets/quick-pick-separators-7c59pj4unybh.png)

## Links

* [[vs.1.7.api.references.vscode-api#QuickPick]]
* [[vs.1.7.api.references.vscode-api#QuickPickItem]]
* [Quick Pick extension sample](https://github.com/microsoft/vscode-extension-samples/tree/main/quickinput-sample)
