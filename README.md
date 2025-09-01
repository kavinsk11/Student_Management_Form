# Student_Management_Form

# Student Management System

A full-stack web application for managing student records with CRUD (Create, Read, Update, Delete) operations. Built with Node.js, Express.js, MongoDB, and vanilla HTML/CSS/JavaScript.

## Features

### Backend Features
- **RESTful API** with Express.js
- **MongoDB** database with Mongoose ODM
- **Input validation** and error handling
- **CORS** enabled for cross-origin requests
- **Environment configuration** support

### Frontend Features
- **Modern, responsive UI** with beautiful gradients and animations
- **Real-time search** and filtering by program
- **Modal dialogs** for edit and delete operations
- **Form validation** with visual feedback
- **Success/error notifications**
- **Loading states** and smooth transitions
- **Mobile-responsive** design

### CRUD Operations
- ✅ **Create**: Add new student records
- ✅ **Read**: View all students and filter by program
- ✅ **Update**: Edit existing student information
- ✅ **Delete**: Remove student records with confirmation

### Student Fields
- Student ID (unique)
- Full Name
- Email (unique)
- Phone Number
- Program (dropdown selection)
- Batch Year

## Technology Stack

- **Backend**: Node.js, Express.js, MongoDB, Mongoose
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **Database**: MongoDB
- **Styling**: Custom CSS with gradients and animations
- **Icons**: Font Awesome

## Prerequisites

Before running this application, make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/try/download/community) (v4.4 or higher)
- [npm](https://www.npmjs.com/) (comes with Node.js)

## Installation & Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd student-management-system
```

### 2. Install Backend Dependencies
```bash
cd backend
npm install
```

### 3. Configure Environment Variables
Create a `.env` file in the `backend` directory:
```env
MONGODB_URI=mongodb://localhost:27017/student-management-system
PORT=5000
NODE_ENV=development
```

### 4. Start MongoDB
Make sure MongoDB is running on your system:
```bash
# On Windows
net start MongoDB

# On macOS/Linux
sudo systemctl start mongod
```

### 5. Start the Backend Server
```bash
cd backend
npm start
```

The server will start on `http://localhost:5000`

### 6. Open the Frontend
Open `frontend/index.html` in your web browser, or serve it using a local server:

```bash
# Using Python 3
cd frontend
python -m http.server 8000

# Using Node.js (if you have http-server installed)
cd frontend
npx http-server -p 8000
```

Then visit `http://localhost:8000`

## API Endpoints

### Students
- `GET /api/students` - Get all students
- `GET /api/students?program=Computer Science` - Get students by program
- `GET /api/students/:studentId` - Get student by ID
- `POST /api/students` - Create new student
- `PUT /api/students/:studentId` - Update student
- `DELETE /api/students/:studentId` - Delete student

### Health Check
- `GET /api/health` - Server health status

## Usage

### Adding a Student
1. Fill out the "Add New Student" form
2. Click "Add Student" button
3. The student will be added to the database and displayed in the table

### Viewing Students
- All students are displayed in a table format
- Use the search box to filter by name, email, or student ID
- Use the program dropdown to filter by specific program

### Editing a Student
1. Click the "Edit" button next to any student
2. Modify the information in the modal
3. Click "Update Student" to save changes

### Deleting a Student
1. Click the "Delete" button next to any student
2. Confirm the deletion in the modal
3. The student will be permanently removed

## Project Structure

```
student-management-system/
├── backend/
│   ├── models/
│   │   └── Student.js          # Student data model
│   ├── routes/
│   │   └── students.js         # Student API routes
│   ├── server.js               # Main server file
│   ├── package.json            # Backend dependencies
│   └── README.md               # Backend documentation
├── frontend/
│   ├── index.html              # Main HTML file
│   ├── styles.css              # CSS styles
│   └── script.js               # JavaScript functionality
└── README.md                   # This file
```

## Development

### Running in Development Mode
```bash
cd backend
npm run dev  # Uses nodemon for auto-restart
```

### Adding Sample Data
You can add sample data by calling the `addSampleData()` function in the browser console:
```javascript
addSampleData()
```

## Error Handling

The application includes comprehensive error handling:

- **Validation errors**: Form validation with user-friendly messages
- **Duplicate entries**: Prevents duplicate student IDs and emails
- **Network errors**: Graceful handling of API connection issues
- **Server errors**: Proper HTTP status codes and error messages

## Security Features

- **Input sanitization**: All user inputs are validated and sanitized
- **CORS configuration**: Proper cross-origin resource sharing setup
- **Environment variables**: Sensitive configuration stored in .env file
- **MongoDB injection protection**: Using Mongoose for safe database operations

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

If you encounter any issues or have questions, please:

1. Check the console for error messages
2. Ensure MongoDB is running
3. Verify all dependencies are installed
4. Check that the backend server is running on port 5000

## Future Enhancements

- [ ] User authentication and authorization
- [ ] File upload for student photos
- [ ] Advanced filtering and sorting
- [ ] Export data to CSV/PDF
- [ ] Pagination for large datasets
- [ ] Real-time notifications
- [ ] Dark mode theme
- [ ] Multi-language support
