---
id: 8k4dlu0faomar0ygfd5j1i7
title: Mac
desc: ''
updated: 1660824078461
created: 1660824078462
isDir: false
Order: 3
Area: setup
TOCTitle: macOS
ContentId: EEADB50A-F5E3-41E9-89DA-35F165196691
PageTitle: Running Visual Studio Code on macOS
DateApproved: 8/4/2022
MetaDescription: Get Visual Studio Code up and running on Mac (macOS).
---
# Visual Studio Code on macOS

## Installation

1. [Download Visual Studio Code](https://go.microsoft.com/fwlink/?LinkID=534106) for macOS.
2. Open the browser's download list and locate the downloaded app or archive.
3. If archive, extract the archive contents. Use double-click for some browsers or select the 'magnifying glass' icon with Safari.
4. Drag `Visual Studio Code.app` to the **Applications** folder, making it available in the macOS Launchpad.
5. Open VS Code from the **Applications** folder, by double clicking the icon.
6. Add VS Code to your Dock by right-clicking on the icon, located in the Dock, to bring up the context menu and choosing **Options**, **Keep in Dock**.

## Launching from the command line

You can also run VS Code from the terminal by typing 'code' after adding it to the path:

* Launch VS Code.
* Open the **Command Palette** (`kbstyle(Cmd+Shift+P)`) and type 'shell command' to find the **Shell Command: Install 'code' command in PATH** command.

![macOS shell commands](/assets/shell-command-eh38cs25gepb.png)

* Restart the terminal for the new `$PATH` value to take effect. You'll be able to type 'code .' in any folder to start editing files in that folder.

>**Note:** If you still have the old `code` alias in your `.bash_profile` (or equivalent) from an early VS Code version, remove it and replace it by executing the **Shell Command: Install 'code' command in PATH** command.

### Alternative manual instructions

Instead of running the command above, you can manually add VS Code to your path,
to do so run the following commands:

```bash
cat << EOF >> ~/.bash_profile
# Add Visual Studio Code (code)
export PATH="\$PATH:/Applications/Visual Studio Code.app/Contents/Resources/app/bin"
EOF
```

Start a new terminal to pick up your `.bash_profile` changes.

**Note**: The leading slash `\` is required to prevent `$PATH` from expanding during the concatenation. Remove the leading slash if you want to run the export command directly in a terminal.

**Note**: Since `zsh` became the default shell in macOS Catalina, run the following commands to add VS Code to your path:

```zsh
cat << EOF >> ~/.zprofile
# Add Visual Studio Code (code)
export PATH="\$PATH:/Applications/Visual Studio Code.app/Contents/Resources/app/bin"
EOF
```

## Touch Bar support

Out of the box VS Code adds actions to navigate in editor history as well as the full Debug tool bar to control the debugger on your Touch Bar:

![macOS Touch Bar](/assets/touchbar-szx4ssybfn88.gif)

## Mojave privacy protections

After upgrading to macOS Mojave version, you may see dialogs saying "Visual Studio Code would like to access your {calendar/contacts/photos}." This is due to the new privacy protections in Mojave and is not specific to VS Code. The same dialogs may be displayed when running other applications as well. The dialog is shown once for each type of personal data and it is fine to choose **Don't Allow** since VS Code does not need access to those folders.

## Updates

VS Code ships monthly [[vs.1.7.updates]] and supports auto-update when a new release is available. If you're prompted by VS Code, accept the newest update and it will get installed (you won't need to do anything else to get the latest bits).

>Note: You can [[vs.1.7.docs.supporting.faq.md#how-do-i-opt-out-of-vs-code-autoupdates]] if you prefer to update VS Code on your own schedule.

## Preferences menu

You can configure VS Code through [[vs.1.7.docs.getstarted.settings]], [[v[[vs.1.7.docs.getstarted.themes]]nd [[vs.1[[vs.1.7.docs.getstarted.keybindings]]able through the **Code** > **Preferences** menu group.

You may see mention of **File** > **Preferences** in documentation, which is the **Preferences** menu group location on Windows and Linux. On a macOS, the **Preferences** menu group is under **Code**, not **File**.

## Next steps

Once you have installed VS Code, these topics will help you learn more about VS Code:

* [[vs.1.7.docs.setup.additional-components]] - Learn how to install Git, Node.js, TypeScript, and tools like Yeoman.
* [[vs.1.7.docs.getstarted.userinterface]] - A quick orientation around VS Code.
* [[vs.1.7.docs.getstarted.settings]] - Learn how to configure VS Code to your preferences settings.

## Common questions

### Why do I see "Visual Studio Code would like access to your calendar."

If you are running macOS Mojave version, you may see dialogs saying "Visual Studio Code would like to access your {calendar/contacts/photos}." This is due to the new privacy protections in Mojave [[vs.1.7.#mojave-privacy-protections]]. It is fine to choose **Don't Allow** since VS Code does not need access to those folders.

### VS Code fails to update

If VS Code doesn't update once it restarts, it might be set under quarantine by macOS. Follow the steps in this [issue](https://github.com/microsoft/vscode/issues/7426#issuecomment-425093469) for resolution.

### Does VS Code run on Mac M1 machines?

Yes, VS Code supports macOS ARM64 builds that can run on Macs with the Apple M1 chip. You can install the Universal build, which includes both Intel and Apple Silicon builds, or one of the platform specific builds.
