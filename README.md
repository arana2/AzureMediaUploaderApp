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

**Steps**
1. Fork sample application repository with GitHub --> https://github.com/Azure-Samples/azure-typescript-e2e-apps/fork

2. Configure dev environment
- IDE: Visual Studio Code
- Extensions: Dev Container (Used to containerize the dev environments)

3. Install dependencies
- Run NPM install in the APP and API folders
- Node Package Manager: a library and registry for JavaScript software packages

4. Create Azure Storage resource with Visual Studio extension
- In Visual Studio Code, navigate to the Azure Extension to create the Azure Storage

5. Configure CORS
- The browser is used to upload the media file and CORS configuration is required to allow cross-origin requests.

6. Restrict Access to the Storage
- Only want authenticated users to access

7. Create upload container
- This container will be used to store the uploaded files.

8. Grant yourself Blob Data access

9. Get Storage resource credentials
- The Storage resource credentials are used in the Azure Functions API app to connect to the Storage resource.

10. Run the API app
- Run the Functions App to make sure it works correctly before deploying it to Azure.

11. Configure and run the client app

12. Commit code changes

13. Deploy static web app to Azure

**Conclusion**
I found working on this project enjoyable as it allowed me to familiarize myself with Visual Studio Code on a Macbook. Through this project, I gained insight into creating a storage container and setting it up for access. A highlight for me was deploying a static web app, enabling direct media file uploads to a blob container. 

However, the most challenging aspect was configuring the Access Keys for the Storage resource credentials. This proved challenging as I had to grasp the process of obtaining both the Azure Account Key and the Azure Storage account connection string.

Reference: https://learn.microsoft.com/en-us/azure/developer/javascript/tutorial/browser-file-upload-azure-storage-blob?tabs=github-codespaces
