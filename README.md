# Job Application Serverless Web App (AWS)

A fully serverless job application portal using AWS services.

## Tech Stack

* **Frontend:** HTML, CSS, JavaScript (deployed to S3 static website hosting)
* **Backend:** AWS Lambda (Python), API Gateway, DynamoDB, S3

---

## ✨ Features

✅ Applicants can submit their details and upload resumes.
✅ Recruiters can view all applications in a secure portal.
✅ Resumes are stored in S3, application data in DynamoDB.
✅ Fully serverless, low-cost and highly scalable.

---

## 📜 Architecture

![Architecture Diagram](https://github.com/user-attachments/assets/2d2e3f78-182c-4281-bcc7-dad027eebdf6)

---

## ⚙️ How It Works

### 1️⃣ Applicant Portal

* Users fill in a form and upload their resume.
* Data is sent via API Gateway to a Lambda function.
* Lambda stores the form data in DynamoDB and uploads the resume to S3.

### 2️⃣ Recruiter Portal

* Recruiters access a secured page to see all applications.
* The portal fetches data from a protected GET API Gateway endpoint.
* Resumes are accessible via secure S3 URLs.

---

## 🗂️ Configuration

* Update the **API endpoint URLs** in your frontend JavaScript as needed.
* To change the S3 bucket used for resumes, update the `bucketName` variable in your recruiter portal JS code.
* Ensure CORS is properly configured on your API Gateway endpoints for your frontend domain.

---

## 🚀 Deployment

1. **Lambda Functions**

   * Deploy via AWS Console, AWS SAM, or Serverless Framework.
   * Make sure IAM roles allow S3 and DynamoDB access.

2. **Frontend**

   * Upload your static HTML, CSS, and JS files to an S3 bucket with *Static Website Hosting* enabled.

3. **API Gateway**

   * Set up POST and GET endpoints.
   * Enable CORS for your frontend origin.

4. **DynamoDB & S3**

   * Create a DynamoDB table to store applicant data.
   * Create an S3 bucket for storing resumes.

---

## 📌 Notes

* IAM permissions must allow Lambda to access S3 and DynamoDB.
* Consider protecting recruiter endpoints with an API key or Cognito.
* For production, use private S3 buckets and pre-signed URLs for secure downloads.

---

## 📣 License

MIT License. Feel free to fork, modify, and deploy your own version!

---

If you want, you can customize the **Features**, **How It Works**, or **Deployment** sections with your own words even further.

If you tell me your GitHub repo name or style, I can make it even more personalized!

outputs
![Screenshot 2025-07-07 131857](https://github.com/user-attachments/assets/851c5a9e-1ef5-46cc-81ac-8247381ff4f2)
![Screenshot 2025-07-07 131843](https://github.com/user-attachments/assets/b00f088d-a8f9-4de8-a06e-fe896ed43494)


