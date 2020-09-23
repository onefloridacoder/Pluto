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

# Git VS Integration, More practice
Seems my Git foo is pretty lame as well.  Years ago it was all command-line interaction, and now the Git-VS integration/extensions can do all of this for us, within the IDE.  In any case, I lost a day's work all with one stash.  The IDE was connected to the remote repo, and after the stash, there was no optin to commit/push to the remote repo.  I returned the IDE the following day, and all the tools outside of VS displayed any stashed objects locally to recover.

I used this to test myself on what I had learned over the previous three days.  I rebuilt all of the missing code by hand, and checked that in.  It helped b/c I wanted a local version of the API and database to interact with as I rev'd to newer versions of the code base.  Once it's checked into Github, I'll hope back into the Azure migration.  In the meantime, I'm directing my focus toward a/the UI.  

# Angular
When I last looked at this UI technology, it was called AngularJS - very popular and well regarded in the community.  Years ago, I understood how it worked, and why it worked like it did, but I didn't actively code any web apps/UIs.  Since then the base product went through many revisions and re-released as Angular sans the "JS" suffix.  

https://angular.io/tutorial
I'm taking a few days to walk/work through the tutorial to build a UI which looks very much like something I can put in front of the API I created prior.  After its built, it'll be a little sketchy for me to deploy this.  The deployment is an unknown space for how this will be hosted in the cloud.  But, I won't have any previous experience like I've had for these other efforts to create confusing collusions in my mind.  Fresh ground to dig into.

Finished the tutorial - it was presented in a way you could build a non-trivial application with what was shared.  While I was going through this, I kept thinking about how we would accomplish these types of constructs 8, 10, 15 years ago.  It would have been miles of code, literally.  This served me well, and I'm planning the UI for the public-facing Azure API UI.  It'll probably be ugly, not a great CSS dev, but it will definitely work, from the cloud.

# Snoopy UI


