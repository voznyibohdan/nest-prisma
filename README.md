# NestJS with Prisma Application

A NestJS application using PostgreSQL database.

## Prerequisites

Before you begin, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (LTS version recommended)
- [npm](https://www.npmjs.com/) (comes with Node.js)
- [Docker](https://www.docker.com/get-started/) and Docker Compose

## Environment Setup

1. Create a `.env` file in the root directory with the following variables:

```env
POSTGRES_USER=your_username
POSTGRES_PASSWORD=your_password
POSTGRES_DB=your_database_name
PGADMIN_DEFAULT_EMAIL=your_email@example.com
PGADMIN_DEFAULT_PASSWORD=your_pgadmin_password
DATABASE_URL="postgresql://johndoe:randompassword@localhost:5432/mydb?schema=public"
```

## Database Setup

1. Start the PostgreSQL database and pgAdmin using Docker Compose:

```bash
docker-compose up -d
```

This will start:

- PostgreSQL database on port 5432
- pgAdmin interface accessible at `http://localhost:15433`

### Database Connection Details

- **Host**: localhost
- **Port**: 5432
- **Database**: as specified in POSTGRES_DB
- **Username**: as specified in POSTGRES_USER
- **Password**: as specified in POSTGRES_PASSWORD

### pgAdmin Access

- Access pgAdmin at: `http://localhost:15433`
- Login using the credentials specified in:
    - PGADMIN_DEFAULT_EMAIL
    - PGADMIN_DEFAULT_PASSWORD

## Project Setup

1. Install dependencies:

```bash
npm install
```

2. Run database migrations (if any):

```bash
npx prisma migrate dev
```

## Running the Application

```bash
# Development mode
npm run start

# Watch mode (recommended for development)
npm run start:dev

# Production mode
npm run start:prod
```

## Testing

```bash
# Unit tests
npm run test

# E2E tests
npm run test:e2e

# Test coverage
npm run test:cov
```

## Development Tools

- Format code:

```bash
npm run format
```

- Lint code:

```bash
npm run lint
```
