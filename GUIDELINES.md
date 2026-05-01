# Service Layer and Repository Pattern

## Goal
Separation of businesslogic and access of data, for clean, testable and scalable code.

## Definitions
### Service Layer
- Includes all businesslogic functions such as create tickets, change status and delegations.
- Communication between API and Repository.
- Does not know any information stored in database

### Repository Pattern
- Encapsulate Access to Database: Entity based CRUD-Operations
- Defines a clear Interface for services
- Doesn't have any businesslogic. Only Access, Queries, Filters, Joins and Transactions.

### Achievements
- Testable: Services can be tested utiilizing mock-repositories
- Maintaneable: Any change made only does so through repositories, services remain untouched.
- Transparency: Developers are able to see the businesslogic and where persistencies can be implemented.
