# Build and Deploy Your SAP Build Apps Application to SAP BTP

## Introduction

In this section you will build the application that you created using SAP Build Apps, and then deploy it to SAP BTP as an HTML5 application.

**Persona:** Citizen Developer

**Abbreviation:** SAP Business Technology Platform = SAP BTP


## Step-by-Step

### Build

1. In **Application Development** choose **LAUNCH**.

2. Choose **OPEN BUILD SERVICE**.

   ![choose Open Build Service](./images/ba_build_open_build_service.png)

3. Choose **Create Configuration**

   ![New Configuration](./images/createConfiguration.png)

4. Select **SAP Builld Workzone** as a target platform

   ![target platform](./images/deploy-2.png)

5. Give a Name for the configuration e.g. *BusinessPartners* and choose **Create**

   ![configuration](./images/deploy-3.png)

6. Back in the configuration page, choose **...** from your newly build configuration

   ![Open Configuration](./images/deploy-4.png)

7. In the pop-up choose a Build Process Number e.g. *0.0.1* and choose **Build**

   ![Build Process](./images/deploy-5.png)

8. In the Build History you can see your build with the status *Building*

   ![Build History](./images/deploy-6.png)

9. As soon as your build is status *Delivered* click on line to open Build Details

   ![Build Delivered](./images/deploy-7.png)

10. Choose **Deploy** to deploy your application

   ![Deploy App](./images/deploy-8.png)

11. In the pop-ip, choose the API endpoint of your subaccount

> Hint: You can find the API endpoint in the overview section of your  of your subaccount

12. In case you are not logged in yet, choose **Login with BTP**

   ![API Endpoint](./images/deploy-9.png)

13. In the pop-up choose **Sign in the the default identity provider**

   ![Identity Provider](./images/deploy-10.png)

14. Back in the **Deploy to Work Zone** view choose your **Organization** and **Space**

> Hint: You can find the Organization and Space in the overview section of your  of your subaccount

15. Choose **Continue**

   ![Org & Space](./images/deploy-11.png)

16. Your application in now being deployed. This can take up to 5 minutes. As soon as the status is 'Your web build is now live at' you can click on the link to open your app.

   ![Org & Space](./images/deploy-12.png)



### Check Deployment

1. In **SAP BTP Cockpit**, navigate to your subaccount.

2. From the left-side subaccount menu navigate to **HTML5 Applications**.

3. Under **Managed Application Router provided by SAP Build Work Zone, standard edition**, you will find a list of applications.

4. Click the **Application Name** (this will be the build number).

   ![Org & Space](./images/deploy-13.png)

5. Your application opens. Depending on how your subaccount is configured, you might need to choose the IAS and login.

## Summary

You have deployed the application that you developed in SAP Build Apps to SAP BTP as an HTML5 application that can be consumed using a URL.
