# Lab 6: Creating New Environment Template

## Introduction

This lab walks you through the steps to create a new environment template from the previously downloaded PeopleSoft Image

Estimated Lab Time: 10 minutes

### Objectives
The purpose of this lab is to show you how to create a new environment template from a downloaded PeopleSoft Image in order to create a new PeopleSoft Environment.

In this lab, you will:
* Create a new environment template

### Prerequisites
- A PeopleSoft Cloud Manager Instance
- A downloaded PeopleSoft Image

## **STEP 1**: Creating a New Environment Template

1. 	Navigate to Dashboard -> Environment Template.  
  Click Add New Template button. Provide below details and click Next. 

  Field | Value
  ---- | -----
  Name | MYPUM
  Description	| Test a PUM image
  Peoplesoft Image | Don't type anything. Click on search icon and select the downloaded DPK.  For example, in our case it is PEOPLESOFT HCM UPDATE IMAGE 9.2.030 - NATIVE OS

  *NOTE:* Don't type PEOPLESOFT HCM UPDATE IMAGE 9.2.030 in the Peoplesoft Image field. If the DPKs are downloaded, you will be able to see it in the Search Results as shown in 2nd screenshot below. If you can't see it yet, please wait and refresh after a while.

  ![](./images/s2.png "")

  ![](./images/s3.png "")

2. 	On Select Topology page, click on search icon to search for a topology and select the PUM Fulltier topology.

  ![](./images/2.png "")

3. 	Expand the Custom Attributes and select the PUM Fulltier topology and click Edit Custom Attributes. 

  ![](./images/3.png "")

4. 	Expand the Region and Availability Domains section. 

  Number | Resource Type | Input
  --------- | --------------- | -------------------
  1 | Region | us-ashburn-1
  2 | Primary Availability Domain | evQs:US-ASHBURN-AD-3 
  3 | Compartment	| Demo
  4 | Virtual Cloud Network | OCIHOLVCN

  ![](./images/s5.png "")

  Refer to the following for network topology:

    ![](./images/arch.png "")

5. 	Expand Full Tier -> General Settings. Make sure to give Database Operator Id as **PS**. Give a database name **MYPUMDB**. The defaults for many parameters can be changed; optionally, we will keep it as default.

  ![](./images/s7.png "")

6. Click on Subnet Settings and make sure the subnet is cm. 

  ![](./images/cm.png "")

7. Keep the rest of the field as default.

8. 	Click Next to configure zone and role. Set Zone as **Test**. For role, click on Search Criteria and search for **PACL_CAD**. Select the role from **search results**.

  ![](./images/s9.png "")

  Your screen should look like:

    ![](./images/5.png "")

9. 	Click Next.  Review the page and click Submit to save the template. 

  ![](./images/s10.png "")

You may proceed to the next lab.

## Acknowledgements

**Authors** 
* **Authors** - Rich Konopka, Peoplesoft Specialist, Megha Gajbhiye, Cloud Solutions Engineer
* **Contributor** -  Sara Lipowsky, Cloud Engineer
* **Last Updated By/Date** - Sara Lipowsky, Cloud Engineer, November 2020

## Need Help?
Please submit feedback or ask for help using our [LiveLabs Support Forum](https://community.oracle.com/tech/developers/categories/Migrate%20SaaS%20to%20OCI). Please click the **Log In** button and login using your Oracle Account. Click the **Ask A Question** button to the left to start a *New Discussion* or *Ask a Question*.  Please include your workshop name and lab name.  You can also include screenshots and attach files.  Engage directly with the author of the workshop.

If you do not have an Oracle Account, click [here](https://profile.oracle.com/myprofile/account/create-account.jspx) to create one.