# Hasura GraphQL Engine on Azure

Click the `Deploy` button below to create a Hasura GraphQL Engine container on
[Azure Container
Instances](https://azure.microsoft.com/en-us/services/container-instances/)
backed by an [Azure Database for
PostgreSQL](https://azure.microsoft.com/en-us/services/postgresql/) Server.

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3a%2f%2fraw.githubusercontent.com%2fhasura%2fgraphql-engine-on-azure%2fmaster%2farm-aci%2fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<!--
<a href="http://armviz.io/#/?load=https%3a%2f%2fraw.githubusercontent.com%2fhasura%2fgraphql-engine-on-azure%2fmaster%2farm-aci%2fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>
-->

## Pre-requisites

- Valid Azure Subscription ([click
  here](https://azure.microsoft.com/en-us/free/) for a free trial).
  
## Instructions

Once you click the button, it will take you to Azure Portal, where you might be
prompted to login first.

A custom deployment screen will show up, enter all required inputs, as shown in
the screenshot.

- **Subscription**: choose an Azure subscription.
- **Resource Group**: choose an existing one or create a new one.
- **Location**: choose a location for the resource group (note: Azure Container
  Instances and Database for PostgreSQL might not be available on all locations.
  [Click
  here](https://azure.microsoft.com/en-us/global-infrastructure/services/?products=postgresql,container-instances&regions=all)
  to check availability.)
- **Name**: type in a unique name for the deployment, this name is used for
  provisioning a DNS label for the container, so it should be globally unique.
- **Postgres Version**: choose a version.
- **Database SKU Tier**: choose the SKU tier for the PostgreSQL service.
- **Database SKU Capacity**: choose the number of cores for the database.
- **Database SKU Size in MB**: choose the storage size for database (in MB).
- **Administrator Login Password**: type in a password for database, minimum 8
  characters, must include lowercase, uppercase and numbers.
- **URL Encoded Admin Password**: if the admin password contains special
  characters (like `#`, `%`, `$` etc.), URL encode them (like `%40` for `@`) and
  enter here. If there are no special characters, just re-type the password.

![Azure Portal screenshot](https://storage.googleapis.com/graphql-engine-cdn.hasura.io/main-repo/img/azure_arm_aci_template.png)

Once all entries are filled, agree to the terms and click the `Purchase` button.

Deployment will start now.

Click on the Notification Bell icon on the header bar and then click on
Deployment in Progress link.

On this screen, you can see progress for various steps in the deployment.

![Azure Portal deployment screen
screenshot](https://storage.googleapis.com/graphql-engine-cdn.hasura.io/main-repo/img/azure_arm_aci_deployment_screen.png)

Once all steps are completed, click on the `Outpus` link on the sidebar.

![Azure Portal deployment output
screenshot](https://storage.googleapis.com/graphql-engine-cdn.hasura.io/main-repo/img/azure_arm_aci_deployment_output.png)

The FQDN and IP address is shown in this screen. Copy the FQDN and paste it into
a browser. It will open up console.

```
http://hasura-graphql-engine.centralindia.azurecontainer.io
```

![Console](https://storage.googleapis.com/graphql-engine-cdn.hasura.io/main-repo/img/azure_arm_aci_console_graphiql.png)

## Next steps

- [Building your schema](https://docs.hasura.io/1.0/graphql/manual/schema/index.html)
- [GraphQL Queries](https://docs.hasura.io/1.0/graphql/manual/queries/index.html)
- [GraphQL Mutations](https://docs.hasura.io/1.0/graphql/manual/mutations/index.html)
- [GraphQL Subscriptions](https://docs.hasura.io/1.0/graphql/manual/subscriptions/index.html)
- [Event Triggers](https://docs.hasura.io/1.0/graphql/manual/event-triggers/index.html)
- [Authentication/Access control](https://docs.hasura.io/1.0/graphql/manual/event-triggers/index.html)
- [Database Migrations](https://docs.hasura.io/1.0/graphql/manual/migrations/index.html)
- [Guides/Tutorials/Resources](https://docs.hasura.io/1.0/graphql/manual/guides/index.html)
