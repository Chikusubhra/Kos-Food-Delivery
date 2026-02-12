# 🥗 KOS: Food Delivery Web App

**KOS** is a high-performance, full-stack delivery platform designed to mirror the robust functionality of industry leaders like Zomato and Swiggy. This project showcases a scalable MERN architecture, secure payment integrations, and real-time location services.

---

## 📸 Project Gallery

| Home Page | Menu Listing | Checkout |
| :--- | :--- | :--- |
| ![Home](../WhatsApp%20Image%202026-02-11%20at%2011.10.27%20PM.jpeg) | ![Menu](../WhatsApp%20Image%202026-02-11%20at%2011.11.58%20PM.jpeg) | ![Shop Owner](../WhatsApp%20Image%202026-02-11%20at%2011.11.10%20PM.jpeg) | ![Delivery Boy](../WhatsApp%20Image%202026-02-11%20at%2011.15.55%20PM.jpeg) |

>
---

## 🛠 Tech Stack

* **Frontend:** React.js (Vite), Tailwind CSS, Firebase
* **Backend:** Node.js, Express.js
* **Database:** MongoDB Atlas (NoSQL)
* **Infrastructure:** Cloudinary (Media), Razorpay (Payments), Geo-location API



[Image of MERN stack architecture diagram]


---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/KOS-food-delivery.git](https://github.com/your-username/KOS-food-delivery.git)
cd KOS-food-delivery

```

### 2. Configure Environment Variables

Create the following `.env` files. **Do not share these keys publicly.**

#### **Backend (`/backend/.env`)**

```env
PORT=8000
MONGODB_URL="mongodb+srv://your_user_name:your_password@cluster.mongodb.net/KOS"
JWT_SECRET="your_secret_key"
EMAIL="your@gmail.com"
PASS="your_app_password"
CLOUDINARY_CLOUD_NAME="your_name"
CLOUDINARY_API_KEY="your_key"
CLOUDINARY_API_SECRET="your_secret"
RAZORPAY_KEY_ID="your_id"
RAZORPAY_KEY_SECRET="your_secret"

```

#### **Frontend (`/frontend/.env`)**

```env
VITE_FIREBASE_APIKEY="your_key"
VITE_GEOAPIKEY="your_key"
VITE_RAZORPAY_KEY_ID="your_id"

```

### 3. Run the Project

Open two terminals in VS Code:

**Terminal 1 (Server):**

```bash
cd backend
npm install
npm run dev

```

**Terminal 2 (Client):**

```bash
cd frontend
npm install
npm run dev

```

💳 1. Razorpay (Payments)
Log in to your Razorpay Dashboard.

Navigate to Settings > API Keys.

Click Generate Test Key.

Copy Key ID (Frontend & Backend) and Key Secret (Backend only).

☁️ 2. Cloudinary (Image Storage)
Log in to your Cloudinary Console.

On your Dashboard, look for Product Environment Credentials.

Copy the Cloud Name, API Key, and API Secret.

🔥 3. Firebase (Authentication)
Go to the Firebase Console.

Create a project and add a Web App.

Copy the apiKey from the config object for your Frontend .env.

🗺️ 4. Geoapify (Maps & Routing)
Log in to the Geoapify MyProjects page.

Create a new project and click on API Keys.

Copy your API Key and paste it into the Frontend .env under VITE_GEOAPIKEY

---

## 🚀 Technical Challenges & Solutions

### 🔐 Secure Payment Workflows

**Challenge:** Preventing "fake" order successes.
**Solution:** Implemented **Razorpay Webhooks**. The backend uses the `crypto` library to hash and verify the payment signature before updating the database.

### ☁️ Media Optimization

**Challenge:** Handling large image uploads for food menus.
**Solution:** Integrated **Cloudinary API**. Images are offloaded to a CDN, reducing server load and ensuring fast image delivery to users.

### 📍 Location Intelligence

**Challenge:** Calculating delivery distances.
**Solution:** Integrated **Google Geo-location API** with **Debouncing** logic in React to minimize API costs and improve UI responsiveness.

---

## 📂 Project Structure

```text
KOS-ROOT/
├── backend/
│   ├── models/         # MongoDB Schemas
│   ├── routes/         # API Endpoints
│   ├── controllers/    # Business Logic
│   └── .env            # Private Server Config
├── frontend/
│   ├── src/
│   │   ├── components/ # UI Kit
│   │   ├── pages/      # View Layers
│   │   └── context/    # Global State
│   └── .env            # Public Client Config
└── README.md

```

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

```
MIT License

Copyright (c) 2026

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

```
