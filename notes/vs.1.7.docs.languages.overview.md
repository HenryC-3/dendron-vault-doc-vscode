---
id: by3a2mobi7cabpgutufknp7
title: Overview
desc: ''
updated: 1660824078453
created: 1660824078453
isDir: false
Order: 1
Area: languages
TOCTitle: Overview
ContentId: AC888642-FBE5-43E5-9DC2-47B197717940
PageTitle: Language Support in Visual Studio Code
DateApproved: 8/4/2022
MetaDescription: >-
  In Visual Studio Code we have support for all common languages including smart
  code completion and debugging.
---
# Programming Languages

## Hundreds of programming languages supported

In Visual Studio Code, we have support for almost every major programming language. Several ship in the box, for example, JavaScript, TypeScript, CSS, and HTML but more rich language extensions can be found in the [VS Code Marketplace](https://marketplace.visualstudio.com/vscode/Languages).

Here are eight of the most popular language extensions:

<div class="marketplace-extensions-languages-curated"></div>

Go to the [Marketplace](https://marketplace.visualstudio.com/vscode) or use the integrated [[vs.1.7.docs.editor.extension-marketplace]] and search for your desired programming language to find snippets, code completion/IntelliSense providers, linters, debuggers, and more.

>**Note**: If you want to change the display language of VS Code (for example, to Chinese), see the [[vs.1.7.docs.getstarted.locales]] topic.

## Language specific documentation

Learn about programming languages supported by VS Code. These include: [[vs.1.7.docs.languages.cpp]] - [[v[[vs.1.7.docs.languages.csharp]][[vs.1[[vs.1.7.docs.languages.css]]rt](https://dart.dev/tools/vs-code) - [[vs.1.7.[[vs.1.7.docs.azure.docker]].7.doc[[vs.1.7.docs.languages.dotnet.md#create-an-f-hello-world-app]]doc[[vs.1.7.docs.languages.go]]docs.l[[vs.1.7.docs.languages.html]]s.lang[[vs.1.7.docs.languages.java]]anguag[[vs.1.7.docs.languages.javascript]]uages.[[vs.1.7.docs.languages.json]]es.jul[[vs.1.7.docs.languages.julia]]css.md[[vs.1.7.docs.languages.css]]
[[vs.1.7.docs.languages.markdown]] - [[v[[vs.1.7.docs.languages.php]][[vs.1[[vs.1.7.docs.languages.powershell]]s.1.7.[[vs.1.7.docs.languages.python]].7.doc[[vs.1.7.docs.languages.r]]docs.l[[vs.1.7.docs.languages.rust]]s.lang[[vs.1.7.docs.languages.css]]anguag[[vs.1.7.docs.languages.tsql]]uages.[[vs.1.7.docs.languages.typescript]]

Click on any linked item to get an overview of how to use VS Code in the context of that language. Most language extensions also contain a summary of their core features in their README.

## Language features in VS Code

The richness of support varies across the different languages and their extensions:

* Syntax highlighting and bracket matching
* Smart completions (IntelliSense)
* Linting and corrections
* Code navigation (Go to Definition, Find All References)
* Debugging
* Refactoring

## Changing the language for the selected file

In VS Code, we default the language support for a file based on its filename extension. However, at times you may want to change language modes, to do this click on the language indicator - which is located on the right hand of the Status Bar. This will bring up the **Select Language Mode** dropdown where you can select another language for the current file.

![Language Selector](/assets/languageselect-lmm21x2p4jbk.png)

**Tip**: You can get the same dropdown by running the **Change Language Mode** command (`kb(workbench.action.editor.changeLanguageMode)`).

## Language identifier

VS Code associates a language mode with a specific language identifier so that various VS Code features can be enabled based on the current language mode.

A language identifier is often (but not always) the lowercased programming language name. Note that casing matters for exact identifier matching ('Markdown' != 'markdown'). Unknown language files have the language identifier `plaintext`.

You can see the list of currently installed languages and their identifiers in the **Change Language Mode** (`kb(workbench.action.editor.changeLanguageMode)`) dropdown.

![language identifiers](/assets/language-identifiers-ah7xlw2zs8fh.png)

You can find a list of known identifiers in the [[vs.1.7.docs.languages.identifiers]].

## Adding a file extension to a language

You can add new file extensions to an existing language with the `files.associations` [[vs.1.7.docs.getstarted.settings]].

For example, the setting below adds the `.myphp` file extension to the `php` language identifier:

```json
    "files.associations": {
        "*.myphp": "php"
    }
```

IntelliSense (`kb(editor.action.triggerSuggest)`) will show you the available language identifiers.

![Language ID IntelliSense](/assets/language-id-intellisense-h09gj6vfd1if.png)

## Next steps

Now you know that VS Code has support for the languages you care about. Read on...

* [[vs.1.7.docs.editor.editingevolved]] - Peek and Go to Definition and more
* [[vs.1.7.docs.editor.debugging]] - This is where VS Code really shines

## Common questions

### Can I contribute my own language service?

Yes you can! Check out the [[vs.1.7.api.language-extensions.language-server-extension-guide]] in the [[v[[vs.1.7.api]]cumentation.

### What if I don't want to create a full language service, can I reuse existing TextMate bundles?

Yes, you can also add support for your favorite language through TextMate colorizers. See the [[vs.1.7.api.language-extensions.syntax-highlight-guide]] in the Extension API section to learn how to integrate TextMate `.tmLanguage` syntax files into VS Code.

### Can I map additional file extensions to a language?

Yes, with the `files.associations` [[vs.1.7.docs.getstarted.settings]] you can map file extensions to an existing language either globally or per workspace.

Here is an example that will associate more file extensions to the PHP language:

```json
"files.associations": {
    "*.php4": "php",
    "*.php5": "php"
}
```

You can also configure full file paths to languages if needed. The following example associates all files in a folder `somefolder` to PHP:

```json
"files.associations": {
    "**/somefolder/*.*": "php"
}
```

Note that the pattern is a [glob pattern](https://en.wikipedia.org/wiki/Glob_%28programming%29) that will match on the full path of the file if it contains a `/` and will match on the file name otherwise.

### How do I set the default language for new files?

Using the `files.defaultLanguage` [[vs.1.7.docs.getstarted.settings]], you can map all new files to a default language. Whenever a new blank file is opened, the editor will be configured for that language mode.

This example will associate new files with the HTML language:

```json
  // The default language mode that is assigned to new files.
  "files.defaultLanguage": "html"
```
