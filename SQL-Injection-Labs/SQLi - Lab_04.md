# Lab 4: SQL Injection UNION Attack, Retrieving Data from Other Tables

* **Solution**: After confirming 3 columns with NULLs, inject a UNION query to fetch usernames and passwords, placing data in string-compatible columns.
* **Final Payload**: category=Gifts' UNION SELECT NULL, username, password FROM users --
