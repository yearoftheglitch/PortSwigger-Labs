# Lab 3: SQL Injection UNION Attack, Determining the Number of Columns

* **Solution**: Use ORDER BY to increment column indices until an error occurs, revealing the column count (3 here).
* **Final Payload**: category=Gifts' ORDER BY 3 -- (errors at 4)