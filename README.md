# 🌏 TravelWorld Backend

A robust and scalable Node.js backend for the TravelWorld platform, handling tours, bookings, user authentication, blogs, reviews, and more! Powered by Express.js and MongoDB.

## 🚀 Features

- **User Authentication** – Register, login, JWT-based protection.
- **Tour Management** – CRUD endpoints for tours, featured & search capabilities.
- **Bookings** – Secure booking system for tours with user information.
- **Reviews** – Users can post and manage reviews on tours.
- **Blog System** – Platform admins can post, update, and highlight blogs with comments.
- **Contact Management** – Visitors can send queries or messages.
- **Robust Data Models** – Cleanly modeled with Mongoose.
- **Environment-friendly** – Dotenv support for secure, flexible environment configuration.

---

## 🗂 Project Structure

```
.
├── controllers/       # Logic for features (auth, tour, booking, blog, etc.)
├── models/            # Mongoose schemas (User, Tour, Booking, Review, Blog, Comment, Contact)
├── router/            # Route definitions
├── utils/             # Utility modules (e.g., JWT verification)
├── index.js           # App entrypoint (Express server)
├── package.json       # Project metadata & dependencies
└── .gitpod.yml        # Gitpod configuration
```

## 📦 Installation

```sh
# Install dependencies
npm install

# Set up your MongoDB URI and JWT secret in a .env file:
cp .env.example .env
```

## 🧑‍💻 Usage

```sh
# Run development server (with nodemon)
npm run dev

# Or run in production
npm start
```
Server starts (default) on: `http://localhost:8000`

## 📚 API Endpoints

### Auth
- `POST /api/v1/auth/register` (Register a new user)
- `POST /api/v1/auth/login` (Login user and get JWT)

### Tours
- `GET /api/v1/tours` (All tours)
- `POST /api/v1/tours` (Create tour)
- `GET /api/v1/tours/:id` (Single tour)
- `PUT /api/v1/tours/:id` (Update)
- `DELETE /api/v1/tours/:id` (Delete)
- `GET /api/v1/tours/featured` (Featured tours)
- `GET /api/v1/tours/count` (Tour count)
- `GET /api/v1/search` (Tour search: city, distance, group size, etc.)

### Bookings
- `POST /api/v1/booking` (Book a tour)
- `GET /api/v1/booking` (All bookings)
- `GET /api/v1/booking/:id` (Single booking)

### Users
- `GET /api/v1/users` (All users)
- `GET /api/v1/users/:id` (Single user)
- `POST /api/v1/users` (Create)
- `PUT /api/v1/users/:id` (Update)
- `DELETE /api/v1/users/:id` (Delete)

### Reviews
- `POST /api/v1/review/:TourId` (Add review)
- `GET /api/v1/review/:TourId` (Tour reviews)
- `DELETE /api/v1/review/:reviewId` (Delete review)

### Blogs & Comments
- `GET /api/v1/blogs` (All blogs)
- `POST /api/v1/blogs` (Create)
- `PUT /api/v1/blogs/:id` (Update)
- `GET /api/v1/blogs/:id` (Single blog)
- `GET /api/v1/blogs/featured` (Featured blogs)
- `POST /api/v1/comment/:BlogId` (Add comment)
- `GET /api/v1/comment/:BlogId` (Get comments by blog)
- `DELETE /api/v1/comment/:commentId` (Delete comment)

### Contact
- `POST /api/v1/contact` (New contact message)
- `GET /api/v1/contact` (All contacts)
- `GET /api/v1/contact/:id` (Single contact)

---

## 🛠️ Tech Stack

- **Node.js** & **Express** – Backend server
- **MongoDB** & **Mongoose** – Database and data modeling
- **JWT** – Authentication
- **bcrypt** – Password hashing
- **dotenv** – Environment config
- **Nodemon** – Dev tool for live reload

---

## 👤 Author

**Jaideep Naidu Killari**

---

## 👥 Contributing

PRs and suggestions welcome! Please open an issue or create a pull request for contributions.

---

## 📄 License

ISC License

---
