# CivicLink

A modern, intelligent civic issue management platform that empowers citizens and municipal administrators to collaborate effectively in addressing urban challenges. Built with Next.js 15, TypeScript, MongoDB, and Tailwind CSS.

![CivicLink Banner](https://images.unsplash.com/photo-1486406146926-c627a92ad1ab?w=1200&h=300&fit=crop)

## 🌟 Overview

CivicLink transforms how cities manage civic issues by providing a comprehensive platform for issue reporting, tracking, and resolution. Whether you're a citizen reporting a pothole or a city administrator managing municipal operations, CivicLink streamlines the entire process with real-time updates and intelligent workflows.

### Key Features

- 🗺️ **Real-time Issue Mapping** - Interactive maps with live issue tracking and geographical analytics
- 👥 **Multi-role Management** - Dedicated dashboards for citizens, field workers, department admins, and city officials
- 📊 **Advanced Analytics** - Comprehensive reporting with performance metrics and data-driven insights
- 🔒 **Enterprise Security** - Bank-level security with encrypted data and secure authentication
- ⚡ **Automated Workflows** - Smart assignment algorithms and automated notifications
- 📱 **Mobile Optimized** - Fully responsive design for seamless mobile experience

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v18 or higher)
- **npm** or **yarn**
- **MongoDB** (Atlas or local instance)
- **Git**

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/KD-3030/nextjs-migration.git
cd nextjs-migration
```

2. **Install dependencies**

```bash
npm install
```

3. **Set up environment variables**

Copy the `.env.local` file and configure your environment:

```bash
cp .env.local .env.local
```

Update the following variables in `.env.local`:

```env
# Demo Mode (for development without backend)
NEXT_PUBLIC_DEMO_MODE=true

# MapBox Configuration (optional, for enhanced maps)
NEXT_PUBLIC_MAPBOX_ACCESS_TOKEN=your_mapbox_token

# MongoDB Configuration
MONGODB_URI=your_mongodb_connection_string

# Authentication & JWT Configuration
JWT_SECRET=your_secret_key_here
```

4. **Seed the database (optional)**

```bash
npm run seed
```

5. **Run the development server**

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## 📁 Project Structure

```
civiclink/
├── public/              # Static assets and images
├── src/
│   ├── app/            # Next.js 15 App Router pages
│   │   ├── api/        # API routes
│   │   ├── dashboard/  # Dashboard pages for different roles
│   │   ├── login/      # Authentication pages
│   │   └── register/   # User registration
│   ├── components/     # Reusable React components
│   │   ├── ui/         # UI components (buttons, cards, etc.)
│   │   └── ...         # Feature-specific components
│   ├── contexts/       # React Context providers
│   ├── lib/            # Utility functions and configurations
│   │   ├── auth.ts     # Authentication utilities
│   │   ├── mongodb.ts  # Database connection
│   │   └── utils.ts    # Helper functions
│   ├── models/         # MongoDB/Mongoose models
│   │   ├── User.ts     # User model
│   │   ├── Issue.ts    # Issue model
│   │   ├── Department.ts # Department model
│   │   └── Analytics.ts # Analytics model
│   └── scripts/        # Utility scripts (e.g., database seeding)
├── .env.local          # Environment variables
├── next.config.js      # Next.js configuration
├── tailwind.config.ts  # Tailwind CSS configuration
├── tsconfig.json       # TypeScript configuration
└── package.json        # Project dependencies
```

## 🎭 User Roles

CivicLink supports multiple user roles, each with specific permissions and dashboards:

### 1. **Citizen**
- Report civic issues with photos and location
- Track reported issues in real-time
- Provide feedback on resolved issues
- View community issue map

### 2. **Field Worker**
- View assigned issues
- Update issue status and progress
- Upload work completion photos
- Navigate to issue locations

### 3. **Department Admin**
- Manage department-specific issues
- Assign issues to field workers
- Monitor department performance
- Access analytics and reports

### 4. **Regional Admin**
- Oversee ward-level operations
- Manage multiple departments
- View regional analytics
- Coordinate cross-department issues

### 5. **City Admin**
- Citywide issue management
- Strategic planning and resource allocation
- Comprehensive analytics dashboard
- User and department management

### 6. **Super Admin**
- System-wide administration
- User role management
- Platform configuration
- Security and audit logs

## 🛠️ Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
- `npm run seed` - Seed database with sample data

## 🗺️ Key Technologies

- **Framework**: Next.js 15 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Database**: MongoDB with Mongoose
- **Authentication**: JWT (JSON Web Tokens)
- **Maps**: Leaflet & React Leaflet
- **Forms**: React Hook Form with Zod validation
- **UI Components**: Custom components with Framer Motion animations
- **Icons**: Lucide React

## 🔐 Authentication

CivicLink uses JWT-based authentication with secure password hashing (bcrypt). The authentication flow includes:

1. User registration with role selection
2. Secure login with JWT token generation
3. Token-based session management
4. Role-based access control (RBAC)

## 📊 Issue Management Workflow

1. **Report** - Citizen reports an issue with details and location
2. **Triage** - System categorizes and prioritizes the issue
3. **Assign** - Department admin assigns to appropriate field worker
4. **Work** - Field worker updates status and resolves the issue
5. **Verify** - Admin verifies completion
6. **Feedback** - Citizen provides feedback on resolution

## 🌍 Demo Mode

CivicLink includes a demo mode for testing without backend dependencies:

```env
NEXT_PUBLIC_DEMO_MODE=true
```

In demo mode:
- Sample data is used for all displays
- No database connection required
- All user roles can be explored
- Perfect for presentations and testing

## 📈 Analytics & Reporting

CivicLink provides comprehensive analytics:

- **Issue Trends** - Track issue volume over time
- **Resolution Times** - Monitor average resolution times
- **Department Performance** - Compare department efficiency
- **Geographic Hotspots** - Identify problem areas
- **Category Analysis** - Understand issue distribution
- **User Engagement** - Track citizen participation

## 🎨 Customization

### Theming

CivicLink uses Tailwind CSS for styling. Customize colors and theme in `tailwind.config.ts`:

```typescript
colors: {
  primary: {
    400: '#your-color',
    500: '#your-color',
    600: '#your-color',
    // ...
  }
}
```

### Configuration

Modify `next.config.js` for Next.js settings:

```javascript
const nextConfig = {
  images: {
    domains: ['your-image-domain.com'],
  },
  // Add your configuration
};
```

## 🧪 Testing

Currently, the project uses ESLint for code quality. To run linting:

```bash
npm run lint
```

## 🚢 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Import project in Vercel
3. Configure environment variables
4. Deploy

### Docker

```bash
# Build image
docker build -t civiclink .

# Run container
docker run -p 3000:3000 civiclink
```

### Manual Deployment

```bash
# Build the application
npm run build

# Start production server
npm run start
```

## 📝 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `NEXT_PUBLIC_DEMO_MODE` | Enable demo mode without backend | No |
| `MONGODB_URI` | MongoDB connection string | Yes* |
| `JWT_SECRET` | Secret key for JWT tokens | Yes* |
| `NEXT_PUBLIC_MAPBOX_ACCESS_TOKEN` | MapBox access token for maps | No |

*Required for production; optional in demo mode

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style

- Follow TypeScript best practices
- Use functional components with hooks
- Maintain consistent formatting (use ESLint)
- Write descriptive commit messages

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:

- 📧 Email: support@civiclink.com
- 📖 Documentation: [docs.civiclink.com](https://docs.civiclink.com)
- 🐛 Issues: [GitHub Issues](https://github.com/KD-3030/nextjs-migration/issues)

## 🙏 Acknowledgments

- Next.js team for the amazing framework
- MongoDB team for the robust database
- Tailwind CSS for the utility-first CSS framework
- OpenStreetMap for map data
- All contributors and users of CivicLink

## 🗺️ Roadmap

- [ ] Mobile native applications (iOS/Android)
- [ ] Real-time notifications via WebSocket
- [ ] AI-powered issue categorization
- [ ] Integration with third-party GIS systems
- [ ] Multi-language support
- [ ] Advanced reporting and export features
- [ ] API documentation and public API

---

**Built with ❤️ for better cities**

© 2024 CivicLink. All rights reserved.
