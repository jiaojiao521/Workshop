![](images/Picture-Title.png)

# Lab 100 - Creating a Visual Builder Application and Displaying Business Data

Updated: July 16, 2018

## Introduction

This is the first of several labs that are part of the **Oracle Autonomous Visual Builder Cloud Service workshop.** This workshop will walk you through creating applications for web and mobile from the browser using a visual development environment.

You will take on the Persona of **Javascript Developer** during the workshop. You will create the web application and add the associated business data. You will then create the mobile application and link it to the web applications existing business data. During the workshop you will get an overview of Oracle Autonomous Visual Builder Cloud Service and its features.

In this first lab you will create a Visual Builder application and add business data to display.

**_To log issues_**, click here to go to the [github oracle](https://github.com/oracle/learning-library/issues/new) repository issue submission form.

## Objectives

- Begin Creating a Web Application
  - Create application within Visual Builder user interface
  - Add business data for application to display
- Create the Application Pages
  - Create pages for displaying business data
  - Create pages for creating and editing business data

## Required Artifacts

- The following lab requires an Oracle Public Cloud account that will be supplied by your instructor.

# Create an Application in Oracle Autonomous Visual Builder Cloud Service

### **STEP 1**: Login to your Oracle Cloud Account

- From any browser, go to the URL:
  `https://cloud.oracle.com`

- click **Sign In** in the upper right hand corner of the browser and on the next screen enter you Cloud Account Name.

**NOTE:** The **Cloud Account Name, User Name** and **Password** values will be given to you by the instructor or Trial confirmation email.

![](images/100/signIn.png)

![](images/100/signIn2.png)

- **IMPORTANT** - _Under my services, select from the drop down list the correct data center and click on **My Services**. If you are unsure of the data center you should select, and this is an in-person training event, ***ask your instructor*** which **Region** to select from the drop down list. If you received your account through an Oracle Trial, your Trial confirmation email should provide a URL that will pre-select the region for you._

  ![](images/100/index.png)

- Enter your User Name and Password and click **My Services**

  **NOTE:** For this lab you will assume the role of Javascript Developer **_Lisa Jones_**. Although you are assuming the identify of Lisa Jones, you will log into the account using the **username** provided to you by your instructor, given to you by your corporation, or supplied to you as part of an Oracle Trial. As you progress through the workshop, you will remain logged in as a single user, but you will make “logical” changes from Lisa Jones the Javascript Developer to other personas.

  ![](images/100/lisa.png)

  ![](images/100/index.png)

- You will be presented with a Dashboard displaying the various cloud services available to this account.

  ![](images/100/index.png)

- If all your services are not visible, **click** on the **Customize Dashboard**, you can add services to the dashboard by clicking **Show.** For this workshop, you will want to ensure that you are showing at least the **Application Container, Developer and Storage** cloud services. If you do not want to see a specific service, click **Hide**

  ![](images/100/index.png)

### **STEP 2**: Access the Oracle Autonomous Visual Builder Cloud Service

Oracle Autonomous Visual Builder Cloud Service provides an easy way to
create and host web and mobile applications in a secure cloud
environment. An intuitive visual development experience on top of a
complete development and hosting platform accelerates application
creation and provisioning, leveraging an open, standard-based
architecture.

- From the Cloud UI dashboard click on the **Visual Builder** service.

  ![](images/100/dashboardVBCS.png)

- The Service Details page gives you a quick glance of the service status overview.

- Click **Open Service Console** for the Oracle Visual Builder Cloud Service. The Service Console will then list all Visual Applications.

  ![](images/100/openServiceConsole.png)

### **STEP 3**: Create Visual Application

- Click **New** to start the application create wizard.

  ![](images/100/vbcsca_cra_s2.png)

- On Details screen enter the following data and click on **Next**.

  In the Create Application dialog box, enter the following.

  - Application name: Application
  - Description: Tutorial application

  - The Application ID text field is automatically populated as you type based on the Application Name.

    ![](images/100/nameApp.png)

- You now have a new application, in which you can begin building pages and adding data.

  ![](images/100/welcome.png)

# Import Business Data

### **STEP 1**: Import Files containing business data

#### Create Business Objects by Importing the Inventory Data

In this step you are assuming the identity of the Javascript, **_Lisa Jones_**.

![](images/lisa.png)

- First we will import some data for our application to display. Click on the **Business Objects** icon in the left panel to open the "Business Objects" panel and click the "menu" icon next to the plus sign and click "Data Manager" to open the import tool.

  ![](images/100/busObj.png)

* Now we'll import the Inventory data from a file. Click on the **Data Manager** entry in the **Business Object** menu.

  ![](images/100/openDataManager.png)

- Click **Import Business Objects** and use the provided "Inventory.xlsx" file to import the data.

  ![](images/100/importBusObj.png)

- You will see a popup stating that the upload is taking place and it will confirm that the upload finished with a message stating "Upload succeeded." Click **Next**.

  ![](images/100/importingData.png)

- The business objects will be displayed with the option to edit the names, we will be leaving the names as they are and click n**Next**.

  ![](images/100/newBusObj.png)

- The next step will display the fields that will be created and will detect the data types and set them accordingly. You can edit the names and types here but we will be leaving them as they are imported. Click **Finish**.

  ![](images/100/fields.png)

- Once the import is finished, you will receive a message showing the business objects that have been imported.

  ![](images/100/changesApplied.png)

- You should now see the **inventory** and **variant** business objects in the panel on the left.

  ![](images/100/busObjects.png)

- After selecting either business object, you can go to the **Data** tab to verify or edit the data imported.

### **STEP 2 Creating the Web App**:

Now that we have data for our app to display we can build our web app to display and modify that data.

- Click on the **monitor** icon in the left panel to open the web apps panel. Then click on the "+ Web Application" button to create a new web app.

  ![](images/100/webApps.png)

- Name your app "InventoryWebApp" and click **Create**.

  ![](images/100/nameWebApp.png)

- Your applications canvas will open. This is where we will begin adding components to the page. You can expand the drop downs in the left panel to see where this page is in the structure of the app.

  ![](images/100/appStructure.png)

- To begin, we'll add a list to our page to display our added inventory data. scroll down in the components list panel and drag a **List View** onto our page.

  ![](images/100/addList.png)

- To associate our inventory data with the list, in the right panel select **Add Data**. (If you DO NOT see **Add Data** you may need to expand the right panel or click on the **Quick Add** icon in the "List View" panel, highlighted below)

  ![](images/100/addPage.png)

- There are several steps for selecting data for our list:

  - For **Select Endpoint** expand **Business Objects** > **Inventory** and select the **GET /Inventory** entry, then click **Next**.

  ![](images/100/inventoryEndpoint.png)

  - For **Choose Template** we will use the default template which is at the top of the list and then click **Next**.

  ![](images/100/defaultTemplate.png)

  - For our **Fields** we will select data from the **Endpoint Structure** and drag them into the **Fields** boxes. Drag the following items into the listed Field and then click **Next**:
    - "title1": name
    - "title2": variant
    - "value1": quantity
    - "value2": reserved

  ![](images/100/dataFields.png)

- We don't need to define a query for our data, so we can click **Finish**.

- At this point we have an application that will display our data and we can look at the the live app by clicking on the **Play** button in the top right corner.

  ![](images/100/liveView.png)

  - We have created a simple app to display our wine inventory...

  ![](images/100/firstLiveView.png)

Our app is displaying our data but our inventory/reserved counts aren't labeled. Let's add labels so users will know what these numbers mean. To do that we can customize the data displayed in our list view.

- Leave the live view and return to the design view of your app. Select an item in the list so that it is highlighted with a blue border and a **List Item** tag.

  ![](images/100/listItem.png)

- In the detail panel on the right side, select the **General** tab. We can add our label to the data in the fields. We add the label as a quoted string inside the double square brackets. So the data in the "Value1" field will contain the following

  `[["Inventory: " + $current.data.quantity]]`

  and the "Value2" field will have:

  `[["Reserved: " + $current.data.reserved]]`

* Now our app displays a list of the available wines with their inventory count and reserved count.

  ![](images/100/liveCountsLabeled.png)

# Summary

We have now created an application in Autonomous Visual Builder Cloud Service, added our business data. The next lab in the series will guide us through adding update and edit features to allow the app's users to update inventory counts from the app.