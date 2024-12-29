# Uber Clone

A full-stack Uber recreation built with React, Next.js, Firebase, styled-components, Tailwind, and Mapbox.

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14.0.0 or later)
- npm (v6.0.0 or later)
- Git

## Detailed Setup Instructions

### 1. Clone and Setup
```bash
# Clone the repository
git clone git@github.com:DevlinRocha/uber-clone.git

# Navigate to project directory
cd uber-clone

# Install dependencies
npm install
```

### 2. Environment Setup
1. Create a `.env.local` file in the root directory
2. Add the following environment variables:
```env
NEXT_PUBLIC_MAPBOX_ACCESS_TOKEN=your_mapbox_token
NEXT_PUBLIC_FIREBASE_API_KEY=your_firebase_api_key
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
NEXT_PUBLIC_FIREBASE_PROJECT_ID=your_firebase_project_id
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=your_storage_bucket
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
NEXT_PUBLIC_FIREBASE_APP_ID=your_app_id
```

### 3. Firebase Setup
1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project
3. Enable Authentication:
   - Go to Authentication > Sign-in method
   - Enable Email/Password and Google Sign-in
4. Create Firestore Database:
   - Go to Firestore Database
   - Create database in test mode
   - Choose a location closest to your users

### 4. Mapbox Setup
1. Create an account at [Mapbox](https://www.mapbox.com/)
2. Navigate to Account > Access tokens
3. Create a new token with the following scopes:
   - map:read
   - map:write
   - geocoding:read
4. Copy the token to your `.env.local` file

### 5. Running the Application
```bash
# Start development server
npm run dev
```
The application will be available at [http://localhost:3000](http://localhost:3000)

### 6. Project Structure
```
uber-clone/
├── components/     # React components
├── pages/         # Next.js pages
├── public/        # Static files
├── styles/        # CSS and styling files
├── utils/         # Utility functions
└── firebase/      # Firebase configuration
```

## Features
- 🗺️ Real-time map integration with Mapbox
- 🔐 User authentication with Firebase
- 📱 Responsive design for mobile and desktop
- 🚗 Real-time ride tracking
- 💰 Price estimation
- 📍 Location search and autocomplete

## Development Stack

### Frontend
- **React**: UI library for building user interfaces
- **Next.js**: React framework for production-grade applications
- **styled-components**: CSS-in-JS styling solution
- **Tailwind CSS**: Utility-first CSS framework

### Backend & Services
- **Firebase**
  - Authentication
  - Firestore Database
  - Real-time updates
- **Mapbox**
  - Maps rendering
  - Geocoding
  - Navigation

## Common Issues and Solutions

### Map Not Loading
- Verify Mapbox token is correctly set in `.env.local`
- Check console for CORS errors
- Ensure proper map initialization in components

### Authentication Issues
- Verify Firebase configuration
- Enable required authentication methods in Firebase Console
- Check for proper initialization of Firebase Auth

## Deployment

### Vercel Deployment
1. Connect your GitHub repository to Vercel
2. Add environment variables in Vercel dashboard
3. Deploy using Vercel's default settings

### Manual Deployment
```bash
# Build the application
npm run build

# Start production server
npm start
```

## Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Troubleshooting

If you encounter any issues:
1. Check console for error messages
2. Verify all environment variables are set correctly
3. Ensure all dependencies are installed (`npm install`)
4. Clear browser cache and local storage
5. Restart the development server

## Support
For support, please:
- Open an issue on GitHub
- Check existing issues for solutions
- Review the documentation

## License
This project is licensed under the MIT License - see the LICENSE file for details