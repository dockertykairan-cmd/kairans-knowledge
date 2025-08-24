# QuizMaster Application

## Overview

QuizMaster is a modern, interactive web-based quiz application built with React and Express.js. The application provides a comprehensive quiz experience with features like timed questions, progress tracking, score calculation, and detailed results with performance feedback. The system uses a full-stack architecture with PostgreSQL for data persistence and includes both in-memory storage for development and database integration for production environments.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
The client-side is built using React 18 with TypeScript, implementing a modern component-based architecture. The application uses Wouter for lightweight client-side routing and React Query (TanStack Query) for efficient server state management and API communication. The UI is constructed using shadcn/ui components built on top of Radix UI primitives, providing accessible and customizable interface elements.

The frontend follows a modular structure with separate components for different quiz screens (welcome, quiz, results), hooks for state management, and utility functions. The application uses CSS-in-JS through Tailwind CSS for styling, with a comprehensive design system including custom color schemes, typography, and responsive design patterns.

### Backend Architecture
The server-side implements a RESTful API using Express.js with TypeScript. The architecture follows a layered approach with clear separation between routes, storage, and business logic. The application uses a storage abstraction pattern that allows switching between in-memory storage (for development) and database storage (for production) without changing the core application logic.

The API provides endpoints for fetching quiz questions, submitting quiz sessions, and managing quiz data. Error handling is implemented at the middleware level, providing consistent error responses across all endpoints.

### Data Management
The application uses Drizzle ORM for database operations with PostgreSQL as the primary database. The schema defines two main entities: quiz questions and quiz sessions. Quiz questions include multiple-choice options, correct answers, difficulty levels, categories, and optional images. Quiz sessions track user performance including scores, completion times, and answer statistics.

The system includes comprehensive data validation using Zod schemas, ensuring type safety across the full stack. Database migrations are managed through Drizzle Kit, providing version control for schema changes.

### State Management
Client-side state is managed through a combination of React hooks and React Query. The useQuiz hook encapsulates all quiz-related state logic including question navigation, answer selection, score calculation, and quiz completion. React Query handles server state caching, background refetching, and optimistic updates for a smooth user experience.

### UI/UX Design
The interface implements a modern design system with consistent spacing, typography, and color schemes. The application includes interactive elements like progress indicators, timers, confetti animations for celebrations, and responsive layouts that work across desktop and mobile devices. The design emphasizes accessibility with proper ARIA labels, keyboard navigation, and screen reader support.

## External Dependencies

### Core Framework Dependencies
- **React 18**: Frontend framework with hooks and concurrent features
- **Express.js**: Backend web application framework
- **TypeScript**: Type safety across the full stack
- **Vite**: Frontend build tool and development server

### Database and ORM
- **PostgreSQL**: Primary database (via @neondatabase/serverless for cloud deployment)
- **Drizzle ORM**: Type-safe database toolkit with schema migrations
- **Drizzle Kit**: Database migration and introspection tools

### UI and Styling
- **Tailwind CSS**: Utility-first CSS framework
- **shadcn/ui**: Component library built on Radix UI primitives
- **Radix UI**: Unstyled, accessible UI components
- **Lucide React**: Icon library for consistent iconography
- **Class Variance Authority**: Utility for creating component variants

### State Management and Data Fetching
- **TanStack React Query**: Server state management and caching
- **React Hook Form**: Form handling with validation
- **Zod**: Schema validation and type inference
- **Wouter**: Lightweight client-side routing

### Development and Build Tools
- **ESBuild**: Fast JavaScript bundler for production builds
- **PostCSS**: CSS processing with Autoprefixer
- **TSX**: TypeScript execution for development server
- **Replit Integration**: Development environment plugins and error handling

### Additional Libraries
- **Date-fns**: Date manipulation and formatting
- **Nanoid**: Unique ID generation
- **CMDK**: Command palette interface component
- **Embla Carousel**: Touch-friendly carousel component