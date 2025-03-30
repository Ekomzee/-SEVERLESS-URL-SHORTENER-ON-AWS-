SEVERLESS-URL-SHORTENER-ON-AWS

A fully serverless URL shortener built using AWS Lambda, API Gateway, DynamoDB, S3, and CloudFront. This project generates short links, retrieves original URLs, and optimizes performance with caching and edge delivery.

🚀 What This Project Does
🔹 Converts long URLs into short, easy-to-share links.
🔹 Redirects users from short links to their original destinations.
🔹 Uses DynamoDB to store URL mappings.
🔹 CloudFront improves performance by caching popular URLs.
🔹 A user-friendly frontend hosted on S3 for easy URL management.

🏗 How It Works (Simple Explanation)
1️⃣ User enters a long URL on the frontend or via API.
2️⃣ Lambda function generates a short code and saves it in DynamoDB.
3️⃣ When a user clicks the short link, API Gateway calls another Lambda function to fetch the original URL.
4️⃣ The user is redirected to the original website.
5️⃣ CloudFront caches frequently used links to make redirections faster.
6️⃣ The frontend on S3 allows users to create and manage short links easily.

⚙️ AWS Services Used
Service	Purpose
API Gateway	Manages API requests for shortening and redirecting URLs.
AWS Lambda	Handles logic for creating and retrieving short URLs.
DynamoDB	Stores short URLs and their original links.
S3	Hosts the frontend for users to create and manage short links.
CloudFront	Caches and speeds up URL redirections.

📌 Project Setup 
1️⃣ Set Up API Gateway
Create a REST API in Amazon API Gateway.

Add a POST endpoint to generate short URLs.

Add a GET endpoint to handle redirections.

2️⃣ Deploy AWS Lambda Functions
One function for creating short URLs and storing them in DynamoDB.

Another function for retrieving original URLs and redirecting users.

3️⃣ Set Up DynamoDB
Create a table with shortCode as the primary key.

Store short codes mapped to their original URLs.

4️⃣ Configure CloudFront
Distribute API Gateway and S3 frontend via CloudFront for faster access.

5️⃣ Host the Frontend on S3
Upload a static HTML + JavaScript page to an S3 bucket.

Configure S3 bucket policies for public access.

Use CloudFront to serve the frontend globally.

🎨 Frontend Overview
The frontend (hosted on S3) allows users to:
✅ Enter a long URL and get a shortened version.
✅ Copy and share the short link.
✅ Click on a short link to be redirected instantly.

