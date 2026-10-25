# Expense Tracker — Architecture

## 1. Architecture Overview

The application will use a frontend-backend architecture.

- **Frontend:** ReactJS
- **Backend:** Java with Spring Boot
- **Build tool:** Maven
- **API style:** REST APIs
- **Database access:** MyBatis with XML mapper files
- **Database:** SQL relational database (to be decided)
- **API testing:** Postman

## 2. Request Flow

During normal application use:

1. The user performs an action in the React frontend.
2. The frontend sends an HTTP request to a Spring Boot REST API.
3. The controller receives the request.
4. The service layer applies the business rules.
5. The MyBatis mapper executes the required SQL query.
6. The database stores or retrieves the data.
7. The result returns through the service and controller.
8. The API sends an HTTP response to the frontend.

## 3. Backend Responsibilities

### Controller Layer
- Expose REST endpoints.
- Receive requests and return HTTP responses.

### Service Layer
- Apply transaction and account business rules.
- Validate that an account exists before creating a transaction.
- Calculate the effects of credits and debits on account balances.
- Calculate dashboard totals for the selected time period.

### MyBatis Mapper Layer
- Connect service logic to SQL queries.
- Use XML mapper files to define SQL statements and result mappings.

### Database Layer
- Store account and transaction information.
- Maintain the relationships between accounts and transactions.

## 4. Development Workflow

1. Finalize requirements and architecture.
2. Design database tables and relationships.
3. Create the Spring Boot project using Maven.
4. Implement backend features and REST APIs.
5. Test the APIs using Postman.
6. Build the React frontend.
7. Integrate and test the complete application.

## 5. Current Scope

The first version focuses on:
- Home dashboard
- New transaction creation
- Total spending by selected period
- Combined account balance
- Account creation
- Transaction history with running balances

The application will initially support a single user. Additional account and tracker-table requirements will be documented when finalized.

## 6. Decisions Still Pending

- SQL database selection
- Database tables and relationships
- API endpoints and request/response formats
- Detailed balance and transaction-handling rules
- Project package structure
