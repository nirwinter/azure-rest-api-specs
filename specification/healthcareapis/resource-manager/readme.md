# HealthcareApis

> see https://aka.ms/autorest

This is the AutoRest configuration file for HealthcareApis.



---
## Getting Started
To build the SDK for HealthcareApis, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`
---

## Configuration



### Basic Information
These are the global settings for the HANA on Azure API.

``` yaml
title: HealthcareApisManagementClient
description: Azure Healthcare APIs Client
openapi-type: arm
tag: package-2018-08-preview
azure-arm: true
```


### Tag: package-2018-08-preview

These settings apply only when `--tag=package-2018-08-preview` is specified on the command line.

``` yaml $(tag) == 'package-2018-08-preview'
input-file:
- Microsoft.HealthcareApis/preview/2018-08-20-preview/healthcare-apis.json
```

# Code Generation


## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-java
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-js
```

## Python

See configuration in [readme.python.md](./readme.python.md)

## Go

See configuration in [readme.go.md](./readme.go.md)

## Java

These settings apply only when `--java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-libraries-for-java clone>`.

``` yaml $(java)
azure-arm: true
fluent: true
namespace: com.microsoft.azure.management.healthcareapis
license-header: MICROSOFT_MIT_NO_CODEGEN
payload-flattening-threshold: 1
output-folder: $(azure-libraries-for-java-folder)/azure-mgmt-healthcareapis
```

### Java multi-api

``` yaml $(java) && $(multiapi)
batch:
  - tag: package-2018-08-preview
```

### Tag: package-2018-08-preview and java

These settings apply only when `--tag=package-2018-08-preview --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2018-08-preview' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.healthcareapis.v2018_08_20_preview
  output-folder: $(azure-libraries-for-java-folder)/healthcareapis/resource-manager/v2018_08_20_preview
regenerate-manager: true
generate-interface: true
```


