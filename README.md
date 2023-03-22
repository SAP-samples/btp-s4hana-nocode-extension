[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/btp-s4hana-nocode-extension)](https://api.reuse.software/info/github.com/SAP-samples/btp-s4hana-nocode-extension)
# Use SAP Build Apps to Build Side-by-Side UI Extensions for SAP S/4HANA

The main focus of this mission is to develop a custom UI application, which consumes an OData service from an SAP S/4HANA system.

We will create a simple custom UI application using no-code tool **SAP Build Apps**, push the code to the HTML5 repository and show different options on how to expose this application - as a stand-alone or with the different SAP Build Work Zone environments.


### Start Discovery Center Mission 

- Login to the Discovery Center with your SAP User and select **Start Mission** to start the mission: [SAP Discovery Center mission](https://discovery-center.cloud.sap/missiondetail/4024/4228/)
- Understand the template business case which could be altered to fit to any business demands
- Understand the Solution Architecture of this scenario 
- Choose tab **Project Board** to see the detailed step by step instructions
- Learn the cards in the **Discover** section
  
  <img src="./dcBoard.png" height="500px">
  
## Landscape Setup for SAP BTP and Mock Server

- For the workshop, a SAP BTP subaccount is precreated for you. You will receive the link to SAP BTP subaccount in the workshop.
- You are provided with an user and initial password for the custom Identity & Authentication Tenant which is configured to the subaccount.
- You will login to the SAP BTP cockpit and to the SAP Build Apps using your SAP email address and initial password which was provided during the workshop
  
  <img src="./loginWithCustomIAS.png" height="400px">
  
- A mock server is deployed and already running in the SAP BTP subaccount. This mock server will act like an SAP S/4HANA backend giving the data for [Business Partners API](https://api.sap.com/api/API_BUSINESS_PARTNER/overview)
- A SAP BTP destination is also preconfigured for you with the name **bupa**. Check the destination **bupa** which points to the mock server URL. You will use this destination in the next step when building SAP Build Apps application

  <img src="./bupa.png" height="400px">


## Implementation of an SAP Build Apps Extension Application

Now that the landscape is all setup, let us learn to build an application using SAP Build Apps. You will also learn to preview the application, deploy the application to the SAP BTP-managed HTML5 repository and to integrate the application in the SAP Build Work Zone, standard edition. 

* Develop a simple UI application:
  * [Create a No-Code Application with SAP Build Apps](./create-application/develop/README.md)
  * [Create a Business Partner List Page](./create-application/develop/ListPage/README.md)
  * [Create a Business Partner Details Page](./create-application/develop/DetailsPage/README.md)
  * [Build and Deploy Your SAP Build Apps Application to SAP BTP](./create-application/deploy/README.md)
  * [Integrate the Application with SAP Build Work Zone, standard edition](./create-application/workzone/README.md)

## How to Obtain Support

[Create an issue](https://github.com/SAP-samples/btp-s4hana-nocode-extension/issues) in this repository if you find a bug or have questions about the content.

For additional support, [ask a question in SAP Community](https://answers.sap.com/questions/ask.html).

## Contributing

If you wish to contribute code, offer fixes or improvements, please send a pull request. Due to legal reasons, contributors will be asked to accept a DCO when they create the first pull request to this project. This happens in an automated fashion during the submission process. SAP uses [the standard DCO text of the Linux Foundation](https://developercertificate.org/).

## License

Copyright (c) 2022 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSE) file.
