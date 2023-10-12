# Lab 05: Online Data Migration with Azure DMS: MySQL to Azure Database for MySQL via Azure Portal

## Lab Scenario

In this lab, you'll use the Azure portal to migrate data from a MySQL source server to an Azure Database for MySQL. The steps involve setting up a migration project, configuring source and target servers, starting the migration, and verifying its completion.

## Lab Objectives:

In this lab, you will perform:

+   Create a new migration project for migrating data from MySQL to Azure Database for MySQL.
+   Configure source and target servers for the migration.
+   Initiate the migration process.
+   Verify the completion of the migration.

## Estimated Timing: 30 minutes

### Task 01: Set up a new migration project

1. In the browser search for **portal.azure.com**. Enter the credentials and sign up

1. In the Azure portal go to a resource group. and Select the **Labvm-<inject key="Deployment ID" enableCopy="false"/>**

   ![](Media/edit07.png)

1. On the overview page **copy** the **IP address** in a Notepad. You will use it for later in this lab

   ![](Media/049.png)

1. Go back to Resource group. Select the Azure data migration service **service<inject key="Deployment ID" enableCopy="false"/>**.

   ![](Media/sixteen.png)

1. On the overview click on **+New Migration project**

   ![](Media/Seventeen.png)

1. On the **New Migration project window** Enter the below details and Click on **Create Run Activity(5)**

   - For **Project Name** Type **Migration-<inject key="Deployment ID" enableCopy="false"/> (1)**

   - For **Source server type** choose **MySQL (2)** from the drop-down

   - For **Target server type** choose **Azure Database for MySQL (Single or Flexible) (3)**

   - For **Migration activity type** choose **Online data migration (4)**.

   ![](Media/eighteen.png)

1. It will create an activity and redirect you to **MySQL to Azure Database for MySQL Online Migration Wizard**, and then click on **Next: Select Target**. (It might take a moment to load.)

1. In **MySQL to Azure Database for MySQL Online Migration Wizard** fill out the information as mentioned below, uncheck **encrypt connection**, and click on **Next: Select Target**

    | Setting                          | Action                           |
    | -------------------------------- | -------------------------------- |
    | **Server name**                  | mention the **ip address** of the lab vm which you copied earlier (1) |
    | **Port**                         | **3306(2)** | 
    | **Username**                     | **sqluser (3)**|
    | **Password**                     | **Password.1!! (4)** |

    ![](Media/edit0014.png)

1. On the **Target tab** fill the following details and Click on Next **select Database(7)** 

    | Setting                          | Action                           |
    | -------------------------------- | -------------------------------- |
    | **Subscription(1)** drop-down list  | Retain the default value.        |
    | **Location(2)**                     | Select the region of your resource group                         |
    | **Resource Group(3)**               | Jumpvm-RG-<inject key="Deployment ID" enableCopy="false"/>                  |
    | **Azuredatabse for mysql server(4)**  | Select Server<inject key="Deployment ID" enableCopy="false"/>             |
    | **Username(5)**                      | azuresqluser                    |
    | **Password(6)**                      | **<inject key="DBpasswd"></inject>**                    |

   ![](Media/edit015.png)

1. In the **databases tab** select **Migrate entire servers**, and click on **Review and start migration**

   ![](Media/edit016.png)

1. On the Review page enter the name as **migrate** for the **Activity** and click on **Start migration**

1. You can view the migration process gets started

1. In the initial load you can see the created database has been migrated.

   ![](Media/0054.png)

1. Monitor the migration on the status screen that appears. You can select the refresh icon in the toolbar to retrieve the latest status. Once the status shows completed, you can go back to the server and review the newly migrated database.

   ![](Media/0055.png)

1. To verify Whether changes made in the local server are reflected, go back to Workbench and create a new database by running the following query.

   ```
    CREATE DATABASE onlinedbtwo;

   ```
1. Execute the command and verify the database created in the schemas tab.

   ![](Media/056.png)

1. Once created navigate back to Azure database and refresh the database. you can view the newly created database has been reflected.

   ![](Media/057.png)


## Review

1. In this lab, you performed a data migration from MySQL to Azure Database for MySQL using the Azure portal.

1. The process involved setting up the migration project, configuring source and target servers, and verifying the successful migration.

# You have successfully completed the lab




  
