# Zoom Clone - Video Conferencing Application

A full-stack video conferencing application built with React.js and Node.js, featuring real-time video/audio communication, screen sharing, and chat functionality.

## 🚀 Features

- **Real-time Video/Audio Communication**: Peer-to-peer video and audio calls using WebRTC
- **Screen Sharing**: Share your screen with other participants
- **Chat System**: Real-time messaging during video calls
- **User Authentication**: Secure user registration and login
- **Meeting History**: Track and view past meetings
- **Responsive Design**: Works on desktop and mobile devices
- **Modern UI**: Built with Material-UI components

## 🛠️ Tech Stack

### Frontend
- **React.js** - Frontend framework
- **Material-UI** - UI component library
- **Socket.io Client** - Real-time communication
- **React Router** - Navigation
- **Axios** - HTTP client

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **Socket.io** - Real-time communication
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **bcrypt** - Password hashing

## 📋 Prerequisites

Before running this application, make sure you have the following installed:

- **Node.js** (v14 or higher)
- **npm** or **yarn**
- **MongoDB** (local or cloud instance)

## 🚀 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/zoom-clone.git
cd zoom-clone
```

### 2. Backend Setup
```bash
cd backend
npm install
```

### 3. Frontend Setup
```bash
cd ../frontend
npm install
```

### 4. Environment Configuration

#### Backend Environment
Create a `.env` file in the `backend` directory:
```env
PORT=8000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
```

#### Frontend Environment
Update the server URL in `frontend/src/environment.js`:
```javascript
const server = "http://localhost:8000";
export default server;
```

### 5. Database Setup
Make sure MongoDB is running and update the connection string in `backend/src/app.js`:
```javascript
const connectionDb = await mongoose.connect("your_mongodb_connection_string")
```

## 🏃‍♂️ Running the Application

### Development Mode

1. **Start the Backend Server**
```bash
cd backend
npm run dev
```
The backend will run on `http://localhost:8000`

2. **Start the Frontend Development Server**
```bash
cd frontend
npm start
```
The frontend will run on `http://localhost:3000`

### Production Mode

1. **Build the Frontend**
```bash
cd frontend
npm run build
```

2. **Start the Backend in Production**
```bash
cd backend
npm start
```

## 📱 Usage

1. **Landing Page**: Visit `http://localhost:3000` to see the landing page
2. **Authentication**: Click on "Sign Up" or "Login" to create an account or sign in
3. **Home Dashboard**: After authentication, you'll see the home dashboard
4. **Start/Join Meeting**: 
   - Create a new meeting or join an existing one using a meeting URL
   - Enter your username in the lobby
   - Allow camera and microphone permissions
5. **Video Call Features**:
   - Toggle video on/off
   - Toggle microphone on/off
   - Share your screen
   - Send messages in the chat
   - End the call

## 🔧 API Endpoints

### Authentication
- `POST /api/v1/users/register` - User registration
- `POST /api/v1/users/login` - User login

### Socket Events
- `join-call` - Join a video call room
- `signal` - WebRTC signaling
- `chat-message` - Send chat message
- `user-joined` - User joined the call
- `user-left` - User left the call

## 🎯 Key Components

### Frontend Components
- **Landing Page** (`pages/landing.jsx`) - Welcome page
- **Authentication** (`pages/authentication.jsx`) - Login/Register
- **Home** (`pages/home.jsx`) - Dashboard
- **Video Meet** (`pages/VideoMeet.jsx`) - Main video call interface
- **History** (`pages/history.jsx`) - Meeting history

### Backend Components
- **Socket Manager** (`controllers/socketManager.js`) - WebRTC signaling
- **User Controller** (`controllers/user.controller.js`) - User management
- **User Routes** (`routes/users.routes.js`) - API routes
- **Models** - User and Meeting data models

## 🔒 Security Features

- Password hashing with bcrypt
- JWT token authentication
- CORS configuration
- Input validation and sanitization

## 🌐 Browser Compatibility

- Chrome (recommended)
- Firefox
- Safari
- Edge

**Note**: WebRTC features work best in Chrome and Firefox.

## 📝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🐛 Troubleshooting

### Common Issues

1. **Camera/Microphone not working**:
   - Ensure you've granted permissions in your browser
   - Check if other applications are using the camera/microphone

2. **Connection issues**:
   - Verify the backend server is running
   - Check the server URL in `environment.js`

3. **Database connection errors**:
   - Ensure MongoDB is running
   - Verify the connection string in `app.js`


## 👥 Author

- **ASHWIN JOBY GEORGE** 

## 🙏 Acknowledgments

- WebRTC for peer-to-peer communication
- Socket.io for real-time messaging
- Material-UI for beautiful components
- React community for excellent documentation

## 📞 Support

If you have any questions or need help, please open an issue in the GitHub repository.

---

**Happy Video Conferencing! 🎥📞**
