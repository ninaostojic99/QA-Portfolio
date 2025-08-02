  
1\)  
**Test Case 1:** Block a user from their profile page  
**Priority:** Medium  
**Preconditions:**   
The user is logged into their Instagram account, and the user test123 exists and is searchable via the Instagram search bar.

| Steps | Test Steps | Test Data | Expected Results |
| :---: | ----- | ----- | ----- |
| 1\. | Open the Instagram application | / | Instagram application is opened. |
| 2\. | Search for the user test123 using the search bar | “test123” | The user’s profile is displayed in the search suggestions |
| 3\. | Tap on the user’s page  | / | The profile page “test123” is displayed |
| 4\. | Tap on the three-dot menu in the top right corner | / | The three-dot menu is displayed |
| 5\. | Select “Block” button from the menu | / | A confirmation popup window appears  |
| 6\. | Click on the “Block” button in the popup | / | The user is successfully blocked |
| 7\. | Log in as user “test123”  | “test123” | Login successful |
| 8\. | Open the profile of the user who blocked them | / | The profile is not accessible \- content is hidden or profile is not found, indicating the user has been blocked |

2\)  
**Test Case 2:** User can’t login with invalid password  
**Priority:** High  
**Preconditions:**   
The user has a registered account and is on the Instagram login screen, the device has an active internet connection

| Steps | Test Steps | Test Data | Expected Results |
| :---: | ----- | ----- | ----- |
| 1\. | Open the Instagram application | / | Instagram login screen is displayed. |
| 2\. | Enter valid username in the username field | “test” | The username field displays “test” |
| 3\. | Enter invalid password in the password field | “incorrectpass” | The password field displays masked input \*\*\*\*\*\*\*\*\*\*\*\*\* |
| 4\. | Tap on the “Login” button | / | User stays on the login page |

