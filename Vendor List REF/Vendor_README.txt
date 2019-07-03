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

Constraints to follow in the development, using the REFrameWork:
1. TransactionItem datatype should be a QueueItem. The process should recover and retry 2 times in case of errors in navigation between the Invoice Search and Invoices - Search Results pages. One transaction is the action of navigating to the Invoices Search page, searching for the Invoice Number and scraping the values from the resulting one row table.
2. Create a separate workflow file for the Login to ACME. File input arguments: URL ; Username ; Password .
3. Create a separate workflow file for closing ACME.
4. Add the ACME_URL and ACME_Credential to the Excel Config file.
5. Populate InitAllApplications.xaml from the Framework folder with Invoking the Login to ACME and navigation to the Work Items.
6. Populate CloseAllApplications.xaml from the Framework folder with Invoking the Close ACME.
7. Populate KillAllProcesses.xaml from the Framework folder with killing the process used.
8. Populate the Process.xaml file with the following actions: Navigation, Searching for Invoice Number, Scraping, Checking if the values match, Handling the Business Rule Exception.

Important Note: Don't use external file references outside of the project folder (including Orchestrator Assets). Place all the used files within the project folder, zip that folder and upload it to the UiPath Certification Platform.

Zip ALL the used workflow files AND the output Excel file. Then upload the .zip file to the UiPath Certification Platform.

Good luck!




Failed criteria for first attempt:

check separate xaml file for login to acme, with correct definition and functionality. ,
check separate xaml file for close acme, with correct definition and functionality. ,
check config file - config.xlsx for extra configurations for acme_url and acme_credential,
check the initallapplications.xaml file, for correct definition and functionality. ,
check the closeallapplications.xaml file, for correct definition and functionality. ,
check the killallprocesses.xaml file, for correct definition and functionality. ,
check data scraping configuration,
check optimal usage of browser interactions,
check for excel appendrange configuration,
check for correct target selector 1,
check for correct target selector 2,
check for correct usage of items from the transactionitem 1 ,
check usage of transactiondata,
check for correct usage of transactiondata,
check against using hardcoded values 1,
check against using hardcoded values 2,
check using correct city values,
check for correct usage of items from the transactionitem 2
