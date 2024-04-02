# Build Your App and Install it on a Mobile Device

## Introduction

For apps installed on mobile devices, SAP Build Apps uses SAP Mobile Services for authenticating mobile users with Cloud Identity Services. This allows integration with S4HANA Cloud services via destinations on SAP BTP. In this section, you will use the build service to build an APK file that can be deployed on an Android device for local testing.

* If you want to build and deploy to Google Play, see [Android builds](https://help.sap.com/docs/build-apps/service-guide/android-builds).
* If you want use an iOS device, see [IOS builds](https://help.sap.com/docs/build-apps/service-guide/ios-builds).

## Prerequisites

* A keystore file. [Android builds](https://help.sap.com/docs/build-apps/service-guide/android-builds) explains how to generate one.
* The destination used must have the parameter **MobileEnabled** set to **true**.
* An Android device that you are allowed to install APKs on. If you do not have such a device, it is possible to use an emulator.

## Configure Authentication

1. Choose **AUTH** at the top section of the app builder and check that SAP BTP authentication has been enabled.

    ![Configuration](./images/authentication_01.png)

2. Choose **LAUNCH** at the top section of the app builder.

    ![Configuration](./images/launch_01.png)

3. Choose **Open build service**. 

    ![Configuration](./images/android_configuration_01.png)
4. Under **Web App**, choose **CONFIGURE**.

    ![Configuration](./images/android_configuration_02.png)

5. Upload your keystore file and enter the passwords and alias. Choose **NEXT**.

    ![Configuration](./images/android_configuration_03.png)

6. Choose **APK** and then choose **Next**.

    ![Configuration](./images/android_configuration_04.png)

7. Choose **NEXT**.

    ![Configuration](./images/android_configuration_05.png)

8. Choose **NEXT**.

    ![Configuration](./images/android_configuration_06.png)

9. Choose **Enable SAP Mobile Services**.

    ![Configuration](./images/android_configuration_07.png)

10. Configure the **API Endpoint**, **Organization**, and **Space**.

    ![Configuration](./images/android_configuration_08.png)

11. Choose **Save**.

    ![Configuration](./images/android_configuration_09.png)

12. Choose **Enable SAP Mobile Services**.   

    ![Configuration](./images/android_configuration_10.png)
    ![Configuration](./images/android_configuration_11.png)
    ![Configuration](./images/android_configuration_12.png)

13. When Mobile Services are enable, choose **NEXT**.

## Build

1. Choose **BUILD**.

    ![Build](./images/android_build_01.png)

2. Choose **APk** and **Runtime Version**. Enter the **Version code** and **Version name**. 

    ![Build](./images/android_build_02.png)

3. Choose **BUILD**.

    ![Build](./images/android_build_04.png)

4. Wait until the DOWNLOAD button appears.

    ![Build](./images/android_build_05.png)

5. Choose **DOWNLOAD** and save the APK file to your computer.    

## Install and Run

1. Install the APK on your Android device.

    ![Install](./images/APK_01.png)
    ![Installed](./images/APK_02.png)

2. Start the app.

    ![Start Setup](./images/APK_03.png)

3. Choose **GET STARTED** and follow the instructions. Once you have finished the configuration process, the deployed app should start automatically.

    ![Running](./images/APK_04.png)