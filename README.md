# AI Phone Scheduler Frontend

A professional React frontend for the AI Phone Scheduler SaaS platform. This frontend provides a modern, responsive interface for managing tenants, appointments, and user authentication.

## Features

- **Authentication**: Complete user registration, login, and session management
- **Dashboard**: Overview of tenants, appointments, and key metrics
- **Tenant Management**: Create, view, and configure business tenants
- **Appointment Management**: View, create, and manage appointments
- **Responsive Design**: Mobile-first design with Tailwind CSS
- **Professional UI**: Modern, clean interface with smooth animations

## Tech Stack

- **React 18**: Modern React with hooks
- **React Router**: Client-side routing
- **Tailwind CSS**: Utility-first CSS framework
- **Axios**: HTTP client for API communication
- **Lucide React**: Beautiful icon library
- **React Hook Form**: Form handling and validation

## Getting Started

### Prerequisites

- Node.js 16+ 
- npm or yarn
- Backend API running on `http://localhost:8000`

### Installation

1. Navigate to the frontend directory:
```bash
cd frontend
```

2. Install dependencies:
```bash
npm install
```

3. Create environment file:
```bash
cp .env.example .env
```

4. Configure environment variables in `.env`:
```env
REACT_APP_API_URL=http://localhost:8000
```

5. Start the development server:
```bash
npm start
```

The app will open at `http://localhost:3000`

## Available Scripts

- `npm start`: Start development server
- `npm build`: Build for production
- `npm test`: Run tests
- `npm run eject`: Eject from Create React App

## Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── Auth/           # Authentication components
│   ├── Dashboard/      # Dashboard components
│   ├── Tenants/        # Tenant management components
│   ├── Appointments/   # Appointment components
│   └── Layout/         # Layout components
├── contexts/           # React contexts
├── services/           # API services
└── App.js             # Main application component
```

## API Integration

The frontend integrates with the following backend endpoints:

### Authentication
- `POST /api/v1/auth/register` - User registration
- `POST /api/v1/auth/login` - User login
- `POST /api/v1/auth/logout` - User logout
- `GET /api/v1/auth/me` - Get current user

### Tenants
- `GET /api/v1/tenants` - List tenants
- `POST /api/v1/tenants` - Create tenant
- `GET /api/v1/tenants/{id}` - Get tenant
- `PUT /api/v1/tenants/{id}` - Update tenant

### Appointments
- `GET /api/v1/appointments/tenant/{id}` - List appointments
- `POST /api/v1/appointments` - Create appointment
- `GET /api/v1/appointments/{id}` - Get appointment
- `PUT /api/v1/appointments/{id}/status` - Update status

## Styling

The project uses Tailwind CSS for styling with custom configurations:

- **Colors**: Custom primary and secondary color palettes
- **Typography**: Inter font family
- **Animations**: Custom fade-in, slide-in, and bounce animations
- **Shadows**: Soft, medium, and large shadow variants
- **Responsive**: Mobile-first responsive design

## Authentication Flow

1. User registers/logs in through the auth forms
2. JWT tokens are stored in localStorage
3. API requests include Authorization headers
4. Token refresh is handled automatically
5. Protected routes redirect to login if not authenticated

## Key Components

### Dashboard
- Overview statistics (tenants, appointments, upcoming)
- Recent appointments list
- Quick actions and navigation

### Tenant Management
- List view with status indicators
- Create new tenant form
- Tenant configuration (business info, agent settings, Twilio integration)

### Appointment Management
- Filterable appointment list
- Status-based filtering
- Search functionality
- Appointment details view

## Contributing

1. Follow the existing code style and patterns
2. Use TypeScript for type safety
3. Write meaningful component and function names
4. Add proper error handling
5. Test components thoroughly

## License

This project is part of the AI Phone Scheduler SaaS platform.
