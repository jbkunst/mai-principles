# SQL

Reusable preferences for SQL work. These notes adapt the general mAI principles to SQL and should remain small.

## Explain the query before the query

Start every substantive SQL query or query block with a short comment immediately above it describing its purpose.

Prefer comments that explain the business intent, transformation, or result being produced rather than restating SQL syntax.

```sql
-- Calculate monthly default rate by origination cohort
SELECT
  ...
```

Keep the comment concise enough to scan quickly. Its purpose is to make a query understandable before reading the implementation.
