# azure-data-factory-deployment

This project contains a custom parameters file to [customize the ARM template generation for Azure Data Factory (V2)](https://docs.microsoft.com/en-us/azure/data-factory/continuous-integration-deployment#use-custom-parameters-with-the-resource-manager-template).

Using [this file](CustomParameters/arm-template-parameters-definition.json) wil customize the ARM parameters as follows:
* All pipeline variables will be parameterized.
* Datasets will not be parameterized.
* Added parameterization for several linked services properties to support Databricks and Azure Batch.
* Added parameterization for trigger status and schedule.

Note that datasets are not parameterized at all. The assumption is that most differences between environments will be in linked services configuration.
If needed, an environment specific value can be stored in a pipeline variable and passed to a dataset parameter.