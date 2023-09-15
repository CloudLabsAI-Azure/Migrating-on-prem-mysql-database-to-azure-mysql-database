# Exercise 01: Azure Private Endpoint Setup for Secure MySQL Database Access

In this lab, you'll create a private endpoint in Azure to securely connect to a MySQL database. This involves configuring the endpoint and connecting it to your database. You'll then use a command prompt to establish a secure connection to the Azure MySQL database. 

## Task 1: Open the Azure portal

1. Search for Microsoft edge in windows start and click on it.

   ![](Media/01.png)

1. Click on continue without using data and continue browsing

1. Search for portal.azure.com  

1. If not Sign-in, then on the **Sign into Microsoft Azure** tab you will see the login screen, in that enter following **Email/Username** and then click on **Next**. 
   * Email/Username: <inject key="AzureUserName"></inject>

   ![](Media/02.png)
   
1. Now enter the following **Password** and click on **Sign in**.
   * Password: <inject key="AzurePassword"></inject>

   ![](Media/03.png)
    
1. If you see the pop-up **Stay Signed in?**, click No.

   ![](Media/04.png)

## Task 2: Create a private Endpoint.

1. On the search bar, search for **private endpoints** and click on it

   ![](Media/001.png)

1. Click on **+Create**

   ![](Media/002.png)

1. leave the subscription as default

1. For the resource group, select **jumpvm-RG-<inject key="DeploymentID" />**

1. For the name type **endpoint-<inject key="DeploymentID" />**

1. Leave the default value for nic card name. and select a region.

1. Click on **Next:resources**

   ![](Media/003.png)

1. Select **Connect to an Azure resource in my directory.** 

1. Leave the default subscription

1. For resource type search for **Microsoft.DBforMySQL/flexibleservers** and click on it.

1. Select the Database in the resource group created prior.

1. Click on **Next:virtualnetwork**

   ![](Media/004.png)

1. Select the existing virtual network and the existing subnet and leave the defaults

1. Click on **Next:DNS**

   ![](Media/005.png)

1. Select yes and select subscription and resource group and click on next tags and again click next.

   ![](Media/006.png)

1. Click on create.

   ![](Media/007.png)

  >**Note**: It might take few minutes for the deployment to complete meanwhile observe the resources which are created with the endpoint.

## Task 3: Connect to azure database.

1. In the Azure Portal, navigate to resource group and select Jumpvm-<inject key="DeploymentID" />

   ![](Media/008.png)

1. Select the created Azure database **server<inject key="DeploymentID" />**

   ![](Media/009.png)

1. On the left menu, click on connect.

   ![](Media/010.png)

1. Check the prerequisites and click on **Add Client IP ( xxxx )**. Wait until it gets updated.

   ![](Media/011.png)

   ![](Media/012.png)

1. After the configuration, Scroll down to **Connect from browser or locally**

1. Copy the command given.

   ```
   mysql -h server1062788.mysql.database.azure.com -u azuresqluser -p

   ```

   ![](Media/013.png)

1. In the system, navigate to start and search for command prompt by typing **cmd** and select.

   ![](Media/014.png)

1. Paste the command you copied earlier. and press enter

1. For password, type **Password.1!!**. click enter

   ![](Media/015.png)

1. You can see the mysql prompt.

     ![](Media/016.png)

## Review

1. In this lab you have Created an Azure Private Endpoint for secure MySQL database access.

1. Configured and connected the endpoint through the Azure Portal.

1. Established a secure connection using a command prompt, enhancing data security and control.

## Proceed to next exercise

  

     
