# Getting Started

Welcome to the Getting Started guide!

## Overview

## Hello World

In this guide, we'll walk you through creating a simple "Hello World" service using the Request and Response APIs.

### Setting Up Your Environment

Before we begin, ensure you have the necessary tools installed and your development environment configured.

> just a joke of course - it is available right away at: 

### Creating Your First Service

Let's start by creating a basic "Hello World" service. We'll use the Request API to get the REST method from the incoming requests and the Response API to send a response back to the client.

```javascript
import { request, response } from "sdk/http";

let method = request.getMethod();

response.println(`Hello World! You are using method: ${method}`);
```

## Explore the Tooling

### Overview: Getting Started with Tooling

This overview will guide you through the basics of the various tools and perspectives available within the platform's workbench. Whether you're managing databases, debugging applications, or designing integration flows, this comprehensive set of tools empowers you to streamline your development workflow and maximize productivity.

#### Workbench Basics

- **[Workbench](tooling/workbench/index.md):** The central hub where you perform your development tasks. It provides access to various perspectives and tools tailored to different aspects of application development.

- **[Import Area](tooling/workbench/import.md):** Easily import existing projects or resources into your workspace.

- **[Search Area](tooling/workbench/search.md):** Quickly find files, resources, or symbols within your project.

- **[Properties Area](tooling/workbench/properties.md):** View and edit properties of selected files or resources.

- **[Console View](tooling/workbench/console.md):** Monitor application logs and execute commands directly within the platform.

- **[Code Editor (Monaco)](tooling/workbench/code-editor.md):** Write, edit, and debug code using the powerful Monaco editor, which provides syntax highlighting, auto-completion, and other advanced features.

- **[Problems View](tooling/workbench/problems.md):** Identify and resolve issues in your codebase with real-time error and warning notifications.

- **[Preview View](tooling/workbench/preview.md):** Preview web pages, documents, or other content directly within the platform.

- **[Logs View](tooling/workbench/logs.md):** Monitor system logs and diagnostic information to troubleshoot issues.

- **[Loggers View](tooling/workbench/loggers.md):** Configure logging settings for different components within your application.

#### Git Perspective

- **[Git Projects View](tooling/git/git-projects.md):** Manage Git repositories, clone, pull, push, and share projects seamlessly.

- **[Local Branches View](tooling/git/local-branches.md):** View and manage local branches within your Git repository.

- **[Remote Branches View](tooling/git/remote-branches.md):** Explore and interact with remote branches in your Git repository.

- **[History View](tooling/git/history.md):** Track changes and revisions in your Git repository's history.

- **[Git Staging View](tooling/git/staging.md):** Stage, unstage, and commit changes to your Git repository.

- **[Diff Editor](tooling/git/diff-editor.md):** Compare and merge differences between files or commits.

#### Databases Perspective

- **[Database Explorer](tooling/databases/explorer.md):** Interact with databases, execute queries, and manage database connections.

- **NoSQL Datasources Support:** Seamlessly work with NoSQL databases and data sources.

- **[SQL Console](tooling/databases/sql.md):** Execute SQL queries and commands directly within the platform.

- **[Result View](tooling/databases/result.md):** View query results and data sets returned from database operations.

- **[Databases View](tooling/databases/databases.md):** Manage database connections, configurations, and schemas.

- **[Transfer View](tooling/databases/transfer.md):** Transfer data between different databases and data sources seamlessly.

- **[Data Export and Import](tooling/databases/export-import.md):** Export and import data between databases using CSV and JSON formats.

#### Debugger Perspective

- **[Debugger Basics](tooling/debugger/index.md#getting-started):** Debug applications using a suite of tools including breakpoints, call stack, variables, and watch expressions.

- **Debugging Tools:** Utilize debugging tools to identify and fix issues in your codebase.

- **[Breakpoints View](tooling/debugger/index.md#2-breakpoints):** Set breakpoints to pause execution at specific points in your code.

- **Call Stack View:** View the call stack to understand the flow of execution.

- **[Variables View](tooling/debugger/index.md#4-variable-inspection):** Inspect and modify variable values during debugging sessions.

#### Documents Perspective

- **[Documents Explorer](tooling/documents/explorer.md):** Manage and organize documents within your project.

- **[Document Preview](tooling/documents/preview.md):** Preview documents and files directly within the platform.

- **[File Upload and Management](tooling/documents/explorer.md#5-drag-and-drop-interaction):** Upload, organize, and manage files and documents within your project.

#### Processes Workspace Perspective

- **[Process Definitions View](tooling/processes/definitions.md):** Explore and manage BPMN process definitions.

- **[Process Instances View](tooling/processes/instances.md):** Monitor and manage running instances of BPMN processes.

- **[Process Context View](tooling/processes/context.md):** View and manage process context data associated with BPMN processes.

- **[Process Viewer](tooling/processes/viewer.md):** Visualize BPMN process diagrams and instances.

- **[Process Inbox](tooling/processes/inbox.md):** Manage user tasks and interactions within BPMN processes.

- **[Dead-Letter Jobs View](tooling/processes/dead-letter-jobs.md):** Monitor and handle failed or erroneous process jobs.

#### Terminal Perspective

- **[Terminal Basics](tooling/terminal/index.md):** Access a command-line interface directly within the platform.

- **[Commands and Shortcuts](tooling/terminal/index.md#2-xtermjs-emulator):** Execute commands, navigate directories, and perform various tasks using terminal commands.

#### Developer Workflows

- **Benefits:** Learn about the benefits of migrating to the codbex platform from SAP HANA XS Classic.

## First Modeled Application

### Overview: Getting Started with MDA

This overview will guide you through the basics of the model driven techniques.

#### Model-Driven Architecture (MDA)

- **[General Overview](tooling/modeling.md#overview):** Understand the concept and benefits of Model-Driven Architecture (MDA) for application development.

- **[Entity Data Modeler (EDM)](tooling/modeling.md#entity-data-modeler-edm):** Design and define domain models using the Entity Data Modeler tool.

## Extend with Event Listener

#### Extensibility in the Platform

- **[Overview](tooling/extensibility.md#overview):** Explore the extensibility features of the platform, including extension points and extensions.

- **[Extension Points](tooling/extensibility.md#extension-points):** Identify and leverage extension points to customize and extend platform functionality.

- **[Extensions](tooling/extensibility.md#extensions):** Develop and deploy extensions to enhance the capabilities of the platform.

## Model Report with a Filter

> TODO

## Schedule a Calculation Job

> TODO

## Synchronize External Data

> TODO

## Add Approval Process

> TODO

## Extend with Custom User Interface

> TODO

## Add Print Template

> TODO

## XS Classic Compatibility

> TODO

#### Compatibility with SAP HANA XS Classic

> TODO

- **Key Features for Compatibility:** Discover the features that make the platform compatible with SAP HANA XS Classic.




