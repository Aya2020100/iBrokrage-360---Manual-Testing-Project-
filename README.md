# iBrokerage 360 CRM — Manual Testing Portfolio 

iBrokerage 360 is a Canadian-owned, all-in-one, AI-driven real estate software platform designed to help real estate agents, teams, and brokerages manage their 
daily operations from a single portal.  Rather than forcing real estate professionals to juggle multiple disconnected tools, the platform centralizes client relationships,
marketing, transactions, and back-office accounting.

# Project Guide
This one-day project produces a complete manual testing portfolio for the iBrokerage 360 Agent CRM page: requirement analysis notes (Requirement,Assumptions, and Questions),
scenarios, test cases, bug reports,an RTM and a summary report.
The page suits a portfolio because it has a free-trial registration, a login, dropdown menus, a video pop-up and contact details.

# Step 1: Requirement Analysis 

# A: Requirement 

| ReqID | Feature/ Page | Requirement |
| --- | --- | --- |
|REQ-01|	Header navigation menu (all pages) |	All menu items and dropdowns open the correct pages
| Req-02 | 360 Agent CRM page → Register page | "Your Free Trial" opens the registration page|
| Req-03 | Register page (free trial) | Registration validates required fields and email format| 
| Req-04 | Login page (Account Login)  | "Account Login" opens the login page and rejects invalid credentials |
| Req-05 | 360 Agent CRM page – video section  |"Watch Video" opens a video pop-up that plays and closes  |
| Req-06 | 360 Agent CRM page – contact section  | Contact details ( email, map) are correct and clickable |
| Req-07 | Footer (all pages)   |Footer and social media links open the correct public pages  |

# B: Assumptions 

• No official requirements document is available, so requirements were taken from the website itself.

• Testing was done on the live production site with the public user role only.

• users browse with a current version of a supported browser (Chrome, Edge, Firefox, Safari) with JavaScript and cookies enabled.

• The price ($19.99/month) and the 30-day free trial without a credit card are correct as shown.


# C: Questions for Product taem 

• Is there an account lockout after repeated failed login attempts? If yes, after how many attempts, and for how long?

• Should the login page tell users when an email isn't registered? The Register page already reveals registered emails, so is hiding it on Login intentional?"

• Should clicking the phone number start a call on mobile (tel: link)? 

• Which social media accounts are official? The handles look inconsistent (e.g. "iBorkerageDev").

• What are the password rules for registration (length, characters)?

• Are spaces allowed in passwords, and are leading or trailing spaces trimmed?

• What happens if a user's session expires mid-form submission?


# Step 2: Test Scenario by Feature & Risk  

I created a file for that part: [View my file] (Test Scenario for iBrokrage.docx) 

# Step 3: TestCases 

I created a file for that part: [View my file] (TESTCASES FOR LOGIN ACCOUNT AND FREE TRIAL.xlsx) 


# Step 4: Run the Tests 

Execution summary: I ran the manual test cases on the live iBrokerage 360 website on [11/24/2026], using Windows 11 with Chrome and Edge. Testing covered the Login page, the Register flow (including the Setup Your Password rules), Forget Password, header navigation, the 360 Agent CRM page (Free Trial and Account Login buttons, pricing and the promo video), contact details, footer and social links, content, responsive layout, keyboard access, load time and HTTPS. Of [43] test cases, [39] passed, [3] failed and [1] were deferred. I found 3 defects, [1] Major and [2] Minor, and reported each one with steps to reproduce, expected and actual results, severity, priority. Each failed test case is linked to its bug ID.

# Step 5: Bug Report 

# Bug Report 1 

| Field | Content |
| --- | --- |
|Bug ID |	BUG-01 |
| Title | Labels and controls are as per requirements in "Your Free Trial" page      |
| Environment |	Windows 11, Chrome [157.0.8103.80], Edge [158.0.4370.33] |
| URL |	[https://ibrokerage-3609.ibrokerage.app/agent/register] |
|Steps |	1.  Open the 360 Agent CRM page 2. clcik on the "Your Free Trial" 3. Check all field labels, placeholders and buttons |
| Expected result |	All labels and controls match the requirements and have no spelling mistakes |
| Actual result |	1. while clicking on the Search Brokerage Name Not listed? Icon shifts upward and breaks alignment   2.  The promo code field where users enter an alphanumeric discount code does not appear on the screen. The section is completely blank, and no text box or button is visible in 100% browser zoom. |
|Severity |	Major  |
|Priority  |	High  |
|Impact |	The page looks broken and less professional, so a new user signing up for the free trial may trust the product less. The user can still register, so it doesn't block anything. |
|Linked test case |	TC-002 |
|Evidence  |	https://github.com/user-attachments/assets/452463fe-c78c-4b6a-bf80-971b4d5fe804 |


# Bug Report 2 

| Field | Content |
| --- | --- |
|Bug ID |	BUG-02 |
| Title | Verify UI layout, container alignment, and text rendering on the Setup Password screen at 100% browser zoom in Your free trial " page → password setup page . | |
| Environment |	Windows 11, Chrome [157.0.8103.80], Edge [158.0.4370.33] |
| URL |	[https://ibrokerage-3609.ibrokerage.app/agent/register] |
|Steps |	1. Open the 360 Agent CRM page 2. click on the "Your Free Trial" 3. fill all the information for creating account 4. press "Next" 5.  Inspect the Confirm Password input field and placeholder text. 6. Inspect the Accept Our Terms & Conditions checkbox and its surrounding pill border.|
| Expected result |	All UI elements render cleanly at 100% zoom: "Confirm Password" placeholder displays in full without clipping, "Accept Our Terms & Conditions" fits inside its rounded pill border with balanced padding, and password rules align neatly without awkward wrapping. |
| Actual result |	At 100% zoom, "Accept Our Terms & Conditions" wraps onto 3 lines and overflows outside the top and bottom of its pill border, "Confirm Password" placeholder is clipped ("Confirm Passwc"), and password rules wrap awkwardly. (Layout only aligns properly at 75% zoom). |
|Severity |	Minor  |
|Priority  |	low  |
|Impact |	the sign-up page looks less polished, but registration still works. |
|Linked test case |	TC-007 |
|Evidence |	<img width="955" height="883" alt="image" src="https://github.com/user-attachments/assets/e47c2786-24df-439b-a208-5f41b9dea816" />
 |


# Bug Report 3

| Field | Content |
| --- | --- |
|Bug ID |	BUG-03 |
| Title | check if the user is able to login if the unregistered email address is entered    |
| Environment |	Windows 11, Chrome [157.0.8103.80], Edge [158.0.4370.33] |
| URL |	[https://ibrokerage-3609.ibrokerage.app/agent/register] |
|Steps |	1. open the ibrokrage 360 website 2. click on the "Account Login" 3. enter unregistered  e-mail  4. press login  |
| Expected result |	the user cant be login with error message (ex: No account found with this email address. Would you like to create account) |
| Actual result |	no message is apperaed and the user can go to the next page "Password" |
|Severity |	Minor  |
|Priority  |	Meduim  |
|Impact |Users who press Login without entering a password receive no feedback and may think the site is broken. This causes confusion, repeated attempts and support requests, and may make new trial users abandon login, reducing conversions and trust in the product. |
|Linked test case |	TC-0035 |
|Evidence |	<img width="955" height="442" alt="image" src="https://github.com/user-attachments/assets/3e4eeac0-2108-47a7-b2c6-cbb227619049" />|




# Step6: Requirements Traceability Matrix (RTM) 

| ReqID | Feature/ Page | Requirement | Test Case IDs | Executed (YES/NO) | Result  | Bug IDs |
| --- | --- | --- | --- | --- | --- | --- |
| Req-01 | 360 Agent CRM page → Register page | "Your Free Trial" opens the registration page | TC-001 | Yes | Pass | - |
| REQ-02|	Header navigation menu (all pages) |	All menu items and dropdowns open the correct pages | TC-002 | Yes | Fail | BUG-01|
| Req-03 | Register page (free trial) | Registration validates required fields and email format| TC-007 | YES | Pass | - |
| Req-04 | Login page (Account Login)  | "Account Login" opens the login page and rejects invalid credentials | TC-030 | Yes | Pass | - | 
| Req-05 | 360 Agent CRM page – video section  |"Watch Video" opens a video pop-up that plays and closes  | TC-003 |Yes| Pass| - |
| Req-06 | 360 Agent CRM page – contact section  | Contact details ( email, map) are correct and clickable | TC-004 |Yes| Pass | - |
| Req-07 | Footer (all pages)   |Footer and social media links open the correct public pages  | TC-005 & TC-006 | Yes| Pass | - |


# Step 7: Report Summary

• Project: iBrokerage 360 CRM page, manual testing

• Date / environment: [11/24/2026], Windows 11, Chrome [157.0.8103.80], Edge [158.0.4370.33] 

• Scope: navigation, registration, login, video, contact, footer, content, responsive layout

• Out of scope: security, performance, and features inside the CRM after login

| Total | Passed  | Failed | Deferred |
| --- | --- | --- | --- |
| 43 | 39 | 3 | 1 | 

# Step 8: Sourses 

[https://ibrokerage.ca/]  

# Conclusion

Testing the iBrokerage 360 website was a great opportunity to apply manual testing on a real, live product used by real-estate professionals in Canada. I went through the full testing life cycle: analysing requirements, raising questions and assumptions, writing test scenarios and test cases, running them, reporting bugs, and tracing everything back to the requirements.

Scope note: Features inside the CRM after login (such as client management, transactions and documents) were not tested, because full access is limited to licensed Canadian real-estate brokers. Testing focused on the public pages, registration and login.

Independent learning project. Not affiliated with or requested by iBrokerage.
