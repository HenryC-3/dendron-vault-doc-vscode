---
id: ki5tilywueh1kcpwbwb6r0o
title: Raspberry Pi
desc: ''
updated: 1660824078462
created: 1660824078462
isDir: false
Order: 5
Area: setup
TOCTitle: Raspberry Pi
ContentId: E059E35A-8AD0-4D4A-9BE1-E23D45D75C1C
PageTitle: Running Visual Studio Code on Raspberry Pi OS
DateApproved: 8/4/2022
MetaDescription: Get Visual Studio Code up and running on Raspberry Pi OS.
---
# Visual Studio Code on Raspberry Pi

You can run Visual Studio Code on [Raspberry Pi](https://www.raspberrypi.org) devices.

[![Raspberry Pi Logo](/assets/rpi-logo-landscape-reg-screen-pvxls4yufldx.png)](https://www.raspberrypi.org)

By downloading and using Visual Studio Code, you agree to the [license terms](https://code.visualstudio.com/license) and [privacy statement](https://go.microsoft.com/fwlink/?LinkID=528096&clcid=0x409).

## Installation

Visual Studio Code is officially distributed via the [Raspberry Pi OS](https://www.raspberrypi.org/software/operating-systems) (previously called Raspbian) APT repository, in both 32-bit and 64-bit variants.

You can install it by running:

```bash
sudo apt update
sudo apt install code
```

### Running VS Code

After installing the VS Code package, you can run VS Code by typing `code` in a terminal or launching it via the **Programming** menu.

![Visual Studio Code under the Programming menu on Raspberry Pi](/assets/vscode-under-programming-z6mxag4kdh2z.jpg)

## Updates

Your Raspberry Pi should handle updating VS Code in the same way as other packages on the system:

```bash
sudo apt update
sudo apt upgrade code
```

You can always check when a new release is available in our [[vs.1.7.updates]] page.

## System requirements

VS Code is supported on these Raspberry Pi models running a 32-bit or 64-bit version of Raspberry Pi OS:

* Raspberry Pi 3 Model B/B+
* Raspberry Pi 4 Model B
* Raspberry Pi 400

While 1 GB of memory (RAM) meets the minimum system requirements, users will benefit from installing VS Code on a Raspberry Pi 4 with more memory.

First-generation Raspberry Pi modules and Raspberry Pi Zero are not supported as they only include an ARMv6 CPU.

### Workaround for poor performance

VS Code on Raspberry Pi 4 may be slow with the default setup. A workaround is to disable hardware (GPU) acceleration in VS Code:

1. Open the VS Code `argv.json` file using the **Preferences: Configure Runtime Arguments** command.
2. Set `"disable-hardware-acceleration": true`.
3. Restart VS Code.

The `"disable-hardware-acceleration": true` runtime argument switch has the effect of passing the `--disable-gpu` command-line argument on VS Code startup.

## Next steps

Once you have installed VS Code, these topics will help you learn more about it:

* [[vs.1.7.docs.setup.additional-components]] - Learn how to install Git, Node.js, TypeScript, and tools like Yeoman.
* [[vs.1.7.docs.getstarted.userinterface]] - A quick orientation to VS Code.
* [[vs.1.7.docs.getstarted.settings]] - Learn how to configure VS Code to your preferences through settings.
