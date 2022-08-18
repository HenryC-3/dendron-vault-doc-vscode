---
id: zxjmj7hywjlh0ru5tgp9ko2
title: Emberjs Tutorial
desc: ''
updated: 1660824078454
created: 1660824078454
isDir: false
Order: 9
Area: nodejs
TOCTitle: Ember Tutorial
ContentId: 4a60ed36-93ff-4ff3-b650-ce74baa405ca
PageTitle: Ember JavaScript Tutorial in Visual Studio Code
DateApproved: 8/4/2022
MetaDescription: >-
  Ember JavaScript tutorial showing IntelliSense and code navigation support in
  the Visual Studio Code editor.
---
# Using Ember in Visual Studio Code

[Ember](https://emberjs.com/) is a popular JavaScript framework for building web application user interfaces. The Visual Studio Code editor supports Ember.js IntelliSense and code navigation out of the box.

![Welcome to app](/assets/tomster-logo-p05t9jiygei0.png)

## Welcome to Ember

We'll be using the [Ember CLI](https://ember-cli.com/) for this tutorial. To install and use the command line interface as well as run the Ember.js application server, you'll need the [Node.js](https://nodejs.org/) JavaScript runtime and [npm](https://www.npmjs.com/) (the Node.js package manager) installed. npm is included with Node.js which you can install from [Node.js downloads](https://nodejs.org/en/download/).

>**Tip**: To test that you have Node.js and npm correctly installed on your machine, you can type `node --version` and `npm --version`.

To install Ember CLI, in a terminal or command prompt type:

```bash
npm install -g ember-cli
```

This may take a few minutes to install. You can now create a new Ember.js application by typing:

```bash
ember new my-app
```

`my-app` is the name of the folder for your application. This may take a few minutes to create the Ember application in [[vs.1.7.docs.languages.javascript]] and install its dependencies.

Let's quickly run our Ember application by navigating to the new folder and typing `ember serve` to start the web server and open the application in a browser:

```bash
cd my-app
ember serve
```

Once you see the **Build successful** message, you can open your browser to [[vs.1.7.http:..localhost:4200]] and you  should see "Congratulations, you made it!". You can press `kbstyle(Ctrl+C)` to stop the Ember server.

![Ember welcome page](/assets/welcome-page-atncr92msfd7.png)

To open your Ember application in VS Code, open another terminal (or command prompt) and navigate to the `my-app` folder and type `code .`:

```bash
cd my-app
code .
```

### Syntax highlighting and bracket matching

Now expand the `app` folder and select the `app.js` file. You'll notice that VS Code has syntax highlighting for the various source code elements and, if you put the cursor on a parentheses, the matching bracket is also selected.

![react bracket matching](/assets/bracket-matching-b53mrfp4fdsj.png)

## IntelliSense

As you start typing in `app.js`, you'll see smart suggestions or completions.

![Ember suggestions](/assets/suggestions-pg9nmbkcvrm4.png)

After you select a suggestion and type `.`, you see the types and methods on the object through [[vs.1.7.docs.editor.intellisense]].

![Ember intellisense](/assets/intellisense-moro2e7ryes2.png)

VS Code uses the TypeScript language service for its JavaScript code intelligence and it has a feature called [[vs.1.7.docs.nodejs.working-with-javascript.md#typings-and-automatic-type-acquisition]] (ATA). ATA pulls down the npm Type Declaration files (`*.d.ts`) for the npm modules referenced in the `package.json`.

If you select a method, you'll also get parameter help:

![Ember parameter help](/assets/parameter-help-0khc8y9gj8wg.png)

### Go to Definition, Peek definition

Through the TypeScript language service, VS Code can also provide type definition information in the editor through **Go to Definition** (`kb(editor.action.revealDefinition)`) or **Peek Definition** (`kb(editor.action.peekDefinition)`). Put the cursor over `Application`, right click and select **Peek Definition**. A [[vs.1.7.docs.editor.editingevolved.md#peek]] will open showing the `Application` definition from `ember_application` Type Declaration file.

![react peek definition](/assets/peek-definition-4hvh2cb62osz.png)

Press `kbstyle(Escape)` to close the Peek window.

## Extensions

The VS Code Marketplace has many community created extensions for Ember.js development which add features like code snippets and advanced code suggestions. You can search in the Extensions view (`kb(workbench.view.extensions)`) by typing 'ember'.

![Ember.js extensions](/assets/ember-extensions-0y019vapfia7.png)

## Common questions

### Can I debug Ember client side code with VS Code?

You can use the [[vs.1.7.docs.nodejs.browser-debugging]] for client side debugging. Unfortunately it is difficult to get the configuration correct due to the sourcemaps created by the Ember CLI default transpiler.
