# 🏨 Hotel Booking App (MERN Stack)

This guide will walk you through setting up and running the **Hotel Booking App** on your local machine.

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed on your system:

* **Node.js** (LTS version recommended)
* **MongoDB Atlas** account
* **Cloudinary** account
* **Stripe** account

---

## 🚀 Cloning the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/PrriyaBandita-2002/Hotel_booking_app.git
cd Hotel_booking_app
```

---

## ⚙️ Backend Configuration

### Step 1: Environment Files

Navigate to the `backend` folder and create two files:

* `.env`
* `.env.e2e`

Add the following contents to **both** files:

```bash
MONGODB_CONNECTION_STRING=
JWT_SECRET_KEY=
FRONTEND_URL=

# Cloudinary
CLOUDINARY_CLOUD_NAME=
CLOUDINARY_API_KEY=
CLOUDINARY_API_SECRET=

# Stripe
STRIPE_API_KEY=
```

### Step 2: MongoDB Setup

1. Sign up at [MongoDB Atlas](https://www.mongodb.com/atlas).
2. Create a new cluster and database.
3. Copy your **MongoDB connection string** and paste it into the `MONGODB_CONNECTION_STRING` variable in both `.env` files.

> 💡 For the `.env.e2e` file, create a **separate test database** for running automated tests.

### Step 3: Cloudinary Setup

1. Create an account at [Cloudinary](https://cloudinary.com/).
2. From your dashboard, note the **cloud name**, **API key**, and **API secret**.
3. Add these values to the respective variables in your `.env` files.

### Step 4: Stripe Setup

1. Sign up at [Stripe](https://stripe.com/).
2. Copy your **API key** from the dashboard.
3. Add it to the `STRIPE_API_KEY` variable.

### Step 5: JWT Secret

Set `JWT_SECRET_KEY` to a long random string (you can generate one [here](https://generate-secret.vercel.app/32)).

### Step 6: Frontend URL

If you’re running locally, set:

```bash
FRONTEND_URL=http://localhost:5173
```

---

## 💻 Frontend Configuration

Navigate to the `frontend` folder and create a `.env` file with the following:

```bash
VITE_API_BASE_URL=http://localhost:7000
VITE_STRIPE_PUB_KEY=
```

> Replace `VITE_STRIPE_PUB_KEY` with your **Stripe publishable key**.

---

## 🧩 Running the Application

### Backend

```bash
cd backend
npm install
npm start
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

The frontend should now be running at:
👉 **[http://localhost:5173](http://localhost:5173)**
(Verify the exact port in your terminal.)

---

## 🧪 Running Automated Tests

### Step 1: Test Database Setup

1. Create a **new MongoDB project and cluster** for testing.
2. Add the connection string to the `MONGODB_CONNECTION_STRING` in your `.env.e2e` file.

### Step 2: Importing Test Data

The repository includes a `data` folder with test JSON files:

* `test-users.json`
* `test-hotel.json`

To import these:

1. Open **MongoDB Compass** and connect to your test database.
2. Go to your `users` collection → **Add Data** → **Import File** → select `test-users.json`.
3. Repeat for your `hotels` collection using `test-hotel.json`.

**Test Credentials:**
`Email:` [1@1.com](mailto:1@1.com)
`Password:` password123

---

### Step 3: Run Tests Using Playwright

1. Install the **Playwright extension** in VS Code.
2. Start both frontend and backend servers.
3. Open the `e2e-tests` directory and run:

```bash
npm install
```

4. Use the Playwright extension to execute automated tests.

---

## 👩‍💻 Author

**Developed by:** [Prriya Bandita](https://github.com/PrriyaBandita-2002)

---

## 🧾 License

This project is open-source and available under the [MIT License](LICENSE).

---

© 2025 Prriya Bandita — All rights reserved.


