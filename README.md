# 🏛️ CivicWatch

**CivicWatch** is a modern, full-stack civic issue reporting and tracking platform. It empowers citizens to report local issues like potholes, broken streetlights, or sanitation problems directly to the concerned authorities and track their resolution in real-time.

---

## 🚀 Live Demo
(https://civic-watch-backend-z51q.vercel.app/)



## ✨ Features

- **Issue Reporting**: Users can easily report civic issues with descriptions and images.
- **Image Uploads**: Integrated with Cloudinary for secure and fast image storage (using **Mongoose** for data modeling).
- **Interactive Maps**: Uses OpenStreetMap (via Leaflet) to pinpoint issue locations.
- **Real-time Status Tracking**: Citizens can track the progress of their reported issues.
- **Responsive Design**: Fully optimized for mobile, tablet, and desktop views.
- **Secure Authentication**: JWT-based authentication for user accounts.
- **Admin Dashboard**: (If applicable) To manage and update issue statuses.

## 🛠️ Tech Stack

### Frontend
- **React 19** with **Vite**
- **Tailwind CSS** for styling
- **Framer Motion** for smooth animations
- **Lucide React** for icons
- **React Leaflet** for maps
- **TanStack Query (React Query)** for data fetching
- **Sonner** for toast notifications

### Backend
- **Node.js** & **Express**
- **TypeScript** for type safety
- **MongoDB** with **Mongoose** (ODM)
- **Cloudinary** for media management
- **JWT** for secure authentication
- **Zod** for schema validation

---

## 📁 Project Structure

```text
CivicWatch/
├── frontend/          # React + Vite application
│   ├── src/           # Component logic and UI
│   └── vercel.json    # Frontend Vercel configuration
├── backend/           # Node.js + Express API
│   ├── src/           # API routes, controllers, and models
│   └── vercel.json    # Backend Vercel configuration
└── README.md          # Project documentation
```

---

## ⚙️ Local Setup

### 1. Clone the repository
```bash
git clone https://github.com/klu2300033050/CivicWatch---A-complaint-raiser.git
cd CivicWatch
```

### 2. Backend Setup
1. Navigate to the backend directory:
   ```bash
   cd backend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file and add your credentials (see Environment Variables section).
4. Start the development server:
   ```bash
   npm run build  # To compile TypeScript
   npm start      # To run the server
   ```

### 3. Frontend Setup
1. Navigate to the frontend directory:
   ```bash
   cd ../frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file and set the backend URL.
4. Start the development server:
   ```bash
   npm run dev
   ```

---

## 🔑 Environment Variables

### Backend (`backend/.env`)
| Variable | Description |
| :--- | :--- |
| `DATABASE_URL` | Your MongoDB Atlas connection string |
| `JWT_PASSWORD` | A secret key for signing JWT tokens |
| `CLOUDINARY_CLOUD_NAME` | Cloudinary cloud name |
| `CLOUDINARY_API_KEY` | Cloudinary API key |
| `CLOUDINARY_API_SECRET` | Cloudinary API secret |
| `PORT` | Port number (default: 3000) |
| `CORS_ORIGIN` | Allowed origin (e.g., your Vercel frontend URL) |

### Frontend (`frontend/.env`)
| Variable | Description |
| :--- | :--- |
| `VITE_BACKEND_URL` | The URL of your deployed backend (or localhost) |

---

## ☁️ Deployment on Vercel

Since this is a monorepo, follow these steps to deploy on Vercel:

### 1. Deploy the Backend
- Import the repository in Vercel.
- Set the **Root Directory** to `backend`.
- Add all the backend Environment Variables in the Vercel dashboard.
- Vercel will automatically use the `backend/vercel.json` file.

### 2. Deploy the Frontend
- Import the same repository as a *new* project in Vercel.
- Set the **Root Directory** to `frontend`.
- Set the **Build Command** to `npm run build`.
- Set the **Output Directory** to `dist`.
- Add `VITE_BACKEND_URL` to the Environment Variables (pointing to your deployed backend URL).

---

## 📄 License
This project is licensed under the ISC License.

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.
