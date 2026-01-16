# Configure End-to-End Communication from SAP BTP to SAP S/4HANA Cloud

## Introduction

In this section, you wil configure the end-to-end communication between the SAP S/4HANA Cloud system and the SAP BTP subaccount so that a UI5 application running in the SAP BTP subaccount can consume an OData service running on the SAP S/4HANA system. Having already configured the SAP S/4HANA Cloud system, all you need to do is define an appropriate destination on SAP BTP. 
You can propagate the user from the SAP BTP custom Identity Provider to SAP S/4HANA system, be sure that the user principal (e.g: email address) is the same in both systems - Custom Identity provider and the SAP S/4HANA system.



## Create a Destination on SAP BTP

1. In **SAP BTP Cockpit**, navigate to your subaccount.

2. From your left-side subaccount menu, navigate to **Connectivity** &rarr; **Destinations**.  Then choose **Create**.

   ![new Destination](./images/destinations_new.png)

3. Then choose **From Scratch** to enter all the details by yourself or you can choose **From File** to import the sample destination file [s4hCloudOauth](./images/s4hanacloudsaml.json).

   ![from scratch](./images/from-scratch.png)

4. Before configuring the **Destination** you will need your SAP S/4HANA system URL. To find this, login to your SAP S/4HANA Cloud system. You can find your S/4HANA Cloud server ID by selecting your **User Icon** > **Settings** > **User Account** > **Server**.

   ![url](./images/prep01.png)
   
   ![url](./images/prep02.png)

5. Enter the following data to the **Destination Details** section:

   * **Name**: a meaningful name, for example: **S4HC_SAMLASSERTION**

   * **Type**: **HTTP**

   * **URL**: Enter the value of the OData URL, for example: **https://myXXXXXX-api.s4hana.ondemand.com/sap/opu/odata/sap/API_BUSINESS_PARTNER**. 

   * **ProxyType**: **Internet**

   * **Authentication**: **SAMLAssertion**

   ![destination details](./images/destination-view-basic.png)

6. Enter the following data to the **SAML Properties** section:

   * **Audience**: **https://myXXXXXX.s4hana.ondemand.com**. This is the URL of your SAP S/4HANA Cloud account (without the -api).

   * **AuthnContextClassRef**: **urn:oasis:names:tc:SAML:2.0:ac:classes:PreviousSession**

   * **Name Id Format**: **urn:oasis:names:tc:SAML:1.1:nameid-format:emailAddress**  

   ![destination SAML details](./images/destination-view-saml.png)

7. Add the following **Additional Properties** by choosing the **New Property** button. If you have imported the sample destination file, the following properties are automatically added:

   | Name | Value |
   | ---- | ----- |
   | **BuildApps.RequiresCsrf** | **true** |
   | **HTML5.DynamicDestination** | **true** |
   | **HTML5.Timeout** | **60000** |
   | **MobileEnabled** | **true** |
   | **WebIDEEnabled** | **true** |
   | **WebIDEUsage** | **odata_gen** |

   ![destination properties](./images/destination-view-properties.png)

8. Check **Use default client trust store**.

9. **Save** your settings.
   
10. Choose **Check Connection**. You should get a success message.
   
   ![check conn](./images/destination-check-connection.png)

## Summary

You have created a destination in the SAP BTP subaccount that can be used by SAP AppGyver to do SSO and user propagation.
