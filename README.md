# Interview task

**Requirements:**

Create a service that provides an API to solve the following problem: select the user with the second highest salary from the SQL database tables below.

`users` table

| id | name | salary_id |
| --- | --- | --- |
| 1 | John | 1 |
| 2 | Bob | 2 |
| 3 | Sara | 3 |
| 4 | Chris | 4 |

`salary` table

| id | salary |
| --- | --- |
| 1 | 4000 |
| 2 | 3500 |
| 3 | 5000 |
| 4 | 4200 |

**Example of usage:**

When making an HTTP request GET [`http://localhost:5000/users/salary`](http://localhost:5000/users/salary), the following response should be returned (if the data has the same form as in the tables above):

```json
{
  "id": 4,
  "name": "Chris",
  "salary": {
    "id": 4
  }
}
```

To solve the problem, you can use any web-framework (express, koa, apollo-graphql, etc.) and any SQL DB (for example sqlite).

**It will be a plus if:**

- the architecture of the service will allow it to be easily extended in the future and allow you to quickly add new API methods
- code will be covered by tests (unit, functional, integration)
- the service will be able to search in a table with 100,000 entries.

