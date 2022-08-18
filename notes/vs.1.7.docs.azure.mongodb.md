---
id: h64sishf6fzu6wqut20av9u
title: Mongodb
desc: ''
updated: 1660824078436
created: 1660824078436
isDir: false
Order: 5
Area: azure
TOCTitle: MongoDB
PageTitle: Working with MongoDB in Visual Studio Code
ContentId: d1187f99-354f-4798-9c19-e432e4ae8572
MetaDescription: Working with MongoDB in Visual Studio Code
DateApproved: 8/4/2022
---
# Working with MongoDB

Visual Studio Code has great support for working with [MongoDB](https://www.mongodb.com/what-is-mongodb) databases, whether your own instance or in [Azure with MongoDB Atlas](https://www.mongodb.com/cloud/atlas/azure-mongodb?utm_campaign=marketplace&utm_source=&utm_medium=marketplace). With the [MongoDB for VS Code](https://marketplace.visualstudio.com/items?itemName=mongodb.mongodb-vscode) extension, you can create, manage, and query MongoDB databases from within VS Code.

## Install the extension

MongoDB support for VS Code is provided by the [MongoDB for VS Code](https://marketplace.visualstudio.com/items?itemName=mongodb.mongodb-vscode) extension. To install the MongoDB for VS Code extension, open the Extensions view by pressing `kb(workbench.view.extensions)` and search for 'MongoDB' to filter the results. Select the **MongoDB for VS Code** extension.

![Select MongoDB for VS Code](/assets/install-cosmosdb-extension-v52ivq4xibf0.png)

## Connect to MongoDB

Once you've installed the MongoDB for VS Code extension, you'll notice there is a new **MongoDB** Activity Bar view. Select the MongoDB view and you'll see the MongoDB Explorer.

![MongoDB explorer](/assets/cosmosdb-explorer-1llgh9e6flwq.png)

To connect to a MongoDB database, select **Add Connection** and enter the connection details for the database then **Connect**, the default is a local MongoDB server at `mongodb://127.0.0.1:27017`. You can also enter a connection string, click the "connect with a connection string" link and paste the connection string.

![Database Connection setup](/assets/attach-database-account-ikazekw33oda.png)

>**Note**: Make sure your MongoDB server (mongod.exe) is running if you are connecting to a local MongoDB server.

Once attached, you can work with the MongoDB server, managing MongoDB Databases, Collections, and Documents.

![attached MongoDB database](/assets/attached-mongodb-database-sa0k3puyivay.png)

You can expand databases to view their collections with their schema and indexes and you can select individual MongoDB Documents to view their JSON.

![open mongodb document](/assets/open-document-q8ckuvcsaw6j.png)

You can also attach a MongoDB shell to the active connection, simply by right-clicking on the connection itself.

![MongoDB Connection](/assets/connection-29dhlp8a3yvk.png)

>**Note**: Make sure the MongoDB shell (`mongo` or `mongosh`) [is installed](https://docs.mongodb.com/mongodb-shell/install#mdb-shell-install) and is on your path. In the extension's settings, you can choose which shell you are using.

## MongoDB Commands

There are MongoDB specific commands available in the VS Code **Command Palette** (`kb(workbench.action.showCommands)`) as well as through Explorer context menus.

![mongodb commands](/assets/mongodb-commands-as2x65re26os.png)

## Using Playgrounds

One of the most powerful features of the VS Code MongoDB integration is **Mongo Playgrounds**. Playgrounds let you create, run, and save MongoDB commands from a VS Code editor. Create a new playground with the **MongoDB: Create MongoDB Playground** command.

![new mongo Playground](/assets/new-mongo-scrapbook-inasyh6tfm7b.png)

In a playground, you can reference MongoDB entities and commands and you get rich IntelliSense as you type. Playgrounds are useful for prototyping database operations and queries. Execute selected lines in the playground queries with the **MongoDB: Run Selected Lines From Playground** command.

![mongodb Playground](/assets/scrapbook-d1b90czp9118.png)

![Run Playground queries](/assets/run-playground-ytycndone73h.png)

## MongoDB on Azure

You can easily create a MongoDB cluster on Azure for **Free** with [MongoDB Atlas](https://www.mongodb.com/cloud/atlas/signup?utm_campaign=marketplace&utm_source=signup&utm_medium=marketplace).

Choose **Create a New Cluster** from the dashboard and choose **Azure** as the Cloud Provider. Once the cluster is created, connect to using the connection string provided by **MongoDB Atlas**.

![Create Azure Cluster](/assets/create-azure-cluster-70z9y0h8d90e.png)

## Next steps

* [[vs.1.7.docs.azure.extensions]] - The VS Code Marketplace has hundreds of extensions for Azure and the cloud.
* [[vs.1.7.docs.azure.deployment]] - Learn step-by-step how to deploy your application to Azure.
* [[vs.1.7.docs.azure.docker]] - Put your application in a Docker container for easy reuse and deployment.
