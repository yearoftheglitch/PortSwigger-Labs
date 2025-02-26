# Lab 2: SQL Injection Vulnerability Allowing Login Bypass

* **Solution**: Inject a payload into the username field to force a true condition, bypassing password verification.
* **Final Payload**: username=administrator' -- (submit with any password)