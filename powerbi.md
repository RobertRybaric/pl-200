# Microsoft Power Platform Functional Consultant (PL-200)

## Microsoft Power BI Hands-On Lab

### Overview

In this exercise you will be continuing your work on the model-driven Knowledge Admin app and canvas app.
Additionally, you will be adding Power BI to them. Finally, you will embed a Power App in a Power BI report

### Prerequisites

In order to create a Power BI solution, following prerequisites must be provided:

- Power BI Desktop tool

### Exercise 1

In this exercise, you will edit the form for the Knowledge Assessment entity.There are two places you can edit
this from, either from the Solutions > Entity > Forms list, or via the App Designer. If you are already in App
Designer start, there.

#### Task 1: Install Power BI Desktop / Prepare Power BI service

1. Navigate to https://aka.ms/pbidesktopstore to download and install Power BI Desktop.
2. Navigate to https://app.powerbi.com/ and click **Sign in**.
3. Scroll down the main section of the web page and click **My Workspace** towards the bottom of the screen. Or expand Workspaces in the navigation and select **Create a workspace**.
4. Enter a name for the workspace similar to your environment name **[my initials] Practice**. (Example: AJ Practice.) and click **Save**.

#### Task 2: Connect to the Power Platform Environment

1. Start the Power BI Desktop
2. Sign-in with your cloud credentials and wait until you name will show up in the upper right corner of Power BI Desktop
3. Select Get Data > More > Power Platform > Common Data Service (Legacy)
4. Click **Connect**

    ![Picture 1](images/image001.PNG)

5. Enter the URL of your Power Platform environment

    ![Picture 2](images/image002.PNG)

6. Click **OK**
7. Click **Sign in** and sign in once again with your cloud credentials
8. Click **Connect**
9. In the data selection dialog, select following tables, you have created in your Knowledge Assessment Solution:
    - Knowledge Assessment
    - Knowledge Question
    - Knowledge Test Result
    - SystemUser
10. Click **Load**

    ![Picture 3](images/image003.PNG)

11. Wait until the data is loaded to Power BI
12. In the Power BI Desktop switch to the **Model** view
13. Establish the relationships between the tables as follows:
    - **1:N** relationship between the **Knowledge Assessment** and the **Knowledge Question**
    - **1:N** relationship between the **Knowledge Assessment** and the **Knowledge Test Result**
    - **1:N** relationship between the **User** and the **Knowledge Test Result** (use the field **Owner** for the relationship)
according to the following screenshot:

    ![Picture 4](images/image004.PNG)

#### Task 3: Create Chart and Time Visualizations

1. In the Power BI Desktop switch to the **Report** view
2. In the "Field" pane on the right side locate the field "xxxxx_totalpoints" ("xxxxx" represents you individual field prefix) in the table "xxxxx_KnowledgeTestResult" and rename the field to "Total Points" according to the following screenshot:

    ![Picture 5](images/image005.PNG)

3. In the field list locate the field "fullname" in the table "SystemUser" and rename the field to "Name" according to the following screenshot:

    ![Picture 6](images/image006.PNG)

4. Drag and drop the "Stacked column chart" from the "Visualisations" pane to the working canvas
5. Locate the previously renamed fields "Name" and "Total Points" and drag and drop them to the "Axis" and "Values" parameters of the chart according to the following screenshot:

    ![Picture 7](images/image007.PNG)

6. The result will look like the following example screenshot. The composition of the charts depends on the values in the table "Knowledge Test Result"

    ![Picture 8](images/image008.PNG)

7. While having the visualisation selected, try to change the visualisation type to "Pie chart". The result will look like the following example screenshot:

    ![Picture 9](images/image009.PNG)

