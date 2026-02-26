# Bharat Bank

A full-stack banking platform built with Spring Boot and React, featuring account management, transactions, notifications, and secure JWT authentication.

## Tech Stack

**Backend:**
- Spring Boot 4.0.0-M3
- Java 21
- MySQL
- Spring Security + JWT
- AWS S3 (file storage)
- Spring Mail

**Frontend:**
- React 19
- React Router
- Axios

## Prerequisites

- Java 21 JDK
- Node.js and npm
- MySQL database
- AWS S3 account (for file storage)
- Gmail account (for email notifications)

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/heyiamantara/banking-platform-using-spring-boot.git
cd banking-platform-using-spring-boot
```

### 2. Backend Setup

Create a `.env` file in the `backend` directory:

```env
PORT=8090
PROD_DB_URL=jdbc:mysql://localhost:3306/bharatbank
PROD_DB_USERNAME=your_db_user
PROD_DB_PASSWORD=your_db_password
JWT_SECRET=your_jwt_secret_key_min_256_bits
JWT_EXPIRATION_TIME=86400000
MAIL_USER=your_gmail@gmail.com
MAIL_PASS=your_gmail_app_password
AWS_ACCESS_KEY=your_aws_access_key
AWS_SECRETE_KEY=your_aws_secret_key
AWS_BUCKET_NAME=your_s3_bucket_name
```

**Note:** For Gmail, you need to generate an [App Password](https://support.google.com/accounts/answer/185833).

### 3. Database Setup

Create the MySQL database:

```sql
CREATE DATABASE bharatbank;
```

The application will automatically create tables on first run.

### 4. Frontend Setup

Install dependencies:

```bash
cd frontend
npm install
```

## Running the Application

### Option 1: Local Development

**Terminal 1 - Backend:**
```bash
cd backend
./mvnw spring-boot:run
```

On Windows:
```bash
cd backend
mvnw.cmd spring-boot:run
```

**Terminal 2 - Frontend:**
```bash
cd frontend
npm start
```

- Backend: http://localhost:8090
- Frontend: http://localhost:3000

### Option 2: Docker

```bash
cd backend
docker compose up
```

Note: You'll still need to run the frontend separately with `npm start`.

## Project Structure

```
banking-platform-using-spring-boot/
├── backend/
│   ├── src/
│   │   └── main/
│   │       ├── java/com/bharat/bharatbank/
│   │       │   ├── account/          # Account management
│   │       │   ├── auth_users/       # Authentication & users
│   │       │   ├── audit_dashboard/  # Audit logs
│   │       │   ├── notification/     # Notifications
│   │       │   ├── transaction/      # Transactions
│   │       │   └── ...
│   │       └── resources/
│   ├── pom.xml
│   └── Dockerfile
└── frontend/
    ├── src/
    ├── package.json
    └── ...
```

## Features

- User registration and authentication
- Account management (multiple account types)
- Money transfers and transactions
- Transaction history
- Notifications system
- Audit dashboard
- Password reset functionality
- Secure JWT-based authentication

## License

[Add your license here]
