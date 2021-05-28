## Block Statuses

Once deployed, the specified block will be updated every 30 seconds with one of the following statuses:

- **Pass** - The url is returning a successful status
- **Fail** - The url is not returning a successful status
- **Misconfigured** - There is an internal error that is preventing a pass/fail status

## Deployment Steps

1. Create a block in CFS

1. Create one or more rules in CFS to create a work unit in CFS

   - Examples:
     - On three 'Fail' statuses in a row, create a work unit in CFS
     - On three 'Misconfigured' statuses in a row, create a work unit in CFS to fix the block

1. Update the CFS protocol as needed for each work unit that would get created

1. Deploy to your environment using the one-click deployment button:

## Managed Scenarios

# Url Monitor

   - **Block Id** - The id of the block created in step 1
   - **Scenario Name** - LOWERCASE ONLY - Used for naming resources deployed in the environment
   - **Url To Monitor** - The url to send requests to and verify success status

   [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fsam2k13%2Furl-monitor%2Fmaster%2Ftemplate.json)
