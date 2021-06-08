## What is a CFS integration?

A CFS integration is a "plug and play" piece of code that can be easily deployed into a customer environment and send updates to CFS.

## Deployment Steps

1. Create a block in CFS

   - Once deployed, the block will be updated by the integration with one of 3 statuses:

     - **Pass** - The managed scneario is passing
     - **Fail** - The managed scneario is failing
     - **Misconfigured** - There is an internal error with the cfs integration

1. Create one or more rules in CFS to create a work unit in CFS based off of block status

   - Examples:
     - On three 'Fail' statuses in a row, create a work unit in CFS to handle the managed scenario
     - On three 'Misconfigured' statuses in a row, create a work unit in CFS to investigate the cfs integration

1. Update the CFS protocol as needed for each work unit that would get created

1. Select a manged scenario below to deploy to your environment

## Managed Scenarios

### Url Monitor

Sends requests to a specified url to check site availability

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FCloudFitSoftware%2Fcfs-integrations%2Fmaster%2Ftemplates%2Furl-monitor.json?version=1)

### Stale App Service Monitor

Provide your deployment schedule and this monitor will verify that your app service is recieving deployments on the expected schedule.

NOTE: The container instance system-assigned identity will need be given the **Reader permission role on the app service**

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FCloudFitSoftware%2Fcfs-integrations%2Fmaster%2Ftemplates%2Fstale-app-service-monitor.json?version=1)

### Github Pull Request Monitor

Checks if there are pull requests older than a specified age in Github.

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FCloudFitSoftware%2Fcfs-integrations%2Fmaster%2Ftemplates%2Fgithub-pull-request-monitor.json?version=1)
