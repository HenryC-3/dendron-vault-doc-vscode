---
id: nyz8vu86db0uj0cm29lz6av
title: Overview
desc: ''
updated: 1660824078438
created: 1660824078438
isDir: false
Order: 1
Area: containers
TOCTitle: Overview
ContentId: 4B462667-8915-4BE0-B8D0-EDE51CB2D273
PageTitle: Docker extension for Visual Studio Code
DateApproved: 11/3/2021
MetaDescription: >-
  Tools for developing and debugging with Docker containers, using Visual Studio
  Code.
---
# Docker in Visual Studio Code

The [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) extension makes it easy to build, manage, and deploy containerized applications in Visual Studio Code.

This page provides an overview of the Docker extension capabilities; use the side menu to learn more about topics of interest. If you are just getting started with Docker development, try the [Docker tutorial](https://docs.microsoft.com/visualstudio/docker) first to understand key Docker concepts.

## Installation

[Install Docker](https://docs.docker.com/install/) on your machine and add it to the system path.

On Linux, you should also [enable Docker CLI for the non-root user account](https://docs.docker.com/install/linux/linux-postinstall/#manage-docker-as-a-non-root-user) that will be used to run VS Code.

To install the extension, open the Extensions view (`kb(workbench.view.extensions)`), search for `docker` to filter results and select Docker extension authored by Microsoft.

![Select Docker extension](/assets/installation-extension-search-f0va6nqzvndl.png)

## Editing Docker files

You can get [[vs.1.7.docs.editor.intellisense]] when editing your `Dockerfile` and `docker-compose.yml` files, with completions and syntax help for common commands.

![IntelliSense for Dockerfiles](/assets/dockerfile-intellisense-nh8y0i0xbada.png)

In addition, you can use the Problems panel (`kb(workbench.actions.view.problems)`) to view common errors for `Dockerfile` and `docker-compose.yml` files.

## Generating Docker files

You can add Docker files to your workspace by opening the Command Palette (`kb(workbench.action.showCommands)`) and using **Docker: Add Docker Files to Workspace** command. The command will generate `Dockerfile` and `.dockerignore` files and add them to your workspace. The command will also ask you if you want to add Docker Compose files as well, but this is optional.

The extension can scaffold Docker files for most popular development languages (C#, Node.js, Python, Ruby, Go, and Java) and customizes the generated Docker files accordingly. When these files are created, we also create the necessary artifacts to provide debugging support for Node.js, Python, and .NET (C#).

## Docker Explorer

The Docker extension contributes a Docker Explorer view to VS Code. The Docker Explorer lets you examine and manage Docker assets: containers, images, volumes, networks, and container registries. If the Azure Account extension is installed, you can browse your Azure Container Registries as well.

The right-click menu provides access to commonly used commands for each type of asset.

![Docker Explorer context menu](/assets/docker-view-context-menu-na1i0effjv4k.gif)

You can rearrange the Docker Explorer panes by dragging them up or down with a mouse and use the context menu to hide or show them.

![Customize Docker Explorer](/assets/docker-view-rearrange-dlhc3ugmmpvx.gif)

## Docker commands

Many of the most common Docker commands are built right into the Command Palette:

![Docker commands](/assets/command-palette-360a1derr4v1.png)

You can run Docker commands to manage [images](https://docs.docker.com/engine/reference/commandline/image/), [networks](https://docs.docker.com/engine/reference/commandline/network/), [volumes](https://docs.docker.com/engine/reference/commandline/volume/), [image registries](https://docs.docker.com/engine/reference/commandline/push/), and [Docker Compose](https://docs.docker.com/compose/reference/overview/). In addition, the **Docker: Prune System** command will remove stopped containers, dangling images, and unused networks and volumes.

## Docker Compose

[Docker Compose](https://docs.docker.com/compose/) lets you define and run multi-container applications with Docker. Our [Compose Language Service](https://github.com/microsoft/compose-language-service) in the Docker extension gives you IntelliSense and tab completions when authoring `docker-compose.yml` files. Press `kb(editor.action.triggerSuggest)` to see a list of valid Compose directives.

 ![Docker Compose IntelliSense](/assets/tab-completions-z0daghgraqde.gif)

We also provide tooltips when you hover over a Docker Compose YAML attribute.

 ![Docker Compose Tooltips](/assets/hover-support-mprpee3jm6t3.png)

While `Compose Up` allows you to run all of your services at once, our new feature `Compose Up - Select Services` lets you select any combination of the services you want to run.

  ![Docker Compose Up - Select Subset](/assets/select-subset-6xdu87g19ntc.gif)

Once your `Compose Up` command completes, navigate to the Docker Explorer to view your services as a Compose Group. This allows you to start, stop, and view the logs of each service as a group.

![Docker Compose Groups](/assets/compose-group-qfpm55iaab0e.png)

## Using image registries

You can display the content and push, pull, or delete images from [Azure Container Registry](https://docs.microsoft.com/azure/container-registry/), [Docker Hub](https://hub.docker.com/), [GitLab](https://gitlab.com/), and more:

![Azure Container Registry content](/assets/container-registry-jlcfuzl09xju.png)

An image in an Azure Container Registry can be deployed to Azure App Service directly from VS Code. See [[vs.1.7.docs.containers.app-service]] to get started. For more information about how to authenticate to and work with registries, see [[v[[vs.1.7.docs.containers.quickstart-container-registries]]

## Debugging services running inside a container

You can debug services built using .NET (C#) and Node.js that are running inside a container. The extension offers custom tasks that help with launching a service under the debugger and with attaching the debugger to a running service instance. For more information, see [[vs.1.7.docs.containers.debug-common]] and [[v[[vs.1.7.docs.containers.reference]]

## Azure CLI integration

You can start Azure CLI (command-line interface) in a standalone, Linux-based container with **Docker Images: Run Azure CLI** command. This gives you access to the full Azure CLI command set in an isolated environment. For more information on available commands, see [Get started with Azure CLI](https://docs.microsoft.com/cli/azure/get-started-with-azure-cli?view=azure-cli-latest#sign-in).

## Next steps

Read on to learn more about

- [[vs.1.7.docs.containers.choosing-dev-environment]]
- [[vs.1.7.docs.containers.quickstart-node]]
- [[vs.1.7.docs.containers.quickstart-aspnet-core]]
- [[vs.1.7.docs.containers.debug-common]]
- [Docker application development](https://docs.docker.com/develop)
- [[vs.1.7.docs.containers.troubleshooting]]
