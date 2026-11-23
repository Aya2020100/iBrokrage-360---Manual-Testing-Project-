# iBrokerage 360 CRM — Manual Testing Portfolio 

iBrokerage 360 is a Canadian-owned, all-in-one, AI-driven real estate software platform designed to help real estate agents, teams, and brokerages manage their 
daily operations from a single portal.  Rather than forcing real estate professionals to juggle multiple disconnected tools, the platform centralizes client relationships,
marketing, transactions, and back-office accounting.

# Project Guide
This one-day project produces a complete manual testing portfolio for the iBrokerage 360 Agent CRM page: requirement analysis notes (Requirement,Assumptions, and Questions),
scenarios, test cases, bug reports,an RTM and a summary report.
The page suits a portfolio because it has a free-trial registration, a login, dropdown menus, a video pop-up and contact details.

# Step 1: Requirement Amalysis 

# A: Requirement 

| ReqID | Feature/ Page | Requirement |
| --- | --- | --- |
|REQ-01|	Header navigation menu (all pages) |	All menu items and dropdowns open the correct pages
| Req-02 | 360 Agent CRM page → Register page | "Your Free Trial" opens the registration page|
| Req-03 | Register page (free trial) | Registration validates required fields and email format| 
| Req-04 | Login page (Account Login)  | "Account Login" opens the login page and rejects invalid credentials |
| Req-05 | 360 Agent CRM page – video section  |"Watch Video" opens a video pop-up that plays and closes  |
| Req-06 | 360 Agent CRM page – contact section  | Contact details (phone, email, map) are correct and clickable |
| Req-07 | Footer (all pages)   |Footer and social media links open the correct public pages  |
| Req-08 | 360 Agent CRM page (desktop, tablet, mobile) | The page displays correctly on desktop, tablet and mobile |
| Req-09 | 360 Agent CRM page – all text | Text is free of spelling and naming errors |

# B: Assumptions 

• No official requirements document is available, so requirements were taken from the website itself.

• Testing was done on the live production site with the public user role only.

• The price ($19.99/month) and the 30-day free trial without a credit card are correct as shown.

• users browse with a current version of a supported browser (Chrome, Edge, Firefox, Safari) with JavaScript and cookies enabled.


# C: Questions for Product taem 

• Is there an account lockout after repeated failed login attempts? If yes, after how many attempts, and for how long?

• Should clicking the phone number start a call on mobile (tel: link)? 

• Which social media accounts are official? The handles look inconsistent (e.g. "iBorkerageDev").

• What are the password rules for registration (length, characters)?

• What happens if a user's session expires mid-form submission?


# Step 2: Test Scenario by Feature & Risk  

I created a file for that part: [View my file] (Test Scenario for iBrokrage.docx) 

# Step 3: Test Cases 

I created a file for that part: [View my file] (Test Scenario for iBrokrage.docx) 



