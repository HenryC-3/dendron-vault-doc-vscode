---
id: wzdc1a9k72dm36yu6besfhx
title: Julia
desc: ''
updated: 1660824078453
created: 1660824078453
isDir: false
Order: 13
Area: languages
TOCTitle: Julia
ContentId: d7ec8e7c-de5e-42b3-86df-a48660f1f6e1
PageTitle: Julia in Visual Studio Code
DateApproved: 8/27/2021
MetaDescription: Learn about working with the Julia programming language in Visual Studio Code.
---
# Julia in Visual Studio Code

The [Julia programming language](https://julialang.org) is a high level and dynamic language built for speed and simplicity. Julia is commonly used in areas such as data science, machine learning, scientific computing, but is still a general purpose language that can handle most programming use cases.

The [Julia extension](https://marketplace.visualstudio.com/items?itemName=julialang.language-julia) for Visual Studio Code includes built-in dynamic autocompletion, inline results, plot pane, integrated REPL, variable view, code navigation, and many other advanced language features.

![Julia VS Code overview](/assets/overview-46xhtmoca5ba.png)

Most of these features work out of the box, while some may require basic configuration to get the best experience. This page summarizes the Julia features included in the Julia VS Code extension. For a more in-depth guide on how these features work and can be configured, see the [Julia in VS Code](https://www.julia-vscode.org/docs/stable/) documentation.

## Getting started

1. Install Julia for your platform: [https://julialang.org/downloads](https://julialang.org/downloads).
2. Install VS Code for your platform: [https://code.visualstudio.com/download](https://code.visualstudio.com/download).
3. Open the Julia extension on the [VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=julialang.language-julia) and press **Install**; or manually install by doing the following steps:
    1. Start VS Code.
    2. Inside VS Code, go to the Extensions view by clicking **View** on the top menu bar and then selecting **Extensions**.
    3. In the Extensions view, search for the term "julia" in the Marketplace search box, then select the Julia extension (julialang.language-julia) and select the **Install** button.
    4. Restart VS Code.

If you run into any issues installing the Julia VS Code extension, check out [[vs.1.7.docs.editor.extension-marketplace.md#install-an-extension]], which should help clarify any issues.

![Julia in the VS Code Marketplace](/assets/julia-extension-marketplace-da6gelvtcb0l.png)

## Running code

There are several ways to run Julia code within VS Code. You can run a Julia file (via `kb(workbench.action.debug.run)`, which will run whatever Julia file you have open and active), execute Julia commands via the REPL, or even execute a specific block of code from a file you have open. To learn more about these options, head to [Julia in VS Code - Running Code](https://www.julia-vscode.org/docs/stable/userguide/runningcode/).

## Debugging

You can start debugging by opening the Julia file that you would like to debug. Then, select the **Run and Debug** view on the Activity bar (as shown below):

![Getting started debugging Julia code](/assets/debug1-d5nbvoy58hk3.png)

Next, you can add a breakpoint by clicking to the left of the line number:

![Adding a breakpoint](/assets/debug2-fcbtnox6mz4h.png)

The red dot will not show up until after you have selected the area next to a line number.

After you have a breakpoint added (or any other type of debug configuration), select the **Run and Debug** button on the left. It may take a few seconds for the initial run to begin. You should then see the output of running the code with the debug configuration. In this example, since we added a breakpoint, you will see the following:

![Run and Debug your Julia file](/assets/debug3-5r6r19fzpwp0.png)

Notice that the second print command has yet to execute and there is only text from the first print command in the terminal. You can finish the execution of the program by selecting the **Continue** button:

![Finish the code execution in the debugger](/assets/debug4-95wsgnil0slt.png)

To find out more about debugging Julia code with VS Code, you can read [Julia in VS Code - Debugging](https://www.julia-vscode.org/docs/stable/userguide/debugging/).

## Code completion (IntelliSense)

The Julia VS Code extension comes with code completion thanks to IntelliSense. This feature works out of the box and is useful for experienced and beginner Julia developers alike.

![Code completion with IntelliSense](/assets/code-completion-vscvncezhl1i.gif)

You can learn more in the [[vs.1.7.docs.editor.intellisense]] topic.

## Julia view

By default, on the left side of the window in the Activity bar, you will see the Julia three dots logo as shown below:

![Julia icon in the Activity bar](/assets/julia-tab1-kczag2pp8a1f.png)

If you select the Julia icon, the Julia view will open that displays sections for **Workspace**, **Documentation**, and the **Plot Navigator**. The **Workspace** section displays a collection of source code that is loaded into your active Julia session. By default, it will be blank since you have not yet run any code, but after you run something, you will be able to see the state of the workspace.

![Julia Workspace](/assets/julia-tab2-qi4rdtkk2gbp.png)

The **Documentation** section lets you review details about specific Julia functions without needing to open a separate browser window. You can search the documentation of any Julia package you have loaded into your active session (by doing `using some_package`), but by default, the search bar will only display results from the core Julia documentation.

![Julia Documentation](/assets/julia-tab3-0pw5ytxo7y13.png)

There is also a built-in **Plot Navigator**, which can be very helpful when you are working on projects with visualization components. You can set the plots to render by default in VS Code and then conveniently navigate back and forth through them.

## Next steps

This has been a brief overview showing the Julia extension features within VS Code. For more information, see the details provided in the Julia extension [README](https://github.com/julia-vscode/julia-vscode#julia).

To stay up to date on the latest features/bug fixes for the Julia extension, see the [CHANGELOG](https://github.com/julia-vscode/julia-vscode/blob/master/CHANGELOG.md).

If you have any issues or feature requests, feel free to log them in the Julia extension [GitHub repo](https://github.com/julia-vscode/julia-vscode/issues).

If you'd like to learn more about VS Code, try these topics:

* [[vs.1.7.docs.editor.codebasics]] - A quick introduction to the basics of the VS Code editor.
* [[vs.1.7.docs.editor.extension-marketplace]] - Learn about other extensions are available in the [Marketplace](https://marketplace.visualstudio.com/vscode).
* [[vs.1.7.docs.editor.editingevolved]] - Move quickly through your source code.
