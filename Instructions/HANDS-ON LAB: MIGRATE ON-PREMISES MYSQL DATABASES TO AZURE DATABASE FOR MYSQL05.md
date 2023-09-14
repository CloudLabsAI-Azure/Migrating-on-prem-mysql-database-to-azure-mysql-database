## Task 01: Set-up a new migration project

1. In the browser search for **portal.azure.com**

1. Enter the credentials and sign up

1. In the azure portal go to resource group.

1. Select the data migration service **service[DID].

1. In the overview click on **+New Migration project**

1. In the **New Migration project window** Enter the details

1. For name Type **Migration-[DID]

1. For source server type choose MySQL from the drop down

1. For Target server type choose **azure database for for MySQL (single or flexible)**

1. For migration activity type choose Online migration.

1. Click on **Create Run Activity**

1. You can see it creates an activity and redirects you to **MySQL to Azure Database for MySQL Online Migration Wizard**.

1. In **MySQL to Azure Database for MySQL Online Migration Wizard** fill out the information as mentioned below

1. In select source tab For server name mention the ip address of the lab vm running in azure.

  >**Note**: Duplicate the current tab and go-to home page. From there go to resource group and navigate to Labvm-[DID].
  >   There you can find the Labvm IP address.

1. For port leave the default **3306**

1. For username type **sqluser** and for password type **Password.1!!**

1. Uncheck the **encrypt connection**

1. Click on **Next Select Target**. It might take a moment to load.

1. On the Target tab fill the below details and Click on Next **select Database** 

    | Setting                          | Action                           |
    | -------------------------------- | -------------------------------- |
    | **Subscription** drop-down list  | Retain the default value.        |
    | **Location**                     | East Us                          |
    | **Resource Group**               | Jumpvm-RG-[DID]                  |
    | **Azuredatabse for mysql server**  | Select Server[DID]             |
    | **Username**                      | azuresqluser                    |
    | **Password**                      | Password.1!!                    |

1. 


  
