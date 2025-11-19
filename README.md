# School Dashboard

A modern school management dashboard application built with Next.js.

> **Note**: This project consists primarily of the frontend implementation with a partial backend integration using Prisma and PostgreSQL. The backend logic is currently a work in progress.

## Features

- **Role-based Access**: Different views for Admins, Teachers, Students, and Parents.
- **Dashboard Overview**: Visualizations for attendance, finance, and gender distribution.
- **Management Lists**: CRUD interfaces for Students, Teachers, Parents, Subjects, Classes, Lessons, Exams, Assignments, and more.
- **Calendar Integration**: Event and schedule management.

## Tech Stack

- **Frontend**: Next.js 15, React 19, Tailwind CSS
- **Backend/Database**: Prisma ORM, PostgreSQL
- **UI Components**: Recharts, FullCalendar, React Hook Form

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- PostgreSQL database (or a Prisma Postgres instance)

### Installation

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure environment variables:
   Create a `.env` file in the `frontend` directory and add your database connection string:
   ```env
   DATABASE_URL="postgresql://user:password@localhost:5432/school_dashboard?schema=public"
   ```

### Database Setup

1. Run migrations to create the database schema:
   ```bash
   npx prisma migrate dev
   ```

2. Seed the database with initial data:
   ```bash
   npx prisma db seed
   ```

### Running the Application

Start the development server:

```bash
npm run dev
```

Open [http://localhost:3000/admin](http://localhost:3000/admin) with your browser to see the basic result.

## Project Structure

- `src/app`: Next.js App Router pages and layouts.
- `src/components`: Reusable UI components.
- `src/lib`: Utility functions and Prisma client instance.
- `prisma`: Database schema and seed scripts.
- `public`: Static assets.
