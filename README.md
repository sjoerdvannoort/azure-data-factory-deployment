# azure-data-factory-deployment

This project contains a custom parameters file to [customize the ARM template generation for Azure Data Factory (V2)](https://docs.microsoft.com/en-us/azure/data-factory/continuous-integration-deployment#use-custom-parameters-with-the-resource-manager-template).

Using [this file](CustomParameters/arm-template-parameters-definition.json) wil customize the ARM parameters as follows:
* All pipeline variables will have variables
* Datasets will not have variables
* Added parameters for several linked services properties to support Databricks and Azure Batch.
* Added variables for trigger status and schedule.
