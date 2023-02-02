# Prerequisites and Required Systems

This section contains the prerequisites that you have to fulfill before you get started. Make sure that the prerequisites are fulfilled and all required systems are in place.

## Systems and Accounts

* [SAP S/4HANA Cloud](https://www.sap.com/products/erp/s4hana-erp.html) system
* [Global account](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/8ed4a705efa0431b910056c0acdbf377.html?locale=en-US#loioc165d95ee700407eb181770901caec94) in SAP BTP
* Subaccount in SAP BTP with Cloud Foundry environment enabled. Please check in the [SAP AppGyver - Pricing section](https://discovery-center.cloud.sap/serviceCatalog/sap-appgyver) in which SAP BTP regions SAP AppGyver is available.
* [Optional] If you don't have an SAP S/4HANA Cloud system you can run this mission by installing a mock server. For the mock server, you would need 256MB of Cloud Foundry runtime.

## Tools

* [Cloud Foundry command line interface (v7 version or later)](https://github.com/cloudfoundry/cli/wiki/V7-CLI-Installation-Guide).
* [Cloud MTA Build Tool](https://sap.github.io/cloud-mta-build-tool/) - you can install it using Node.js.

     ```cmd
     npm install -g mbt
     ```


## SAP BTP Provider Account

* Enable SAP BTP Cloud Foundry [global account](https://developers.sap.com/tutorials/cp-cf-entitlements-add.html).
* SAP BTP [subaccount](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/8ed4a705efa0431b910056c0acdbf377.html?locale=en-US#loio8d6e3a0fa4ab43e4a421d3ed08128afa)
* SAP BTP space

### Entitlements

The application requires the following [Entitlements and Quotas](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/00aa2c23479d42568b18882b1ca90d79.html?locale=en-US) in the SAP BTP cockpit:

| Service                           | Plan       | Number of Instances |
|-----------------------------------|------------|:-------------------:|
| SAP AppGyver                      | standard   |          1          |
|  SAP Build Work Zone, standard edition | free or standard |    1          |
| Cloud Foundry runtime (optional)  | MEMORY     |          1          |
| Destination service               | lite       |          1          |


