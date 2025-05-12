# Library Management System Database

## Project Description
This is a comprehensive Library Management System database designed using MySQL. The system manages books, members, loans, reservations, and fines in a library setting. It includes proper relationships, constraints, and indexes for optimal performance.

## Features
- Member management with contact information and membership status
- Book catalog with ISBN, title, publisher, and edition information
- Author and publisher management
- Category-based book organization
- Loan tracking system
- Reservation system
- Fine management
- Performance-optimized with appropriate indexes

## Database Structure
The database consists of the following main tables:
- `members`: Stores library member information
- `books`: Contains book details and inventory
- `authors`: Author information
- `publishers`: Publisher details
- `categories`: Book categories/genres
- `loans`: Book loan records
- `reservations`: Book reservation records
- `fines`: Fine records for overdue books

## Relationships
- Books can have multiple authors (Many-to-Many)
- Books can belong to multiple categories (Many-to-Many)
- Books belong to one publisher (Many-to-One)
- Members can have multiple loans (One-to-Many)
- Loans can have multiple fines (One-to-Many)

## Setup Instructions
1. Install MySQL Server (version 5.7 or higher)
2. Open MySQL command line or MySQL Workbench
3. Run the `library_management.sql` script:
   ```sql
   source path/to/library_management.sql
   ```

## ERD (Entity Relationship Diagram)
The database structure can be visualized as follows:

```
[Members] 1----* [Loans] *----1 [Books]
[Books] *----* [Authors]
[Books] *----* [Categories]
[Books] *----1 [Publishers]
[Loans] 1----* [Fines]
[Books] 1----* [Reservations] *----1 [Members]
```

## Constraints and Features
- Primary Keys on all tables
- Foreign Key constraints with appropriate ON DELETE actions
- NOT NULL constraints on required fields
- UNIQUE constraints on ISBN and email
- ENUM types for status fields
- Automatic timestamp management
- Indexed fields for better query performance

## Author
Gerald
