  
**1\. Draw and fill in the table for the 2BVA task from the ISTQB mock test**

| EP | min-1 | min | max | max+1 |
| :---- | :---- | :---- | :---- | :---- |
| EP1: ?\<90 |  |  | 90 | 91 |
| EP2: 90 \- 110 | 90 | 91 | 110 | 111 |
| EP3: 110-130 | 110 | 111 | 130 | 131 |
| EP4: ?\>130 | 130 | 131 |  |  |

**1.2. Write which values cover 100% per 2BVA this table**

| EP | min-1 | min | max | max+1 |
| :---- | :---- | :---- | :---- | :---- |
| EP1: t\<=10 |  |  |  10    | 11 |
| EP2: \[11-15\] | 10 | 11 | 15 | 16 |
| EP3: (15-20) | 15 | 16 | 19 | 20 |
| EP4: \[20 to 22\] | 19 | 20 | 22 | 23 |
| EP5: t \> 22 | 22 | 23 |  |  |

| BV | TC |
| :---- | :---- |
| 10 | TC1: 10 |
| 11 | TC2: 11 |
| 15 | TC3: 15 |
| 16 | TC4: 16 |
| 20 | TC5: 20 |
| 21 | TC6: 21 |
| 22 | TC7: 22 |
| 23 | TC8: 23 |

**1.3 Draw a table of 2 point BVA**

| EP | min-1 | min | max | max+1 |
| :---- | :---- | :---- | :---- | :---- |
| EP1:speed\<=50  |  |  | 50 | 51 |
| EP2: (50;55\] | 50 | 51 | 55 | 56 |
| EP3: (55;60\] | 55 | 56 | 60 | 61 |
| EP4:speed\>60 |  60 | 61 |  |  |

**2\.Write 3 test cases for the employee creation form: 

**1\) Happy path (successful creation)**  
**2\) Negative test case (checking for an error) in this form**  
**3\) Adding Tier \- a happy path https://demo.benefiti.rs/\#/settings**

**1)Test Case 1:** Verify adding a new employee with valid input values  
    **Priority:** High  
    **Preconditions:** The user is logged in with an HR account.

| Steps | Test Steps | Test Data | Expected Results |
| :---: | ----- | ----- | ----- |
| 1\. | Click on the Employee section from the sidebar. | / | Employee section is displayed. |
| 2\. | Click on the "+ Add Employee" button. | / | User is redirected to “Add Employee” page. |
| 3\. | Fill in the Name field:  | "Ana" | The "Name" field displays "Ana". The avatar field shows a circle with "A" inside it. |
| 4\. | Fill in the Surname field: | “Petrovic” | The "Surname" field displays "Petrovic". The avatar field shows a circle with "P" inside it. |
| 5\. | Fill in the Email field: | “test@gmail.com” | The "Email" field displays "test@gmail.com".  |
| 6\. | Select Location from the dropdown menu  | “Aleksinac” | The “Location” field displays “Aleksinac” |
| 7\. | Select Tier from the dropdown menu  | “Test” | The “Tier” field displays “Test” |
| 8\. | Click on the button Add | / | Employ is created, the user is redirected from the “Add Employee” page to the “Employees” page and the added employee can be seen in the table of Employees |

**2)Test Case 2:** Verify adding a new employee when data is not inserted  
    **Priority:** High  
    **Preconditions:** The user is logged in with an HR account.

| Steps | Test Steps | Test Data | Expected Results |
| :---: | ----- | ----- | ----- |
| 1\. | Click on the Employee section from the sidebar. | / | Employee section is displayed. |
| 2\. | Click on the "+ Add Employee" button. | / | User is redirected to “Add Employee” page. |
| 3\. | Fill in the Name field:  | " " | The "Name" field displays “ ”  |
| 4\. | Fill in the Surname field: | “ ” | The "Surname" field displays “ ” |
| 5\. | Fill in the Email field: | “ ” | The "Email" field displays " ".  |
| 6\. | Select Location from the dropdown menu  | “ ” | The “Location” field displays “ ” |
| 7\. | Select Tier from the dropdown menu  | “ ” | The “Tier” field displays “ ” |
| 8\. | Click on the button Add | / | Employee is not created |

**3)Test Case 3:** Verify adding a new tier with valid input values  
    **Priority:** High  
    **Preconditions:** The user is logged in with an HR account.

| Steps | Test Steps | Test Data | Expected Results |
| :---: | ----- | ----- | ----- |
| 1\. | Click on the Settings section from the sidebar. | / | Settings section is displayed. |
| 2\. | Click on the "+ Add Tier" button. | / | User is redirected to “Add Tier” popup window. |
| 3\. | Fill in the Name field:  | "Test" | The "Name" field displays "Test".  |
| 4\. | Fill in the \# of tokens field: | “4” | The "\# of tokens" field displays “4”. |
| 5\. | Click on the Add button | “/ | Tier is created, a success message “Tier successfully created”displays on the top of the screen  |

