---
title: Microsoft Power Platform CLI application command group| Microsoft Docs
description: "Describes commands and parameters for the Microsoft Power Platform CLI application command group."
keywords: "pac cli"
ms.subservice: developer
author: kkanakas
ms.author: kartikka
ms.date: 10/13/2022
ms.reviewer: jdaly
ms.topic: reference
contributors: 
 - JimDaly
---
<!-- 
Do not edit this file. 
This file is generated by a program and any changes will be overwritten when this topic is re-generated.
Use the include files to add additional content to this topic.
-->
# pac application

Commands for listing and installing available Dataverse applications from AppSource

[!INCLUDE [application-intro](includes/application-intro.md)]

## Commands

|Command|Description|
|---------|---------|
|[pac application install](#pac-application-install)|Installs Dataverse application to given environment|
|[pac application list](#pac-application-list)|List available Dataverse applications from AppSource|


## pac application install

Installs Dataverse application to given environment

[!INCLUDE [application-install-intro](includes/application-install-intro.md)]


### Optional Parameters

#### `--application-list` `-al`

Location of the JSON file with list of the Dataverse applications from AppSource to be installed

#### `--application-name` `-an`

Unique name of the application that will be installed to target environment

#### `--environment` `-env`

List available Dataverse applications for given environment (by id or url); if not specified, list all applications in the tenant

#### `--environment-id` `-id`

**Deprecated**: Use `--environment` instead.
[!INCLUDE [application-install-remarks](includes/application-install-remarks.md)]

## pac application list

List available Dataverse applications from AppSource

[!INCLUDE [application-list-intro](includes/application-list-intro.md)]


### Optional Parameters

#### `--environment` `-env`

List available Dataverse applications for given environment (by id or url); if not specified, list all applications in the tenant

#### `--environment-id` `-id`

**Deprecated**: Use `--environment` instead.
#### `--installState` `-s`

Filter by application install state

Use one of these values:

- `NotInstalled`
- `Installed`
- `All`

#### `--output` `-o`

Location of the JSON file to be created with list of the Dataverse applications from AppSource

[!INCLUDE [application-list-remarks](includes/application-list-remarks.md)]

[!INCLUDE [application-remarks](includes/application-remarks.md)]

### See also

[Microsoft Power Platform CLI Command Groups](index.md)<br />
[Microsoft Power Platform CLI overview](../introduction.md)