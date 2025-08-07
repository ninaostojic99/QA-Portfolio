  
**Fill in the test plan**

**INTRODUCTION:**This test plan describes the entire approach to testing the Sale page on the cosmetic shop website.

**IN SCOPE:** Functional testing of the entire web application was conducted with a focus on:

* Correctness of product display  
    
* Accuracy and format of displayed prices (regular and reduced price)

**OUT OF SCOPE:** 

* Payment systems  
* Performance testing  
* Security testing

**RISKS AND ASSUMPTIONS:** 

* Functionality marked as ready for testing is not fully implemented, which can lead to incorrect results during testing.  
* Testing relies on limited team resources \- testing is performed by an inexperienced practitioner while the QA mentor is present only part of the time.  
    
* The test environment can be unstable, which makes it difficult to reproduce errors  
    
* There is a risk of missing test data, there are not enough discounted items to check the sale  
    
* The limited number of real devices for mobile testing can make it difficult to detect visual functional problems that do not appear on emulators.

**RESOURCE:**

* Testing performed by: 1 QA practitioner, 1 QA mentor.  
* Tools: browser, API tools, bug tracker  
* Access: the team has access to the admin panel and API documentation  
* Data: There are test data, real items, login accounts

**TIMESCALES:**   
1 day: Writing and revising test cases  
2 days: Functional testing  
3 days: Functional testing and writing and formalizing bug reports  
1 day: Retest and verification of fixes  
1 day: Regression testing and final QA review

**ENVIRONMENTS AND TOOLS:**   
Environment test: Staging version of cosmetic shop site, production site  
Tools:   
\-Browsers: Google Chrome, Microsoft Edge, Firefox  
\-DevTools for loading resources and network applications, mobile view  
\-TestRail for managing test cases  
\-Jira for reporting and tracking bugs  
