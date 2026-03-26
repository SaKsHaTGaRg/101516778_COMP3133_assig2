Employee Management System – GraphQL Backend

Course: COMP 3133 – Full Stack Development II
Assignment: Assignment – I
Student ID: 101516778
Repository: COMP3133_101516778_Assignment1

📖 Project Overview

This project is a backend Employee Management System developed using:

Node.js

Express.js

GraphQL (express-graphql)

MongoDB Atlas

JWT Authentication

Cloudinary (Image Upload)

The system allows:

User registration and login

Employee CRUD operations

Image upload to Cloudinary

JWT protected endpoints

Input validation and error handling

🛠️ Technologies Used

Node.js

Express.js

GraphQL

MongoDB Atlas

Mongoose

bcryptjs

jsonwebtoken

Cloudinary

dotenv

express-validator

Postman (API Testing)

📂 Project Structure
src/
 ├── config/
 │    ├── db.js
 │    └── cloudinary.js
 │
 ├── graphql/
 │    ├── typeDefs.js
 │    └── resolvers.js
 │
 ├── middleware/
 │    └── auth.js
 │
 ├── models/
 │    ├── User.js
 │    └── Employee.js
 │
 ├── validation/
 │    └── graphqlValidation.js
 │
 ├── app.js
 └── server.js

⚙️ Environment Variables (.env)
MONGO_URI=your_mongodb_connection_string
PORT=3000

JWT_SECRET=comp3133_secret_key
JWT_EXPIRES_IN=1d

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

🗄️ Database

Database Name:

comp3133_101516778_Assigment1


Collections:

Users Collection

username (Primary Key)

email (Unique)

password (Encrypted)

created_at

updated_at

Employee Collection

first_name

last_name

email (Unique)

gender

designation

salary (>= 1000)

date_of_joining

department

employee_photo (Cloudinary URL)

created_at

updated_at

🔐 Authentication

JWT token generated at Signup/Login

All Employee APIs are protected

Authorization header format:

Authorization: Bearer <token>

📌 GraphQL APIs Implemented
1️⃣ Signup (Mutation)

Creates a new user account.

2️⃣ Login (Query)

Authenticates user and returns JWT token.

3️⃣ Get All Employees (Query)

Returns all employees (JWT required).

4️⃣ Add Employee (Mutation)

Creates new employee and uploads profile picture to Cloudinary.

5️⃣ Search Employee by EID (Query)

Find employee by MongoDB ObjectId.

6️⃣ Update Employee by EID (Mutation)

Updates employee details.

7️⃣ Delete Employee by EID (Mutation)

Deletes employee record.

8️⃣ Search Employee by Designation or Department (Query)

Filters employees by designation or department.

☁️ Cloudinary Integration

Profile pictures are uploaded to Cloudinary.

Stored in folder:

comp3133_employees


Database stores only secure image URL.

🧪 Validation & Error Handling

The application validates:

Required fields

Email format

Password length

Salary minimum value

Gender enum validation

Duplicate email detection

JWT authorization errors

All errors return proper JSON response objects.

🧪 API Testing

All APIs were tested using:

GraphiQL

Postman

Postman Collection is included in submission.

🚀 Running the Project
Install dependencies
npm install

Run development server
npm run dev

Server URL
http://localhost:3000/graphql

📸 Screenshots Included

MongoDB collections

Cloudinary uploads

Signup & Login

All GraphQL operations

Validation error responses

Unauthorized access

Postman collection

🧾 Sample User Credentials
Username: sakshat
Password: password123