# ♻️ CircuLink – Circular Economy Marketplace

**CircuLink** is a full-stack web application that enables industries to trade waste materials — turning one company’s scrap into another’s raw material. By facilitating waste reuse, CircuLink supports the circular economy, reduces landfill contributions, and helps businesses save on raw material costs.

This project was born from a hackathon idea and is now being developed solo by [Ewa](https://github.com/ewa-edun) as a showcase of both frontend and backend development, data handling, and real-world problem-solving with sustainability in mind.

---

## 🚀 MVP Features

### 1. 🔐 **User Authentication**
- Companies can sign up as either **Buyers** or **Sellers**
- Login system using secure **Firebase Authentication**
- Authenticated users gain access to a personalized dashboard

### 2. ♻️ **Waste Listing System**
- Sellers can post detailed listings of waste materials, including:
  - Title and category (e.g., metals, plastics, e-waste)
  - Description
  - Quantity and units
  - Price per unit (or "open to offers")
  - Optional image upload
- Listings are stored in the backend (SQL) and images in Supabase storage bucket

### 3. 🔍 **Browse & Search Listings**
- Buyers can:
  - Browse all available waste listings
  - Search by keyword
  - Filter by category, location, or price
  - View complete details on each listing
- Responsive UI designed with React + CSS modules

### 4. 📩 **Express Interest System**
- Buyers can click “Express Interest” on a listing to notify the seller
- This triggers a notification and stores the expression in the seller’s dashboard
- Acts as a lead system for future contact

### 5. 📊 **User Dashboard**
- **Buyers**: 
  - View saved listings
  - Track interests expressed
- **Sellers**:
  - Manage posted waste listings
  - View list of buyers who showed interest
- Each user sees relevant data based on their role

### 6. 💬 **Real-Time Chat System**
- Enables **direct messaging** between buyers and sellers
- Used for:
  - Negotiating prices
  - Discussing pickup/delivery details
  - Asking product-related questions
- Tech: Firebase Realtime Database or WebSocket with Flask-SocketIO
- **Feature Highlights**:
  - Message history retained for each buyer-seller pair
  - Simple, clean UI with timestamped messages
  - Basic formatting (line breaks, emojis)

### 7. 🧠 **Recommendation Engine (MVP Version)**
- Basic logic for suggesting listings to buyers based on:
  - Category of interest
  - Location proximity (if enabled)
- Future-ready for ML upgrades

---

## 🛠️ Tech Stack

### Frontend
- **React.js**
- **React Router** (for routing)
- **Axios** (API communication)
- **Vanilla CSS**

### Backend
- **Python Flask** (REST API)
- **Flask-SQLAlchemy** (Database ORM)
- **Flask-JWT-Extended** (Authentication)
- **Flask-SocketIO** (for real-time chat, if not using Firebase)

### Database
- **PostgreSQL** or **SQLite** (for development)
- **Firebase Realtime DB** or **SocketIO** (chat messages)
- **Supabase** or **Firebase Storage** (images)
