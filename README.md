# Modern Notes App

![Status](https://img.shields.io/badge/Status-Live-brightgreen)
![React](https://img.shields.io/badge/React-18-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)
![Vite](https://img.shields.io/badge/Vite-4.0-yellow)
![AWS](https://img.shields.io/badge/AWS-Amplify-orange)

## 📝 Overview

Modern Notes App is a feature-rich note-taking application built with React, TypeScript, and Vite, fully deployed on AWS infrastructure. The app provides a seamless, intuitive interface for creating, organizing, and managing notes with real-time synchronization across devices.

## ✨ Features

- **User Authentication**: Secure sign-up, login, and account management
- **Real-time Sync**: Notes automatically sync across all devices
- **Rich Text Editing**: Format text with bold, italic, lists, headings, and more
- **Organization Tools**: Tags, folders, and search functionality
- **Offline Support**: Create and edit notes even without internet connection
- **Dark/Light Mode**: Toggle between themes for comfortable viewing
- **Responsive Design**: Optimized for both desktop and mobile experiences
- **Cloud Storage**: All notes securely stored in the cloud
- **Collaboration**: Share notes with other users (optional permissions)
- **Version History**: Track changes and restore previous versions

## 🛠️ Tech Stack

### Frontend
- **React 18** with **Vite** for an optimized development experience
- **TypeScript** for type safety and improved developer experience
- **React Router** for client-side routing
- **Zustand/Redux** for state management
- **React Query** for efficient data fetching
- **TailwindCSS/Styled Components** for styling
- **React Testing Library** for component testing

### Backend & Infrastructure
- **AWS Amplify** for authentication, API, storage, and hosting
- **GraphQL API** using AWS AppSync
- **DynamoDB** for data persistence
- **S3** for file storage
- **Lambda** for serverless functions
- **Cognito** for user authentication

## 🚀 Deployment

The application is fully deployed on AWS using the Amplify platform, which provides a scalable and reliable environment with CI/CD capabilities.

**Live URL**: [modern-notes-app.example.com](https://modern-notes-app.example.com)

## 📷 Screenshots

![Homepage](/assets/homepage.png)
![Note Editor](/assets/editor.png)
![Mobile View](/assets/mobile.png)

## 🏗️ Architecture

```
┌────────────────┐       ┌───────────────────┐       ┌─────────────────┐
│                │       │                   │       │                 │
│  React App     │──────▶│  AWS AppSync      │──────▶│  AWS Lambda     │
│                │       │  (GraphQL API)    │       │                 │
└────────────────┘       └───────────────────┘       └────────┬────────┘
        │                                                     │
        │                                                     ▼
        │                ┌───────────────────┐       ┌─────────────────┐
        │                │                   │       │                 │
        └───────────────▶│  AWS Cognito      │       │  AWS DynamoDB   │
                         │  (Authentication) │       │                 │
                         └───────────────────┘       └─────────────────┘
```

### Key Implementation Details

#### Data Model
The application uses a GraphQL API with the following main models:
- User
- Note
- Folder
- Tag

#### Authentication Flow
AWS Cognito handles the authentication process with features like:
- Email/password authentication
- Social login options
- Multi-factor authentication
- Password reset flows

#### Offline Support
The app implements offline support using:
- IndexedDB for local storage
- Sync queue for changes made offline
- Conflict resolution strategies

## 🧪 Testing

Run tests using the following command:
```bash
npm test
# or
yarn test
```

## 📱 Mobile Support

The app is fully responsive and works well on mobile devices. Key mobile features include:
- Touch-friendly UI components
- Swipe gestures for common actions
- Optimized layout for small screens
- Mobile-specific UX considerations

## 🔒 Security Features

- Secure user authentication with AWS Cognito
- HTTPS for all communications
- Data encryption at rest and in transit
- Role-based access control
- Input validation and sanitization

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- AWS for their comprehensive cloud infrastructure
- The React and TypeScript communities for excellent tools and documentation
- Open-source libraries that made this project possible
