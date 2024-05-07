# AzureMediaUploaderApp
This web application using the Azure infrastructure to securely upload media to a blob container.

**Project Workflow**

![image](https://github.com/arana2/AzureMediaUploaderApp/assets/38359810/067dd1ef-b2fc-4268-8442-e92986a31857)

1.  The customer connects to the statically generated website. The website is hosted in Azure Static Web Apps.
2.  The customer uses that website, to select a media file to upload. For this project, the front-end framework is Vite React and the file uploaded is an image file.
3.  The website calls the Azure Functions API sas to get a SAS token based on the exact filename of the file to upload. The serverless API uses the Azure Blob Storage SDK to create the SAS token. The API returns the full URL to use to upload the file, which includes the SAS token as the query string. https://YOUR-STORAGE-NAME.blob.core.windows.net/YOUR-CONTAINER/YOUR-FILE-NAME?YOUR-SAS-TOKEN
4.  The front-end website uses the SAS token URL to upload the file directly to Azure Blob Storage.

**Azure Services Used**
- Azure Static Web Apps: Uses the generated SAS token to upload image file to the Azure Blob Storage
- Azure Functions API: Used to generate the SAS token based out of the filename
- Azure Blob Storage: Used to store the uploaded files

Steps

Conclusion This project was enjoyable and provided a learning experience in Azure's Manage Identities and Compliance domain. It did not involve any coding apart from understanding the JSON format.

Reference: [https://github.com/madebygps/projects/blob/main/az-104/onboarder.md](https://learn.microsoft.com/en-us/azure/developer/javascript/tutorial/browser-file-upload-azure-storage-blob?tabs=github-codespaces)
