📄 Coding Test — HR Management Application
Time: 3 hours
Goal: Evaluate your ability to build a small but functional full-stack application using Next.js, Prisma, React Hook Form, and Zod.

🎯 Project Overview
You will build a simple HR Management application where two user roles exist:
1. HR
Manage User Information (Create, Update, Delete)
Manage Attendance (Create, Update, Delete)
Manage Payroll
View Performance (read-only)
2. Manager
Manage Performance (Assign tasks + update rating)
View User Information (read-only)
View Attendance (read-only)
View payroll (read-only)
Note: There is no need to implement the Employee flow.

🧩 Functional Requirements
1. Authentication Requirement
You may implement authentication using either of the following:
Option A — NextAuth
Use Credentials Provider
Store users in the provided Prisma database
Restrict routes based on role (HR, Manager)
Option B — Manual Authentication (JWT)
Implement custom sign-in logic
Issue JWT on login
Protect server actions + pages using middleware
Store password hashes (never plain text)
You may choose whichever method you are more comfortable with.
2. User Management (HR only)
A simple CRUD form for user records.
Required Fields:
name
email
phone
password
authToken
address
designation
department
role: hr | manager | employee
joiningDate
salary
contractExpire

3. Performance Module (Manager only)
The manager should be able to:
Add a task to assign an employee
Update completion date
Update performance rating (1–5)
Fields:
employee (relation to User)
title
assignAt
completedAt (optional)
performanceRating (1–5)

4. Attendance Module
HR:
Add attendance
Edit attendance
Delete attendance
Manager:
View only
Fields:
employee
date
checkIn
checkOut

5. Payroll Module (HR only)
Steps to generate payroll:
Click Create Payroll
A modal opens with:
Select User (dropdown)
Select Month (dropdown)
Calculation (read-only):
workingDays = 22
payable = (salary / 22) * attendanceDays
Confirm → save payroll
Required Fields:
payrollFor
payrollMonth
totalAmount
reduceAmount (optional)
createdBy

⚙️ Technical Requirements
Mandatory Technologies
You must use:
Next.js (App Router)
shadcn/ui
React Hook Form
Zod (schema validation)
Prisma ORM
Database: your choice (e.g., PostgreSQL/MongoDB)

🧪 Coding Tasks
✔ Zod Validation (Required)
Every form must:
Use a Zod schema
Display validation errors
Disable the submit button until the form is valid
✔ Proper Button States (Optional)
Disable buttons while submitting
Disable buttons if required fields are empty or invalid
✔ Modal Messages (Optional)
Every modal action (create/update/delete) must show:
A success message, or
An error message
🚀 Setup Instructions
We will provide you with the starter project structure and database schema at:
🔗 https://github.com/username/projectname
Please follow these steps:
1. Clone the repository: git clone https://github.com/username/projectname
2. Install dependencies
npm install
3. Configure environment
DATABASE_URL=’’
more..
4. Run Prisma migrations
npx prisma migrate dev
5. Start the project
npm run dev

📤 What You Must Submit
1️⃣ GitHub Repository
 Push the full project to a public branch (e.g., submission).
 Environment variables, credentials, and the live link must be included in the README.md.
2️⃣ Live Deployment
 Deploy on Vercel / Netlify / Railway and share the live URL.
3️⃣ Login Credentials
 Provide:
HR Account
Manager Account
Example:
HR → hr@example.com / 123456
Manager → manager@example.com / 123456
4️⃣ Submitted Emails
mokhles.xponent@gmail.com
gazinafis.xponent@gmail.com
Note: README.md must contain the env file, login credentials, and live deployment link. GitHub link should be shared with the mentioned email addresses.
📝 Evaluation Criteria
We will evaluate:
Correct use of Next.js App Router
Clean UI using shadcn
Proper Zod validation
Button disabled states implemented correctly
Code structure and readability
