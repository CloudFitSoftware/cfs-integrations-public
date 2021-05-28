## What is a CFS integration?

A CFS integration is a "plug and play" piece of code that can be easily deployed into a customer environment and send updates to CFS.

## Deployment Steps

1. Create a block in CFS

   - Once deployed, the block will be updated by the integration with one of 3 statuses:

     - **Pass** - The url is returning a successful status
     - **Fail** - The url is not returning a successful status
     - **Misconfigured** - There is an internal error that is preventing a pass/fail status

1. Create one or more rules in CFS to create a work unit in CFS based off of block status

   - Examples:
     - On three 'Fail' statuses in a row, create a work unit in CFS
     - On three 'Misconfigured' statuses in a row, create a work unit in CFS to fix the block

1. Update the CFS protocol as needed for each work unit that would get created

1. Deploy to your environment using the one-click deployment button:

## Managed Scenarios

### Url Monitor

Sends requests to a specified during a specified second interval to check site availability 

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsam2k13%2Furl-monitor%2Fmaster%2Ftemplate.json)
