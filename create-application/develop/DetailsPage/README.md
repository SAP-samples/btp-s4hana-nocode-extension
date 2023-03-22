## Create a Business Partner Details Page

After you have created the entry page of your application, you will now create a page to show the details of the selected business partner.

### Create a New Page

You will add a new page to your application and add page parameters so you can access data from your application.

1. On the top left section, choose the name of your current page **Home**, which is highlighted in light blue to open the page menu of SAP Build Apps.

2. Choose **ADD NEW PAGE**.

   <img src="./ba_createPage.png">

3. Enter **Details** as **Page name**, and then Select **OK**. Your new page will be created and open.

4. On the Details page, choose the toggle button to switch to **VARIABLES** tab.

5. Choose the **PAGE PARAMETERS** button on the left side of the screen.

6. Choose **ADD PARAMETER**.

7. It creates a new parameter, choose the created parameter to edit.

8. On the right side of the screen, change the **Parameter name** to **businessPartnerId**.

9. Again, choose  **ADD PARAMETER** and create a second parameter.

10. Change **Parameter name** to **businesspartnerName**.

11. Choose **SAVE**.

    <img src="./ba_pageparameters1.png">

12. Switch back to **VIEW** via the toggle button.

### Enable Navigation from Home Page to Details Page

To show the business partner details on the details page, you need to connect the **Home** page and the **Details** page. In this section, you will first create a new navigation logic to pass the page parameter created in the previous step.
On the details page, you will then load the business partner address by passing the business partner id to the **A_BusinessPartnerAddress** entity.

1. On the top left section, choose the name of your current page **Details**, which is highlighted in light blue, to open the **PAGES** menu. 
2. Select **Home** to switch to Home page to create a logic to pass the business partner and business partner full name parameters from Home page to Details page .
3. Select the first row in the list.

4. At the bottom of App Builder where you can see **Add logic to LIST ITEM1**. Choose the arrow to open the logic canvas.

   <img src="./ba_enableNavigation.png" height="400px">

5. In the component menu on the left side, choose **NAVIGATION** &rarr; **Open page** to add a function that opens a new page.

6. Drag and drop it to the Logic canvas.

7. Hover over the **Component tap** and choose the round dot. Connect the dots of the **Component tap** and the **Open page** components. It creates a new connection and sets the logic to open a new page on the event of tapping an item in the list item.

   <img src="./logiccanvas2.png">

8. Choose the **Open page** component.

9. On the right side of the screen, select **PROPERTIES** &rarr; **Parameters** &rarr; **businessPartnerId**.

10. Choose the **X** button. It opens a popup.

    <img src="./openPage.png">

11. Select **Data item in repeat**.

12. Select **current**.

13. Scroll the list and select **BusinessPartner**, and then choose **SAVE**.

    <img src="./ba_pageVariable.png">

14. Repeat the steps 9-13 for to the **businesspartnerName** parameter and select **current.BusinessPartnerFullName**.

    <img src="./openPage02.png">
    
15. Choose **SAVE** to save the changes.

With this step now, you can pass the selected business partner id and name fields from the list to the details page.

### Load Business Partner Address on the Details Page

The detail page receives the Business partner ID from the main page. In this step, the ID is used to get the address of the selected business partner.

1. From the left side of the screen, choose **Home**.

2. Select the **Details** page from there to switch to the Details page.

3. Toggle to the **VARIABLES** tab.

4. Select **DATA VARIABLES** on the left.

5. Choose **ADD DATA VARIABLE**.

6. Select **A_BusinessPartnerAddress** from the list.
   <img src="./ba_detailspage2.png">

7. Choose the **Filter Conditions** button on the right. 

8. A popup opens. Select **Object with properties**.

      <img src="./objectwithproperties.png">

9. Choose **Add Condition**. In the **Property** dropdown, select **Business Partner**.

10. Under **Compared Value**, choose button **ABC**.

   <img src="./propertybinding.png">

11. Select **Data and Variables**.

    <img src="./bindingdatavariables.png">

12. Select **Page parameter**.

    <img src="./bindingpageparameter.png">

13. Select **businesspartnerId** and choose **SAVE**.

    <img src="./bpid.png">

14. Choose the **SAVE** button to save changes to the page.

15. Toggle to the **VIEW** mode now.

Now, your application loads the business partner's address and stores it to the data variable.


### Display the Business Partner Name on the Details Page

Next, you will change the header of the details page, so it displays the current Business Partner.

1. Select the default description on the page and delete it by pressing **X**.

   <img src="./ba_datailspage3.png">

2. Select headline component. On the right side of the screen, choose **ABC** button in **Content** section.

   <img src="./ba_detailspage4.png">

3. Select **Data and Variables**

   <img src="./bindingdatavariables.png">

4. Select **Page parameter**.

   <img src="./bindingpageparameter.png">

5. Select **businessPartnerName** and choose **SAVE**.

<img src="./editbinding.png">



### Display Business Partner Addresses on the Details Page

Next, you will add a list element, which displays the address of the business partner.

1. Drag the **List item** from the **CORE** tab on the left.

   <img src="./ba_detailspage5.png">

2. From the right **PROPERTIES** panel, find **Arrow Visible** section and select **false** from the dropdown.

3. Choose the **Repeat with** button on the left side of the screen.

   <img src="./ba_detailspage6.png">

1. In the popup, select **Data and Variables** &rarr; **Data variable**.

    <img src="./objectdata.png">

5. Select **A_BusinessPartnerAddress1** from the list.

6. Choose **SAVE**.

   <img src="./bpaddress.png" height="400px">

7. On the right side of the screen, choose **ABC** button under **Primary Label**.

8. Select **Data item in repeat**.

9.  Choose **current**.

10. Scroll and select **StreetName**. Choose **SAVE*.

    <img src="./streetname.png" height="400px">

11. On the right side of the screen, Choose **ABC** button under the **Secondary Label**.

12. Select **Data item in repeat**.

    <img src="./secondarylabel.png">

13. Choose **current**.

14. Scroll and select **PostalCode**. Choose **SAVE**.

     <img src="./postalcode.png">

     <img src="./primarylabel.png" height="400px">

15. Choose **SAVE** at the top of page.

Now, that your app is developed, Let's preview the application.

### Preview Your Application

1. Choose **LAUNCH**.

2. Choose **OPEN PREVIEW PORTAL** and choose **Open web preview** button.
   
   <img src="./ba_preview1.png">

3. Select your application and choose **OPEN**.

   <img src="./ba_preview2.png">

4. Choose the list item to see the details page.

The main page should look like:

   ![main page](../images/preview1.png)

The details page should look like:

   <img src="./ba_deatilspagePreview.png">



