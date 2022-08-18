---
id: nr15xak79ks4dlfjmgtljqs
title: Wsl Tutorial
desc: ''
updated: 1660824078461
created: 1660824078461
isDir: false
Order: 9
Area: remote
TOCTitle: WSL Tutorial
PageTitle: Work in Windows Subsystem for Linux with Visual Studio Code
ContentId: 44988826-46b8-498a-b1c9-f821378c2870
MetaDescription: Work in Windows Subsystem for Linux with Visual Studio Code
DateApproved: 8/4/2022
---
# Remote development in WSL

This tutorial walks you through enabling [Windows Subsystem for Linux](https://docs.microsoft.com/windows/wsl/install) (WSL) and running Visual Studio Code in WSL using the [Remote - WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) extension.

## Prerequisites

You need [Visual Studio Code](https://code.visualstudio.com/) installed.

### Install the extension

The Remote - WSL extension enables you to run Visual Studio Code within the Windows Subsystem for Linux (WSL).

> <a class="tutorial-install-extension-btn" href="vscode:extension/ms-vscode-remote.remote-wsl">Install the Remote - WSL extension</a>

![Remote - WSL extension](/assets/remote-wsl-extension-7i5z2czfgmxi.png)

### Prerequisite check

With the Remote - WSL extension installed, you will see a new Status bar item at the far left.

![Remote Status bar item](/assets/remote-status-bar-gafiscqc82i6.png)

The Remote Status bar item can quickly show you in which context VS Code is running (local or remote) and clicking on the item will bring up the Remote - WSL commands.

![Remote - WSL commands](/assets/remote-wsl-commands-bb4uhq2c7vl4.png)

## Enable WSL

Windows Subsystem for Linux (WSL) is an optional feature on Windows 10. You can enable it through the Windows Features dialog or PowerShell.

### Windows Features dialog

In the Windows search bar, type 'features' to bring up the **Turn Windows Features on and off** dialog. Scroll down and check **Windows Subsystem for Linux**.

![Turn Windows features on and off dialog](/assets/windows-features-04jmgi0yygfz.png)

Select **OK** and you will be prompted to restart Windows.

### PowerShell

If you prefer, you can open PowerShell as an Administrator and type:

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

After the command runs, you will be prompted to restart Windows.

![PowerShell prompt to restart](/assets/powershell-output-di6d0852d64o.png)

### Check WSL

After restarting Windows, you can check that you have WSL enabled by opening a Command Prompt and typing 'wsl'.

![WSL check](/assets/wsl-check-sdvfx70arthr.png)

WSL is enabled, but you haven't installed a Linux distribution yet.

## Install a Linux distro

You install Linux distributions for WSL from the Microsoft Store. You can use the store app, or search for a Linux distro in the Windows search bar. Choose the Linux distribution you want to install (for example Ubuntu) and follow the prompts.

![select Ubuntu distro](/assets/select-distro-z37ju2kh2jy4.png)

Select **Install**.

![install Ubuntu](/assets/install-ubuntu-yofhvdeuv08j.png)

And when done, select **Launch** to get started. This will open a Linux terminal and complete the installation.  You'll need to create a user ID and password since you are setting up a full Linux instance. You are now running Linux on Windows.

![Linux terminal](/assets/linux-terminal-4fdnb7f34tnv.png)

## Python development

If you don't have Python already installed, run the following commands to install Python3 and pip, the package manager for Python, into your Linux installation.

```bash
sudo apt update
sudo apt install python3 python3-pip
```

And to verify, run:

```bash
python3 --version
```

Start with the canonical "Hello World" app. Create a new folder called "helloWorld" and then add a Python file that will print a message when run:

```bash
mkdir helloWorld && cd helloWorld
echo 'print("hello from python on ubuntu on windows!")' >> hello.py
python3 hello.py
```

In a remote Linux environment (this WSL distro is technically another machine without UI, that just happens to be running locally on your computer), your development tools and experiences are pretty limited.  You can run [Vim](https://stackoverflow.blog/2017/05/23/stack-overflow-helping-one-million-developers-exit-vim/) in the terminal to edit your file, or you can edit the sources on the Windows side through the `\\wsl$` mount:

![\\wsl$ mount](/assets/wsl$-mount-q7totnhrzm3t.png)

The problem with this model is that the Python runtime, pip, or any conda packages for that matter, are not installed on Windows.

![no Python on Windows](/assets/no-python-on-windows-178yy6e1layj.png)

Remember, Python is installed in the Linux distro, which means if you're editing Python files on the Windows side, you can't run or debug them unless you install the same Python development stack on Windows. And that defeats the purpose of having an isolated Linux instance set up with all your Python tools and runtimes!

## Run in WSL

In the WSL terminal, make sure you are in the helloWorld folder, and type in `'code .'` to launch Visual Studio Code. The `'.'` argument tells VS Code to open the current folder.

> **Note:** If this command does not work, you may need to restart your terminal, or you may not have added VS Code to your path when it was installed.

![launch VS Code](/assets/launch-code-2j9u43dueugz.png)

The first thing you'll see is a message about "Installing VS Code Server" (the c7d83e57… number is the version of the VS Code Server that matches the client-side tools you just installed). VS Code is installing a small server on the Linux side that the desktop VS Code will then talk to. That server will then install and host extensions in WSL, so that they run in the context of the tools and frameworks installed in WSL. In other words, your language extensions will run against the tools and frameworks installed in WSL, not against what is installed on the Windows side, as it should for the proper development experience.

The next thing that happens is VS Code will start and open the `helloWorld` folder. You may see a quick notification telling you that VS Code is connecting to WSL, and you may be prompted to allow access to the Node.js-based server.

![installing vscode server](/assets/installing-vscode-server-3az5bahzv1tb.png)

Now, when you hover over `hello.py`, you get the proper Linux path.

![show hello.py Linux path](/assets/show-linux-path-2wbc7obqcpby.png)

### Integrated Terminal

Run **Terminal** > **New Terminal** (`kb(workbench.action.terminal.toggleTerminal)`) to open a new terminal instance.

![new terminal in WSL](/assets/new-terminal-in-wsl-cfqfxc7ftwji.png)

You'll start a new instance of the bash shell in WSL, again from VS Code running on Windows.

**Tip**: In the lower left corner of the Status Bar, you can see that you're connected to your **WSL: Ubuntu** instance.

![Remote - WSL Status bar](/assets/wsl-status-bar-h1ncddfo09a1.png)

## Edit and debug

### Installing the Python extension (and additional tools)

Click on `hello.py` to open it for editing. You will be prompted with an extension recommendation, in this case to install the [Microsoft Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) extension, which will give you rich editing and debugging experiences. Go ahead and select **Install** and reload if prompted.

![Python extension recommendation](/assets/python-extension-recommendation-58sodcdi7bbf.png)

To prove that the extension is installed in WSL, open the Extensions view again (`kb(workbench.view.extensions)`). You will see a section titled **WSL: Ubuntu – Installed**, and you can see any extensions that are installed on the WSL side.

![WSL installed extensions](/assets/wsl-installed-extensions-8lnxy7v1f171.png)

Upon reload, you'll also get prompted telling you that the pylint linter is not installed. Linters are used to show errors and warnings in source code. Go ahead and select **Install**.

![pylint not installed notification](/assets/pylint-not-installed-gn2zme8aayic.png)

Now, when you edit your code, you get rich colorization and completions.

![Python IntelliSense](/assets/python-intellisense-w8e6hvcjz71r.png)

And when you save your file (`kb(workbench.action.files.save)`), you'll get linting errors and warnings on the file.

![pylint error](/assets/pylint-error-s5uvjsdtm7lr.png)

### Debugging

With your tools set up, let's take this one step further. Set a breakpoint on line 1 of hello.py by clicking in the gutter to the left of the line number or by putting the cursor on the line and pressing `kb(editor.debug.action.toggleBreakpoint)`.

![set breakpoint](/assets/set-breakpoint-3a41sc8995qk.png)

Now, press `kb(workbench.action.debug.start)` to run your application. You will be asked how to run the application, and since this is a simple file, just choose **Python File**.

![select debug configuration](/assets/select-debug-config-m1mahtkp06ra.png)

The app will start, and you'll hit the breakpoint. You can inspect variables, create watches, and navigate the call stack.

Press `kb(workbench.action.debug.stepOver)` to step and you'll see the output of the print statement in the debug console.

![VS Code debug view](/assets/debug-view-4zynms2qmvt1.png)

You get the full development experience of Visual Studio Code, using the Linux instance installed in WSL.

If you want to open another folder in WSL, open the **File** menu and choose **Open Folder**. You'll get a minimal file and folder navigator for the Linux file system, not the Windows file system.

![open folder navigator](/assets/open-folder-9x5koruqpekn.png)

If you want to switch back to the Windows, select the **Show Local** option and you'll get the standard Windows File Open dialog.

### Ending your WSL connection

You can end your session in WSL and go back to running VS Code locally with **File** > **Close Remote Connection**.

### Congratulations

Congratulations, you've successfully completed this tutorial!

Next, check out the other Remote Development extensions.

* [Remote - SSH](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh)
* [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

Or get them all by installing the
[Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) Extension Pack.
