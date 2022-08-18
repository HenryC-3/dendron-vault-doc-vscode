---
id: phxz4k075dkwh4myr1z3n1g
title: Activity Bar
desc: ''
updated: 1660824078433
created: 1660824078433
isDir: false
ContentId: 13b649f1-156f-489a-9c03-c2cff8060733
DateApproved: 8/4/2022
MetaDescription: UX guidelines for the Activity Bar in a Visual Studio Code extension.
---

# Activity Bar

The Activity Bar is a core navigation surface in VS Code. Extensions can contribute [[vs.1.7.api.ux-guidelines.views#view-containers]] to the Activity Bar that appear as Activity Bar Items. Users can drag the item to other locations like the Panel to customize their layout.

**✔️ Do**

- Use an icon that matches the default Activity Bar item icon style
- Use a clear, obvious name for the [[vs.1.7.api.ux-guidelines.views#view-containers]] associated with the item

**❌ Don't**

- Duplicate an existing icon
- Use an Activity Bar item to open a Webview Panel

![Example of the Activity Bar](/assets/activity-bar-w2qd1jcyxahe.png)

## Links Resources

- [[vs.1.7.api.references.contribution-points#contributes.viewsContainers]]
- [[vs.1.7.api.references.contribution-points#contributes.views]]
