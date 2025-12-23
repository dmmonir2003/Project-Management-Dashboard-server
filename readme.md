# Project Management Backend

A robust, scalable backend API for comprehensive project management systems, designed to handle property development projects from inception to completion. Built with modern technologies and best practices to ensure reliability, security, and maintainability.

## 🚀 Features

### Core Functionality

- **User Authentication & Authorization**: Secure JWT-based authentication with role-based access control
- **Project Management**: Full lifecycle management of property development projects
- **Document Management**: Hierarchical document organization with file upload capabilities
- **Financial Tracking**: Comprehensive expense tracking for labor, materials, and subcontractors
- **Real-time Notifications**: Socket.io-powered real-time updates and notifications
- **Payment Integration**: Stripe integration for secure payment processing
- **Analytics Dashboard**: Business intelligence and reporting capabilities
- **Certificate Management**: Digital certificate handling and validation
- **Contact Management**: Stakeholder and contact information management
- **Time Scheduling**: Project timeline and milestone tracking

### Advanced Features

- **File Upload**: AWS S3 integration for secure cloud storage
- **Email Services**: Automated email notifications and communications
- **Error Handling**: Comprehensive error management with custom error types
- **Data Validation**: Zod schema validation for type-safe API endpoints
- **Load Balancing Ready**: Containerized deployment with Docker
- **Performance Monitoring**: Built-in analytics and performance tracking

## 🛠 Tech Stack

### Backend Framework

- **Node.js** - Runtime environment
- **TypeScript** - Type-safe development
- **Express.js** - Web application framework

### Database & Storage

- **MongoDB** - NoSQL database with Mongoose ODM
- **AWS S3** - Cloud file storage
- **Multer** - File upload handling

### Authentication & Security

- **JWT** - JSON Web Tokens for authentication
- **bcrypt** - Password hashing
- **Helmet** - Security headers
- **CORS** - Cross-origin resource sharing

### Real-time & Communication

- **Socket.io** - Real-time bidirectional communication
- **Nodemailer** - Email service integration

### Payment & External Services

- **Stripe** - Payment processing
- **Axios** - HTTP client for external API calls

### Development Tools

- **ESLint** - Code linting
- **Prettier** - Code formatting
- **TSX** - TypeScript execution and REPL
- **Docker** - Containerization

## 📁 Project Structure

```
src/
├── app.ts                 # Main application setup
├── server.ts              # Server initialization
├── app/
│   ├── builder/           # Query builder utilities
│   ├── config/            # Configuration files
│   ├── DB/                # Database connection
│   ├── errors/            # Custom error handlers
│   ├── interface/         # TypeScript interfaces
│   ├── middlewares/       # Express middlewares
│   └── modules/           # Business logic modules
│       ├── AboutUs/       # About page management
│       ├── Analytic/      # Analytics and reporting
│       ├── Auth/          # Authentication module
│       ├── Certificate/   # Certificate management
│       ├── Contact/       # Contact management
│       ├── Document/      # Document management
│       ├── Handover/      # Project handover
│       ├── Labour/        # Labor management
│       ├── PaymentTracker/# Payment tracking
│       ├── Project/       # Core project management
│       ├── User/          # User management
│       └── ...            # Additional modules
├── routes/                # API route definitions
└── utils/                 # Utility functions
```

## 🏗 Architecture

### Modular Design

- **Separation of Concerns**: Each module encapsulates its own business logic, routes, validation, and database models
- **Middleware Layer**: Centralized authentication, validation, and error handling
- **Service Layer**: Business logic abstraction for maintainability

### Security Architecture

- **JWT Authentication**: Stateless authentication with refresh token support
- **Role-Based Access Control**: Granular permissions system
- **Input Validation**: Comprehensive validation using Zod schemas
- **Error Sanitization**: Secure error responses without sensitive information

### Scalability Features

- **Containerization**: Docker support for consistent deployment
- **Database Optimization**: Efficient queries with Mongoose indexing
- **Caching Ready**: Architecture prepared for Redis integration
- **Load Balancing**: Stateless design supports horizontal scaling

## 🚀 Getting Started

### Prerequisites

- Node.js (v18 or higher)
- MongoDB (local or cloud instance)
- Docker (optional, for containerized deployment)
- AWS S3 credentials (for file uploads)

### Installation

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd project-management-backend-simone
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Environment Setup**
   Create a `.env` file in the root directory:

   ```env
   NODE_ENV=development
   PORT=5000
   DATABASE_URL=mongodb://localhost:27017/project-management
   JWT_SECRET=your-jwt-secret
   JWT_EXPIRES_IN=7d
   AWS_ACCESS_KEY_ID=your-aws-access-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret-key
   AWS_REGION=your-aws-region
   AWS_S3_BUCKET=your-s3-bucket
   STRIPE_SECRET_KEY=your-stripe-secret-key
   EMAIL_USER=your-email@example.com
   EMAIL_PASS=your-email-password
   ```

4. **Database Setup**
   Ensure MongoDB is running locally or update `DATABASE_URL` for cloud instance.

### Running the Application

#### Development Mode

```bash
npm run dev
```

#### Production Build

```bash
npm run build
npm start
```

#### Docker Deployment

```bash
docker-compose up --build
```

## 📡 API Documentation

### Postman Collection

Import the provided Postman collection for comprehensive API testing:

- [Project-Management.postman_collection.json](./Project-Management.postman_collection.json)

### Key Endpoints

- `POST /api/auth/login` - User authentication
- `GET /api/projects` - Retrieve projects
- `POST /api/projects` - Create new project
- `GET /api/analytics` - Get analytics data
- `POST /api/upload` - File upload to S3

### API Features

- RESTful design principles
- JSON response format
- Comprehensive error handling
- Rate limiting ready
- API versioning support

## 🧪 Testing & Quality Assurance

### Code Quality

```bash
# Linting
npm run lint

# Code formatting
npm run prettier

# Type checking
npm run build
```

### Load Testing

The project includes load testing configuration:

- [load-test.yml](./load-test.yml) - K6 load testing scripts

### Performance Monitoring

- Built-in analytics module for tracking API performance
- Error logging and monitoring capabilities
- Database query optimization

## 🚀 Deployment

### Vercel Deployment

The project is configured for Vercel deployment:

- [vercel.json](./vercel.json) - Deployment configuration

### Docker Deployment

```bash
# Build and run with Docker Compose
docker-compose up -d

# View logs
docker-compose logs -f
```

### Environment Variables

Ensure all environment variables are set in your deployment platform.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines

- Follow TypeScript best practices
- Write comprehensive tests for new features
- Maintain code coverage above 80%
- Use conventional commit messages
- Run linting and formatting before commits

A property development project involves planning, designing, and constructing residential, commercial, or industrial properties to create value and meet market demands. It encompasses land acquisition, regulatory approvals, construction, and final sale or leasing of the developed property.

**Built with ❤️ for efficient project management**
