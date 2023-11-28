# MERN Stack Web App Deployment on Azure

This repository contains the necessary steps and code to deploy a MERN (MongoDB, Express.js, React, Node.js) web application on Microsoft Azure. Follow the instructions below to set up and deploy your MERN stack web app.

## Prerequisites

- [Azure Account](https://azure.microsoft.com/)
- [Node.js](https://nodejs.org/) installed
- [Git](https://git-scm.com/) installed
- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli) installed

## Step 1: Create Azure Resource Group

```bash
az group create --name YourResourceGroupName --location YourLocation
```

## Step 2: Create App Service Plan

```bash
az appservice plan create --name YourAppServicePlanName --resource-group YourResourceGroupName --sku B1
```

## Step 3: Create App Service / Web App

```bash
az webapp create --name YourWebAppName --plan YourAppServicePlanName --resource-group YourResourceGroupName
```

## Step 4: Create GitHub Repo

Create a new repository on GitHub: [GitHub Repo](https://github.com/your-username/your-repo)

## Step 5: Connect GitHub to Azure

In the Azure Portal, navigate to your Web App -> Deployment Center -> GitHub -> Authorize and select your repository.

## Step 6: Write Script for Production in `server.js`

Add a production-ready script in your server.js file.

```javascript
// Your production server.js code here
```

## Step 7: Change Base URL

Update the base URL in your client-side code to match the Azure URL.

## Step 8: Build Client Static Files

```bash
cd client
npm install
npm run build
```

## Step 9: Push Code to GitHub

```bash
git add .
git commit -m "Deploying to Azure"
git push origin main
```

## Step 10: Set Up Environment Variables in Azure

In the Azure Portal, navigate to your Web App -> Configuration -> Application settings. Add any necessary environment variables.

## Execute Deployment

Refer to the following [video tutorial](https://youtu.be/zMbXMSma5hg?si=4OwKpUx28dDz6E9y) for a step-by-step walkthrough of the deployment process.

[![Watch the video](https://img.youtube.com/vi/zMbXMSma5hg/maxresdefault.jpg)](https://youtu.be/zMbXMSma5hg?si=4OwKpUx28dDz6E9y)

That's it! Your MERN stack web app should now be deployed on Azure. If you encounter any issues, refer to the video tutorial or check the Azure documentation for troubleshooting.
