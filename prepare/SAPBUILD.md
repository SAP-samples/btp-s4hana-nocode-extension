# Prerequisites and Required Systems

This section contains the prerequisites that you have to fulfill before you get started. Make sure that the prerequisites are fulfilled and all required systems are in place.

## Systems and Accounts

* You need to have access to a [Global account](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/8ed4a705efa0431b910056c0acdbf377.html?locale=en-US#loioc165d95ee700407eb181770901caec94) on SAP BTP and your user is mapped to the Global Account Adminstrator role collection.
* Please check in the [SAP Build Apps - Pricing section](https://discovery-center.cloud.sap/serviceCatalog/sap-appgyver) in which SAP BTP regions SAP Build Apps is available.
* For running SAP Build Apps the [SAP Cloud Identity Service - Identiy Authentication](https://help.sap.com/docs/IDENTITY_AUTHENTICATION?locale=en-US) is required
* You have 3  backend options to run this tutorial
    -  Option 1: Using a [SAP S/4HANA Cloud](https://www.sap.com/products/erp/s4hana-erp.html) system.
    -  Option 2: Using a [SAP S/4HANA on-premise](https://community.sap.com/topics/s4hana) system.
    -  Option 3: If you don't have an SAP S/4HANA system you can run this mission by installing a mock server. For the mock server you would need to enable the Cloud Foundry environment and 256MB of Cloud Foundry runtime.

## Tools
optional for mock server installation:
* [Cloud Foundry command line interface (v8 version or later)](https://github.com/cloudfoundry/cli/wiki/V8-CLI-Installation-Guide).
* [Cloud MTA Build Tool](https://sap.github.io/cloud-mta-build-tool/) - you can install it using Node.js.

     ```cmd
     npm install -g mbt
     ```


## SAP BTP Provider Account

* SAP BTP [subaccount](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/8ed4a705efa0431b910056c0acdbf377.html?locale=en-US#loio8d6e3a0fa4ab43e4a421d3ed08128afa)
* Enable SAP BTP Cloud Foundry [global account](https://developers.sap.com/tutorials/cp-cf-entitlements-add.html) and Cloud Foundry space - optional for mock server installation

### Entitlements

The application requires the following [Entitlements and Quotas](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/00aa2c23479d42568b18882b1ca90d79.html?locale=en-US) in the SAP BTP cockpit:

| Service                           | Plan       | Number of Instances |
|-----------------------------------|------------|:-------------------:|
| SAP Build Apps                    | free or standard |    1          |
| SAP Build Workzone - standard edition | free or standard |    1          |
| SAP Cloud Identity Service - Identity Authentication  | MEMORY     |          1          |
| Cloud Foundry runtime (optional)  | MEMORY     |          1          |
| Destination service               | lite       |          1          |


