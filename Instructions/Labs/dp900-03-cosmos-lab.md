# Explore Azure Cosmos DB

In this exercise, you'll provision an Azure Cosmos DB database in your Azure subscription, and explore the various ways you can use it to store non-relational data.

## Exercise 1 : Explore Azure Cosmos DB

### Task 1 : Create a Cosmos DB account

To use Cosmos DB, you must provision a Cosmos DB account in your Azure subscription. In this exercise, you'll provision a Cosmos DB account that uses the core (SQL) API.

1.  In the Azure portal, select  **+ Create a resource**  at the top left, and search for  _Azure Cosmos DB_. In the results, select  **Azure Cosmos DB**  and select  **Create**.

2.  In the  **Azure Cosmos DB for NoSQL**  tile, select  **Create**.

3.  Enter the following details, and then select  **Review + Create**:
    -   **Subscription**: If you're using a sandbox, select  _Concierge Subscription_. Otherwise, select your Azure subscription.
    -   **Resource group**: If you're using a sandbox, select the existing resource group (which will have a name like  _learn-xxxx..._). Otherwise, select existing resource group **DP-900-Module-3-<inject key="DeploymentID" enableCopy="false"/>**
    -   **Account Name**: **cosmosdb-<inject key="DeploymentID" enableCopy="false"/>**
    -   **Location**: Choose any available location
    -   **Capacity mode**: Provisioned throughput
    -   **Apply Free-Tier Discount**: Select Apply if available
    -   **Limit total account throughput**: Unselected

4.  When the configuration has been validated, select  **Create**.

5.  Wait for deployment to complete. Then go to the deployed resource.

### Task 2 : Create a sample database

*Throughout this procedure, close any tips that are displayed in the portal*.

1. On the page for your new Cosmos DB account, in the pane on the left, select **Data Explorer**.
1. In the **Data Explorer** page, select **Launch quick start**.
1. In the **New container** tab, review the pre-populated settings for the sample database, and then select **OK**.
1. Observe the status in the panel at the bottom of the screen until the **SampleDB** database and its **SampleContainer** container has been created (which may take a minute or so).

### Task 3 : View and create items

1.  In the Data Explorer page, expand the  **SampleDB**  database and the SampleContainer, and select  **Items**  to see a list of items in the container. The items represent people, each with a unique id, a firstname, an age, and other properties.

2.  Select any of the items in the list to see a JSON representation of the item data.

3.  At the top of the page, select  **New Item**  to create a new blank item.

4.  Modify the JSON for the new item as follows, and then select  **Save**.


    ```
    {
        "id": "123",
        "firstname": "Bob",
        "age": 54
    }

    ```
5.  After saving the new item, notice that additional metadata properties are added automatically.

### Task 4  : Query the database

1.  In the  **Data Explorer**  page, select the  **New SQL Query**  icon.

2.  In the SQL Query editor, review the default query (`SELECT * FROM c`) and use the  **Execute Query**  button to run it.

3.  Review the results, which includes the full JSON representation of all items.

4.  Modify the query as follows:

    ```
    SELECT c.id, c.firstname, c.age
    FROM c
    WHERE c.age > 40

    ```

5.  Use the  **Execute Query**  button to run the revised query and review the results, which includes JSON containing the id, firstname, and age fields for person items with an age greater than 40.
    
6.  Close the SQL Query editor, discarding your changes.
    
    You've seen how to create and query JSON entities in a Cosmos DB database by using the data explorer interface in the Azure portal. In a real scenario, an application developer would use one of the many programming language specific software development kits (SDKs) to call the core (SQL) API and work with data in the database.
    
     > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
     > - Click the (...) icon located at the upper right corner of the lab guide section and navigate to the Lab Validation Page.
     > - Hit the Validate button for the corresponding task.If you receive a success message, you can proceed to the next task. 
     > - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
     > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.


