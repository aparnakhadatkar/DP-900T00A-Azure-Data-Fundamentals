# Lab 1a: Explore Azure Database for PostgreSQL

In this exercise, you'll provision an Azure Database for PostgreSQL resources in your Azure subscription.

### Exercise 1: Explore Azure Database for PostgreSQL

In this exercise, you'll provision an Azure Database for PostgreSQL resources.

#### Task 1: Provision an Azure Database for PostgreSQL resource
 
1. In the Azure portal, select **&#65291; Create a resource** (1) from the upper left-hand corner and search for **Azure Database for PostgreSQL** (2).  From the marketplace select the **Azure Database for PostgreSQL Flexible Serve** (3).
 
    ![Screenshot of Azure Database for PostgreSQL deployment options](images/dp900-1a-1(1).png)

1. Review the Azure Database for PostgreSQL options that are available, and then in the **Azure Database for PostgreSQL** (1) tile, select **Azure Database for PostgreSQL Flexible server** (2), then **Create** (3).

    ![Screenshot of Azure Database for PostgreSQL deployment options](images/dp900-1a-2(1).png)

1. Enter the following values on the **Create SQL Database** page:
    - **Subscription**: Select your Azure subscription.
    - **Resource group**: Choose the existing resource group **Dp-900-lab01a-<inject key="DeploymentID" enableCopy="false"/>**
    - **Server name**: **postgresql-<inject key="DeploymentID" enableCopy="false"/>**
    - **Region**: Select a region near you.
    - **PostgreSQL version**: Leave unchanged.
    - **Workload type**: Select **Development**.
    - **Compute + storage**: Leave unchanged.
    - **Availability zone**: Leave unchanged.
    - **Enable high availability**: Leave unchanged.
    - **Admin username**: Your name.
    - **Password** and **Confirm password**: A suitably complex password.

1. Select **Next: Networking >**.

1. Under **Firewall rules**, select **&#65291; Add current client IP address**.

1. Select **Review + Create**, and then select **Create** to create your Azure PostgreSQL database.

1. Wait for deployment to complete. Then go to the resource that was deployed, which should look like this:

    ![Screenshot of the Azure portal showing the Azure Database for PostgreSQL page.](images/dp900-1a-3(1-1).png)

1. Review the options for managing your Azure Database for PostgreSQL resource.

    > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
    > - Click the Lab Validation tab located at the upper right corner of the lab guide section and navigate to the Lab Validation Page.
    > - Hit the Validate button for the corresponding task.
    > - If you receive a success message, you can proceed to the next task. If not, carefully read the error message and retry the step, following the instructions in the lab guide.
    > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.

**You have successfully completed the lab.**
