CFSelenium Cross-Browser Converter Ant Script

Currently, CFSelenium test cases created using the Firefox Selenium IDE plugin and then exported in CFML format contain a placeholder for the URL of the site (local or remote) you want to test against, and is set to execute the test against the Firefox browser.
	
This Ant script will make some changes to your initial Firefox test cases, such as inserting the site URL you want to test against and setting an AJAX-friendly execution speed (so any changes made to be page via AJAX have time to occur before the next step of the test).  It will then makes copies of the tests for whichever additional browsers you want to test against and place them in separate folders (one per browser).
	
If any of your tests capture screenshots, this Ant script will adjust the screenshot commands to make sure they work for each supported browser and will ensure that each screenshot file has a unique and incremental name associated with the test so that you can take multiple screenshots during a test and can distinguish them afterwards.  The screenshots will be saved in a screenshots folder within each browser test folder.
	
Once you have the script in place and configured properly, you can create new tests in Selenium IDE, save them to your Firefox test case folder, and run the script to not only make them operational in Firefox but to make useable copies for each browser you want to test (and you can run the script every time you add new tests).