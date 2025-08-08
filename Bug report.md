

**1)Write the bug report using the video**

**Title/Summmary: Sale \-** The old price is displayed instead of the reduced price (the main problem) for the product “Cetka za kosu”

On the "Sale" page, the “Cetka za kosu”product shows the old price above the reduced price instead of showing it crossed out.  
**Description:** On the sales page on the cosmetic shop website, when displaying discounted products, an error was noticed in the display of prices.

**Environment:** Desktop, Windows 11, Chrome Browser ver.13  
**Steps to Reproduce:** 

1\. Open the home page of the cosmetic shop

2\. Click on the "Sale in the main menu" tab

3\. Choose a product

4\. Click on the product

4\. Click the "Add to cart" button

5\. Click on the icon in the upper right corner to enter the basket

6\. Click on the "Checkout" button

7\. Enter your account login information

8\. Click on the "Sign up" button

9\. Enter the delivery information 

10\. Choose a payment method

11\. Click on the "Buy product" button

**Expected Results:** 

The reduced price is shown above and the old price is crossed out below.

**Actual Results:** 

The old price is displayed above the reduced price, the reduced price is crossed out.

**Severity:** Low  
**Priority:** Low

**Title/Summmary:** Special offer \- products have a delay in loading, a white screen appears when scrolling  
**Description:** When scrolling the "Special Offer" page on the cloth shop website, a visual error occurs, the screen turns white while the content is loading, the products become visible after a few seconds. This kind of behavior can have a negative impact on the user experience because it seems as if the site is not working properly.

**Environment:**Desktop, Windows 11, Chrome Browser ver.13

**Steps to Reproduce:** 

1\. Open cloth shop webpage

 2\. Go to the Special offer section 

3\. Scroll down several times and then quickly up

4\. Examine the behavior of the page

**Expected Results:** Products should load gradually and be immediately visible without showing empty (white) space. The visual transition during loading should be continuous and uninterrupted.

**Actual Results:** 

During loading, the screen temporarily turns white while the products are loading.

**Severity:** Medium  
**Priority:** Medium

**2)Detect the bugs and describe them \- Benefiti platform**

**Title/Summmary:** Impossible to add benefits on the demo.benfiti.rs page in the role of HR due to an error regarding the expiration date. The system disables the addition of benefits and displays an error that the “Expiration Type” is not correct, although the field is still present and filled in correctly.  
**Description:** As a user with the HR role, when I try to add a benefit, a message appears that Expiration Type is mandatory, even though that field is on the form and is filled.

**Environment:** Desktop, Windows 11, Chrome Browser ver.13  
**Precondition:** User is logged in with an HR account.

1\) Go to the section “Company Benefits”

2\) Fill in all required fields \- including Expiration Type

3\) Click the “Add Company Benefit Group” button  
4\) Enter a name  
5\) Select a category  
6\) Write a summary  
7\) Add a photo  
8\) Click on the button “Add”   
9\) Inside the created Company benefit group click on the “Add benefit” button  
10\) Enter a name  
11\) Select an Expiration type  
12\) Enter Benefit price in tokens  
13\) Write a summary  
14\) Click on the “Add” button

**Expected Results:**The system should successfully save the new benefit if all fields are filled in correctly, including the Expiration Type, and should be displayed within the Benefit Group for which it was created.

**Actual Results:** A popup window with the message "ValidationError:Expiration required" appears in the upper part of the screen. The user remains on the same page, the benefit is not created.

**Severity:** High  
**Priority:** High
