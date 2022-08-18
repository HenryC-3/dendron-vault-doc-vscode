---
id: 1hsbldyyuctgy8ngmlfdgee
title: Settings
desc: ''
updated: 1660824078434
created: 1660824078434
isDir: false
ContentId: 9f5daebb-1566-46b8-a04d-0fd6c5d4a926
DateApproved: 8/4/2022
MetaDescription: UX guidelines for settings contributed by a Visual Studio Code extension.
---

# Settings

[[vs.1.7.api.references.contribution-points#contributes.configuration]] are how a user can configure your extension. Settings can be inputs boxes, booleans, dropdowns, lists, key/value pairs. If your extension requires the user to configure specific settings, you can open the Settings UI and query your extension setting via the setting ID.

**✔️ Do**

* Add default values to each setting
* Add clear descriptions to each setting
* Link to documentation for complicated settings
* Link to additional settings that are related
* Link to setting IDs when needing the user to configure specific settings

❌ Don't

* Create your own settings page/webview
* Create long descriptions

![Settings](/assets/settings-jh7gwt07gzy5.png)

*This example links to a specific setting using the setting ID.*

## Links

* [[vs.1.7.api.references.contribution-points#contributes.configuration]]
