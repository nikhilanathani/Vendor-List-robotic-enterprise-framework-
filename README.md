# Vendor-List-robotic-enterprise-framework-

RPA Certification

Exercise

In this exercise, you will create a UiPath automation that performs the steps below. To achieve this, you will use the REFrameWork as the starting template and follow the UiPath development best practices.

Here are the steps performed by the Robot:


1. log in to https://www.acme-test.com. 

2. on the landing page, dashboard, click or hover over the vendors menu item and then click on search for vendor. 
   click on display all vendors. scrape the data from the whole table displayed. 
   the resulting datatable will be used as the input data for the process. navigate back to the dashboard. 
   
   note: navigation can be achieved in multiple ways by the robot - choose whichever you find best. 

3. for each tax id:
   - navigate to vendors 
   - search page (click or hover over the vendors menu item and then click on search for vendor); 
   - type the tax id into the vendor tax id field; 
   - click on search; 
   - extract the values for the vendor, city and country and compare them with the values from the previously extracted table 
     from the display all vendors page (check for exact match for all fields!); 
   - if the values are not matching, this should be categorized as a business rule exception; 
   - if the country does not belong to the group {""germany"", ""russia"", ""italy""}, 
     this should be categorized as the second business rule exception. 
     we can only process requests from these countries. 
     check the country value extracted after the individual tax id search; 
   - if no business rule exception, append the resulting datatable from each page into an excel worksheet; 
     you shouldn't worry about the headers and format of the output file.

Note: Navigation can be achieved in multiple ways by the robot - choose whichever you find best.
