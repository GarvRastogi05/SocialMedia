<h1 align="center">📱 SocialMedia</h1>

<p align="center">
  <b>A full-stack social media platform built with React, Node.js, Express, MongoDB, ImageKit.io, and Clerk for authentication.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Frontend-React-blue?style=flat-square" />
  <img src="https://img.shields.io/badge/Backend-Node.js-green?style=flat-square" />
  <img src="https://img.shields.io/badge/Database-MongoDB-brightgreen?style=flat-square" />
  <img src="https://img.shields.io/badge/Images-ImageKit.io-orange?style=flat-square" />
  <img src="https://img.shields.io/badge/Auth-Clerk-purple?style=flat-square" />
  <img src="https://img.shields.io/badge/Version-1.0.0-blueviolet?style=flat-square" />
  <img src="https://img.shields.io/badge/License-MIT-lightgrey?style=flat-square" />
</p>

---

## 🚀 Overview  
**SocialMedia** is a modern social networking platform that allows users to create profiles, post updates, follow friends, and interact with content.  

It uses **ImageKit.io** for image uploads and optimization, and **Clerk** for secure authentication.  
Built with a React frontend and Node.js/Express backend, it offers a seamless experience for users to connect and share.

---

## ✨ Key Features  
- 📝 **Create and Edit Profiles**  
- 📸 **Upload and Share Images with ImageKit.io**  
- 🔄 **Follow and Unfollow Users**  
- 💬 **Comment on Posts**  
- ❤️ **Like and Share Posts**  
- 🔐 **User Authentication with Clerk**  
- 📱 **Responsive Design**  

---

## 🧩 Project Structure  
    SocialMedia/
    │
    ├─ client/ # React frontend
    │ ├─ src/
    │ │ ├─ components/
    │ │ ├─ pages/
    │ │ ├─ services/
    │ │ └─ App.js
    │ └─ package.json
    │
    ├─ server/ # Node.js + Express backend
    │ ├─ controllers/
    │ ├─ models/
    │ ├─ routes/
    │ ├─ config/
    │ ├─ services/ # ImageKit.io integration
    │ ├─ server.js
    │ └─ .env
    │
    └─ README.md

  
---

## ⚙️ Installation & Setup  

### 1️⃣ Clone the repository  
      ```bash
      git clone https://github.com/GarvRastogi05/SocialMedia.git
      cd SocialMedia
      
2️⃣ Backend Setup

    cd server
    npm install

3️⃣ Setup Environment Variables

Create a .env file inside the server/ directory:

    # Frontend URL
    FRONTEND_URL = http://localhost:5173
    
    # Clerk
    CLERK_PUBLISHABLE_KEY=  --------- CLERK PUBLISHABLE KEY ---------
    CLERK_SECRET_KEY=  --------- CLERK SECRET KEY ---------
    
    # MongoDB
    MONGODB_URI=  --------- MONGODB URI ---------
    
    # ImageKit
    IMAGEKIT_PUBLIC_KEY = '----- IMAGEKIT PUBLIC KEY -----'
    IMAGEKIT_PRIVATE_KEY = '----- IMAGEKIT PRIVATE KEY -----'
    IMAGEKIT_URL_ENDPOINT = '----- IMAGEKIT URL ENDPOINT -----'


Start the backend server:

    npm run start

4️⃣ Frontend Setup

    cd ../client
    npm install
    npm start

🖼️ ImageKit.io Integration

ImageKit.io is used for image upload, storage, and optimization.

Example usage in your backend:

    import ImageKit from "imagekit";
    
    const imagekit = new ImageKit({
      publicKey: process.env.IMAGEKIT_PUBLIC_KEY,
      privateKey: process.env.IMAGEKIT_PRIVATE_KEY,
      urlEndpoint: process.env.IMAGEKIT_URL_ENDPOINT,
    });
    
    const uploadImage = async (file) => {
      const result = await imagekit.upload({
        file,
        fileName: "profile-picture.jpg",
      });
      return result.url;
    };

🔐 Clerk Authentication

Clerk handles user signup, login, and session management.
Example integration in React frontend:

    import { ClerkProvider, SignedIn, SignedOut, SignIn } from '@clerk/clerk-react';
    
    function App() {
      return (
        <ClerkProvider frontendApi={process.env.CLERK_FRONTEND_API}>
          <SignedIn>
            <Dashboard />
          </SignedIn>
          <SignedOut>
            <SignIn />
          </SignedOut>
        </ClerkProvider>
      );
    }

🧠 Tech Stack

| Category       | Technology       |
| -------------- | ---------------- |
| Frontend       | React.js         |
| Backend        | Node.js, Express |
| Database       | MongoDB          |
| Authentication | Clerk            |
| Image Upload   | ImageKit.io      |



🧪 Usage

1. Create a profile using Clerk authentication.
2. Upload and share images with ImageKit.io.
3. Follow friends, comment, like, and share posts.
4. Enjoy a responsive social media experience on web and mobile.

👨‍💻 Contributing

Contributions are welcome!
1. Fork the repository
2. Create a branch (git checkout -b feature/your-feature)
3. Make your changes and commit (git commit -m "Add feature")
4.Push to your branch (git push origin feature/your-feature)
5.Open a Pull Request

<p align="center">💙 Developed by <b>Garv Rastogi</b></p> ```
