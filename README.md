# Productathon
# Asset Manager - Enhanced Edition

A comprehensive asset management platform with authentication, messaging, contractor profiles, task management, reporting, and 15 customizable themes.

## 🚀 Features

### ✅ Complete Authentication System
- Sign In / Sign Up pages with animations
- Role-based access control (Admin, Officer, Contractor, Customer)
- Session management
- Password hashing and security

### ✅ Messaging System
- Internal communication between all users
- Send messages to officers, contractors, and customers
- Message threading and replies
- Read/unread status tracking
- Real-time message notifications

### ✅ Contractor Profiles
- Detailed contractor profiles with bio, skills, and certifications
- Rating system (1-5 stars)
- Hourly rate tracking
- Availability status
- Completed projects counter
- Task history and performance metrics

### ✅ Enhanced Task Management
- Create tasks directly from task section
- Assign to officers or contractors
- Priority levels (Low, Medium, High, Urgent)
- Progress tracking with percentage (0-100%)
- Status management (Pending, In Progress, Completed)
- Due date management
- Visual progress bars

### ✅ Reports & Analytics
- Task completion reports with charts
- Lead conversion analytics
- Contractor performance metrics
- Officer activity tracking
- Interactive charts (Bar, Line, Pie)
- Export functionality
- Date range filtering

### ✅ 15 Beautiful Themes
1. Default
2. Ocean Blue
3. Forest Green
4. Sunset Orange
5. Lavender Purple
6. Rose Pink
7. Slate Gray
8. Crimson Red
9. Mint Green
10. Amber Gold
11. Sky Blue
12. Emerald
13. Indigo
14. Teal
15. Monochrome

### ✅ Smooth Animations
- Page transitions using Framer Motion
- Loading states
- Hover effects
- Toast notifications
- Card animations

## 🛠️ Tech Stack

- **Frontend**: React 18 + TypeScript + Vite
- **UI Framework**: shadcn/ui + Tailwind CSS
- **Animations**: Framer Motion
- **Backend**: Express + Node.js
- **Database**: PostgreSQL + Drizzle ORM
- **Authentication**: Passport.js + bcrypt
- **State Management**: TanStack Query
- **Charts**: Recharts

## 📦 Installation

### Prerequisites
- Node.js 20+
- PostgreSQL database
- npm or yarn

### Step 1: Clone and Install
```bash
cd Asset-Manager-Enhanced
npm install
```

### Step 2: Database Setup
1. Create a PostgreSQL database
2. Create `.env` file:
```env
DATABASE_URL=postgresql://username:password@localhost:5432/asset_manager
SESSION_SECRET=your-super-secret-key-change-this
NODE_ENV=development
```

### Step 3: Initialize Database
```bash
npm run db:push
```

### Step 4: Start Development Server
```bash
npm run dev
```

The application will be available at `http://localhost:5000`

## 📱 User Roles

### Admin
- Full system access
- User management
- All CRUD operations
- System-wide reports
- Theme customization

### Officer
- Lead management
- Task creation and assignment
- Contractor communication
- Regional reports
- Theme customization

### Contractor
- Personal profile management
- View assigned tasks
- Update task progress
- Message officers
- Theme customization

### Customer
- View projects
- Track progress
- Communication
- Theme customization

## 🎨 Using Themes

1. Navigate to Settings page
2. Choose from 15 available themes
3. Toggle between light/dark mode
4. Theme preference is saved per user

## 📊 Database Schema

### New Tables
- `users` - Authentication and user management
- `messages` - Internal messaging system
- `customers` - Customer profiles
- `reports` - Generated reports
- `notifications` - System notifications

### Enhanced Tables
- `contractors` - Extended with profile fields
- `tasks` - Added priority and progress tracking

## 🔐 Security Features

- Password hashing (bcrypt)
- Session management
- Role-based access control
- Protected API routes
- Input validation
- CSRF protection

## 📋 API Endpoints

### Authentication
- `POST /api/auth/register` - Create new user
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/me` - Get current user

### Messages
- `GET /api/messages` - Get all messages
- `POST /api/messages` - Send new message
- `PATCH /api/messages/:id/read` - Mark as read

### Tasks
- `GET /api/tasks` - List all tasks
- `POST /api/tasks` - Create new task
- `PATCH /api/tasks/:id` - Update task
- `PATCH /api/tasks/:id/progress` - Update progress

### Contractors
- `GET /api/contractors` - List contractors
- `GET /api/contractors/:id` - Get contractor profile
- `PATCH /api/contractors/:id` - Update profile

### Reports
- `GET /api/reports` - Get reports
- `POST /api/reports/generate` - Generate new report

## 🚀 Deployment

### Build for Production
```bash
npm run build
npm start
```

### Environment Variables (Production)
```env
DATABASE_URL=your-production-database-url
SESSION_SECRET=your-production-secret
NODE_ENV=production
```

## 📖 Usage Guide

### Creating a Task
1. Navigate to Tasks page
2. Click "Create Task" button
3. Fill in details (title, description, priority, assignee)
4. Set due date and initial progress
5. Click "Create"

### Sending Messages
1. Go to Messages page
2. Click "Compose" button
3. Select recipient
4. Write subject and message
5. Click "Send Message"

### Viewing Contractor Profile
1. Go to Contractors page
2. Click on a contractor card
3. View detailed profile, skills, and performance
4. Assign tasks or send messages directly

### Generating Reports
1. Navigate to Reports page
2. Select report type
3. Choose date range (optional)
4. View interactive charts and statistics
5. Export if needed

## 🎯 Key Improvements from Original

1. ✅ Complete authentication system with sign in/up
2. ✅ Internal messaging for all user types
3. ✅ Detailed contractor profiles with ratings
4. ✅ Task creation from task section
5. ✅ Progress bars on all tasks
6. ✅ Comprehensive reports section
7. ✅ 15 customizable themes
8. ✅ Smooth animations throughout
9. ✅ Role-based access control
10. ✅ Mobile responsive design

## 🔧 Troubleshooting

### Database Connection Issues
- Verify DATABASE_URL in .env
- Ensure PostgreSQL is running
- Check database credentials

### Build Errors
- Clear node_modules: `rm -rf node_modules && npm install`
- Clear cache: `npm run clean`

### Authentication Issues
- Check SESSION_SECRET is set
- Verify cookies are enabled
- Clear browser cookies

## 📝 License

MIT License - Feel free to use in your projects!

## 🤝 Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📧 Support

For issues or questions:
- Check the Implementation Guide
- Review the documentation
- Create an issue on GitHub

## 🎉 What's Next?

Future enhancements planned:
- File attachments in messages
- Real-time notifications (WebSocket)
- Email integration
- Calendar view for tasks
- Advanced search and filters
- Bulk operations
- PDF/Excel export
- Two-factor authentication
- Profile image uploads
- Activity logs
- Advanced analytics

---

Built with ❤️ using React, TypeScript, and modern web technologies.
