# 🤖 AI Resume Builder

> **An AI-powered full-stack resume builder that helps users create, enhance, customize, preview, download, and share professional resumes online.**

[![Live Demo](https://img.shields.io/badge/Live-Demo-success?style=for-the-badge)](https://ai-resume-builder-rho-gold.vercel.app/)
[![Frontend](https://img.shields.io/badge/Frontend-Vercel-black?style=for-the-badge\&logo=vercel)](https://ai-resume-builder-rho-gold.vercel.app/)
[![Backend](https://img.shields.io/badge/Backend-Render-46E3B7?style=for-the-badge)](https://ai-resume-builder-backend-wq1m.onrender.com/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](#-license)

---

## 🌐 Live Demo

### 🚀 Frontend

**[Open AI Resume Builder](https://ai-resume-builder-rho-gold.vercel.app/)**

### ⚙️ Backend API

**[Backend API](https://ai-resume-builder-backend-wq1m.onrender.com/)**

---

## 📌 Overview

**AI Resume Builder** is a full-stack web application designed to simplify the resume creation process.

Users can create multiple resumes, improve their content using AI, upload an existing PDF resume for automatic extraction, customize templates and colors, add profile images, and publish their resumes with a shareable public URL.

The application combines a modern React frontend with a Node.js/Express backend, MongoDB for data persistence, and Google Gemini for AI-powered content enhancement.

---

## ✨ Features

### 👤 User Authentication

* 🔐 User Signup & Login
* 🔑 JWT-based authentication
* 🛡️ Protected user routes
* 👥 User-specific resume management

### 📄 Resume Management

* ➕ Create multiple resumes
* ✏️ Edit existing resumes
* 👀 Live resume preview
* 🗑️ Manage multiple resumes
* 📥 Download resume as PDF

### 🤖 AI-Powered Features

* ✨ AI-generated Professional Summary
* 💼 AI-enhanced Experience Descriptions
* 📑 Extract resume information from uploaded PDF
* 🧠 Automatically improve resume content using Google Gemini API

### 🎨 Customization

* 📋 Multiple professional resume templates
* 🎨 Custom theme colors
* 🖼️ Profile image upload
* ✂️ Automatic background removal using ImageKit

### 🌍 Resume Sharing

* 🔗 Publish resumes publicly
* 🌐 Generate shareable resume links
* 👀 Allow recruiters and others to view published resumes online

---

## 🖥️ Application Preview

> Add screenshots/GIFs of your application here.

```text
📸 Recommended screenshots:

1. Login / Signup
2. Resume Dashboard
3. Resume Editor
4. AI Enhancement
5. Live Resume Preview
6. Template Selection
7. Public Resume Page
```

Example:

```markdown
![Dashboard](./screenshots/dashboard.png)
![Resume Editor](./screenshots/editor.png)
![Resume Preview](./screenshots/preview.png)
```

---

## 🛠️ Tech Stack

### 🎨 Frontend

| Technology       | Purpose                  |
| ---------------- | ------------------------ |
| ⚛️ React         | User interface           |
| ⚡ Vite           | Development & build tool |
| 🎨 Tailwind CSS  | Styling                  |
| 🧭 React Router  | Client-side routing      |
| 🔗 Axios         | API communication        |
| 🖼️ Lucide Icons | UI icons                 |

### ⚙️ Backend

| Technology           | Purpose                               |
| -------------------- | ------------------------------------- |
| 🟢 Node.js           | Runtime environment                   |
| 🚂 Express.js        | REST API                              |
| 🍃 MongoDB           | Database                              |
| 🧩 Mongoose          | MongoDB ODM                           |
| 📤 Multer            | File uploads                          |
| 🔐 JWT               | Authentication                        |
| 🤖 Google Gemini API | AI-powered enhancements               |
| 🖼️ ImageKit         | Image processing & background removal |

### ☁️ Deployment

| Service      | Usage                      |
| ------------ | -------------------------- |
| ▲ Vercel     | Frontend deployment        |
| 🚀 Render    | Backend deployment         |
| 🍃 MongoDB   | Database                   |
| 🖼️ ImageKit | Image hosting & processing |

---

## 🏗️ Project Architecture

```text
                    ┌─────────────────────┐
                    │      User           │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   React + Vite      │
                    │    Frontend         │
                    └──────────┬──────────┘
                               │
                         REST API / Axios
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Node.js + Express   │
                    │      Backend        │
                    └──────┬──────┬───────┘
                           │      │
              ┌────────────┘      └────────────┐
              ▼                                ▼
       ┌──────────────┐                ┌──────────────┐
       │   MongoDB    │                │ Gemini API   │
       │  Database    │                │ AI Features  │
       └──────────────┘                └──────────────┘
                                             
                           ┌────────────────────┐
                           │     ImageKit       │
                           │ Image Processing   │
                           └────────────────────┘
```

---

## 📂 Project Structure

```text
AI-Resume-Builder/
│
├── client/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── ...
│
├── server/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── middleware/
│   ├── uploads/
│   ├── package.json
│   └── ...
│
├── README.md
└── .gitignore
```

---

## 🔐 Environment Variables

### Frontend

Create a `.env` file inside the `client` directory:

```env
VITE_BASE_URL=https://your-backend-url.onrender.com
```

### Backend

Create a `.env` file inside the `server` directory:

```env
MONGO_URI=your_mongodb_connection_string

JWT_SECRET=your_jwt_secret

IMAGEKIT_PUBLIC_KEY=your_imagekit_public_key
IMAGEKIT_PRIVATE_KEY=your_imagekit_private_key
IMAGEKIT_URL_ENDPOINT=your_imagekit_url_endpoint

GEMINI_API_KEY=your_gemini_api_key
```

> ⚠️ **Never commit your `.env` files or API keys to GitHub.**

---

## 🚀 Getting Started

Follow these steps to run the project locally.

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/AI-Resume-Builder.git

cd AI-Resume-Builder
```

### 2️⃣ Setup Backend

```bash
cd server

npm install
```

Create your `.env` file and add the required environment variables.

Then start the backend:

```bash
npm start
```

---

### 3️⃣ Setup Frontend

Open a new terminal:

```bash
cd client

npm install
```

Create the frontend `.env` file:

```env
VITE_BASE_URL=http://localhost:5000
```

Then start the development server:

```bash
npm run dev
```

---

## 🔄 How It Works

```text
1. User creates an account
          ↓
2. Creates a new resume
          ↓
3. Enters or uploads resume information
          ↓
4. AI enhances summary & experience
          ↓
5. User selects template & theme
          ↓
6. Live resume preview is generated
          ↓
7. Resume can be downloaded as PDF
          ↓
8. User can publish the resume
          ↓
9. Shareable public URL is generated
```

---

## 🤖 AI Resume Enhancement

The application uses **Google Gemini API** to improve resume content.

### Professional Summary

Users can provide basic information and receive a more polished professional summary.

### Experience Description

Existing experience descriptions can be enhanced to make them clearer, more professional, and resume-friendly.

### PDF Resume Extraction

Users can upload an existing resume PDF and automatically extract relevant information, reducing the amount of manual data entry required.

---

## 🎨 Resume Customization

Users can personalize their resumes using:

* 📄 Multiple templates
* 🎨 Custom theme colors
* 🖼️ Profile images
* ✨ AI-enhanced content
* 👀 Real-time preview

This allows users to create resumes suitable for different job applications.

---

## 🌍 Public Resume Sharing

Users can publish their completed resumes and receive a unique public URL.

Example:

```text
https://your-domain.com/resume/unique-resume-id
```

This makes it easy to share a resume with:

* Recruiters
* Hiring managers
* Companies
* Professional networks

---

## 🔒 Security

The application implements:

* JWT-based authentication
* Protected API routes
* Environment variables for secrets
* User-specific resume access
* Secure API communication

---

## 📈 Future Improvements

Potential improvements include:

* [ ] ATS Resume Score
* [ ] Job Description → Resume Optimization
* [ ] AI-powered keyword suggestions
* [ ] More resume templates
* [ ] LinkedIn profile import
* [ ] Resume analytics
* [ ] Custom domain for public resumes
* [ ] Cover Letter Generator
* [ ] Multiple PDF export formats
* [ ] Resume version history

---

## 🤝 Contributing

Contributions are welcome!

```bash
# Fork the repository

# Create a new branch
git checkout -b feature/your-feature

# Commit your changes
git commit -m "Add your feature"

# Push the branch
git push origin feature/your-feature
```

Then open a Pull Request.

---

## 📄 License

This project is licensed under the **MIT License**.

See the `LICENSE` file for more information.

---

## 👨‍💻 Author

**Shivani Kumari**

Built with ❤️ using **React, Node.js, Express, MongoDB, and Google Gemini AI**.

⭐ If you found this project useful, consider giving it a **star**!
