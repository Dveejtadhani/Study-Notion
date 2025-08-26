# Study-Notion
A Online Learning Platform -MERN Stack Project
# StudyNotion - MERN Stack Educational Platform

A complete educational web application inspired by platforms like Udemy or Coursera, built with the MERN stack (MongoDB, Express.js, React.js, Node.js).

## 🚀 Features

### 🔐 User Authentication
- **Simple Authentication**: No JWT/OTP - uses localStorage and React state
- **User Registration**: Name, email, password with validation
- **User Login**: Email/password authentication with bcrypt hashing
- **Session Management**: Persistent login state using localStorage
- **Logout**: Clear session and redirect to login

### 🎓 Course Management
- **Course Creation**: Instructors can create courses with comprehensive details
- **Course Editing**: Full CRUD operations for course management
- **Course Categories**: Programming, Design, Business, Marketing, Music, Photography, Other
- **Course Details**: Title, description, thumbnail, video URL, price, duration, level, tags
- **Video Integration**: YouTube video embedding support

### 🌐 Frontend Features
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Modern UI**: Clean, professional interface with smooth animations
- **Search & Filter**: Course search and category filtering
- **Pagination**: Efficient course listing with pagination
- **Protected Routes**: Authentication-based route protection
- **Toast Notifications**: User feedback with react-toastify

### 📱 Pages
- **Home Page**: Hero section, featured courses, statistics
- **Courses Page**: Grid/list view with search and filtering
- **Course Detail**: Full course information with video player
- **Login/Signup**: User authentication forms
- **Dashboard**: Instructor course management
- **404 Page**: User-friendly error page

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **bcryptjs** - Password hashing
- **express-validator** - Input validation
- **cors** - Cross-origin resource sharing

### Frontend
- **React.js** - UI library
- **React Router DOM** - Client-side routing
- **Tailwind CSS** - Utility-first CSS framework
- **Axios** - HTTP client
- **react-toastify** - Toast notifications
- **Lucide React** - Icon library

## 📦 Installation & Setup

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn

### 1. Clone the Repository
```bash
git clone <repository-url>
cd studynotion
```

### 2. Install Dependencies
```bash
# Install root dependencies
npm install

# Install backend dependencies
cd backend
npm install

# Install frontend dependencies
cd ../frontend
npm install
```

### 3. Environment Setup

#### Backend Configuration
Create a `.env` file in the `backend` directory:
```env
MONGODB_URI=mongodb://localhost:27017/studynotion
PORT=5000
NODE_ENV=development
```

For MongoDB Atlas, use:
```env
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/studynotion?retryWrites=true&w=majority
```

### 4. Database Setup
Make sure MongoDB is running locally or you have access to MongoDB Atlas.

### 5. Start the Application

#### Development Mode (Both Backend & Frontend)
```bash
# From root directory
npm run dev
```

#### Individual Start
```bash
# Start backend only
npm run server

# Start frontend only
npm run client
```

The application will be available at:
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000

## 📁 Project Structure

```
studynotion/
├── backend/
│   ├── controllers/
│   │   ├── authController.js
│   │   └── courseController.js
│   ├── models/
│   │   ├── User.js
│   │   └── Course.js
│   ├── routes/
│   │   ├── auth.js
│   │   └── courses.js
│   ├── config.env
│   ├── package.json
│   └── server.js
├── frontend/
│   ├── public/
│   │   └── index.html
│   ├── src/
│   │   ├── components/
│   │   │   ├── Navbar.js
│   │   │   ├── CourseCard.js
│   │   │   └── ProtectedRoute.js
│   │   ├── context/
│   │   │   └── AuthContext.js
│   │   ├── pages/
│   │   │   ├── Home.js
│   │   │   ├── Courses.js
│   │   │   ├── CourseDetail.js
│   │   │   ├── Login.js
│   │   │   ├── Signup.js
│   │   │   ├── Dashboard.js
│   │   │   └── NotFound.js
│   │   ├── services/
│   │   │   └── api.js
│   │   ├── App.js
│   │   ├── index.js
│   │   └── index.css
│   ├── package.json
│   ├── tailwind.config.js
│   └── postcss.config.js
├── package.json
└── README.md
```

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/profile/:id` - Get user profile

### Courses
- `GET /api/courses` - Get all courses (with pagination, search, filter)
- `GET /api/courses/:id` - Get single course
- `POST /api/courses` - Create new course
- `PUT /api/courses/:id` - Update course
- `DELETE /api/courses/:id` - Delete course
- `GET /api/courses/instructor/:instructorId` - Get courses by instructor

## 🎯 Usage Guide

### For Students
1. **Browse Courses**: Visit the home page or courses page to explore available courses
2. **Search & Filter**: Use the search bar and category filters to find specific courses
3. **View Course Details**: Click on any course to see detailed information and video preview
4. **Create Account**: Sign up to access the platform features
5. **Enroll in Courses**: Click "Enroll Now" to join courses (feature can be extended)

### For Instructors
1. **Create Account**: Sign up as an instructor
2. **Access Dashboard**: Navigate to the dashboard to manage your courses
3. **Create Courses**: Use the course creation form to add new courses
4. **Manage Courses**: Edit or delete existing courses
5. **Track Performance**: View statistics about your courses

## 🎨 Customization

### Styling
The application uses Tailwind CSS for styling. You can customize the design by:
- Modifying `frontend/tailwind.config.js` for theme customization
- Updating `frontend/src/index.css` for custom styles
- Changing color schemes in the Tailwind config

### Adding Features
- **Payment Integration**: Add Stripe or PayPal for course purchases
- **File Upload**: Integrate Cloudinary for image/video uploads
- **Real-time Chat**: Add Socket.io for instructor-student communication
- **Progress Tracking**: Implement course completion tracking
- **Reviews & Ratings**: Add course review system

## 🚀 Deployment

### Backend Deployment (Heroku)
1. Create a Heroku app
2. Set environment variables in Heroku dashboard
3. Connect your GitHub repository
4. Deploy the backend

### Frontend Deployment (Netlify/Vercel)
1. Build the frontend: `npm run build`
2. Deploy the `build` folder to Netlify or Vercel
3. Set environment variables for API URL

### Database Deployment
- Use MongoDB Atlas for cloud database
- Update the `MONGODB_URI` in your environment variables

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -am 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License.

## 🆘 Support

If you encounter any issues or have questions:
1. Check the console for error messages
2. Verify your MongoDB connection
3. Ensure all environment variables are set correctly
4. Check that all dependencies are installed

## 🎉 Acknowledgments

- Built with the MERN stack
- Inspired by educational platforms like Udemy and Coursera
- Uses modern web development best practices
- Responsive design for all devices 
