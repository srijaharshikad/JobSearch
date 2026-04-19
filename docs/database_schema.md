# Database Schema

## Users Table
- **user_id**: INT (Primary Key)
- **name**: VARCHAR(100)
- **email**: VARCHAR(100, Unique)
- **password**: VARCHAR(255)
- **created_at**: TIMESTAMP
- **updated_at**: TIMESTAMP

## JobPostings Table
- **job_id**: INT (Primary Key)
- **title**: VARCHAR(200)
- **description**: TEXT
- **company_id**: INT (Foreign Key)
- **location**: VARCHAR(100)
- **date_posted**: DATE
- **created_at**: TIMESTAMP
- **updated_at**: TIMESTAMP

## Companies Table
- **company_id**: INT (Primary Key)
- **name**: VARCHAR(100)
- **industry**: VARCHAR(100)
- **website**: VARCHAR(100)
- **created_at**: TIMESTAMP
- **updated_at**: TIMESTAMP

## Applications Table
- **application_id**: INT (Primary Key)
- **user_id**: INT (Foreign Key)
- **job_id**: INT (Foreign Key)
- **status**: ENUM('applied', 'interviewing', 'offered', 'rejected')
- **date_applied**: DATE
- **created_at**: TIMESTAMP
- **updated_at**: TIMESTAMP