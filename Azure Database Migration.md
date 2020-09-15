## Azure Database Migration 

# Which tool to use?
I had a local SQLExpress database I created during a Julie Lerhman PS course on EF.Core.  Once I had a local database created for the Model first approach, I wanted to migrate the API and the database to Azure. 
It's been a minute since I worked with Azure, actually pre-GU using the 1.x frameworks/APIs for queue and storage, etc.  The migration tools were new, very new (to me) and I had two choices - (Azure) Data Migration Assistant (DMA) and a SSMS utility for the migration as well.


The DMA tool couldn't figure out where my local server was, or how to connect to this, and I'm taking the wrap for this.  I dropped back into SSMS and used the migration task for the database context menu.  This approach understands the source server, and just needs some extra information for the Azure SQL Db deploy.

