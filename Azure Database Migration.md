## Azure Database Migration 

# Which tool to use?
I had a local SQLExpress database I created during a Julie Lerhman PS course on EF.Core.  Once I had a local database created for the Model first approach, I wanted to migrate the API and the database to Azure. 
It's been a minute since I worked with Azure, actually pre-GU using the 1.x frameworks/APIs for queue and storage, etc.  The migration tools were new, very new (to me) and I had two choices - (Azure) Data Migration Assistant (DMA) and a SSMS utility for the migration as well.


The DMA tool couldn't figure out where my local server was, or how to connect to this, and I'm taking the wrap for this.  I dropped back into SSMS and used the migration task for the database context menu.  This approach understands the source server, and just needs some extra information for the Azure SQL Db deploy.

# Azure Details
The next step in the wizard needs to the Azure *database server*, if you don't have an instance to push to create one, then choose it from your resource group.  The wizard is looking for the Az SQL DB instance - in my case it was already categorized as a database (instance) hosted by the VM when I chose to create an Az SQL Db.

# SQL Authentication
Once you've authenticated with the Az SQL Db instance - and verified your selections on the following page, you'll be presented with a dialog to start the migration.  Fingers crossed... it worked!  Both the schema and the data are visible inside SSMS after a refresh on the database node within SSMS.

# WebAPI Deploy from VS2019 (Enterprise)
Swagger package add-in / missing dependency for Swashbuckle.EntityFramework.Core - SwashBuckle.Entity 
Successfully installed 'Microsoft.Extensions.ApiDescription.Server 3.0.0' to PlutoWebApi
Successfully installed 'Swashbuckle.AspNetCore 5.3.3' to PlutoWebApi
Successfully installed 'Swashbuckle.AspNetCore.SwaggerGen 5.3.3' to PlutoWebApi
Successfully installed 'Swashbuckle.AspNetCore.SwaggerUI 5.3.3' to PlutoWebApi
https://www.thecodebuzz.com/iservicecollection-does-not-contain-a-definition-of-addswaggergen/

# Azure App Service Deploy
APIM - Azure API Management Instance?

# GitHub PAT
Personal access tokens function like ordinary OAuth access tokens. They can be used instead of a password for Git over HTTPS, or can be used to authenticate to the API over Basic Authentication => https://docs.github.com/v3/auth/#basic-authentication 24d9cccc624cceca416667a65efa1c47dfe17093



%APPDATA%\Microsoft\UserSecrets\4b7f6a2c-de7b-4852-bab8-f54d9f9805d9\secrets.json

Key Vault Usage
https://devblogs.microsoft.com/azure-sdk/azure-sdk-release-april-2020/

