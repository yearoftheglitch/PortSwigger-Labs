# Lab 1: SQL Injection Vulnerability in WHERE Clause Allowing Retrieval of Hidden Data

* **Solution**: Modify the category parameter to include unreleased products by appending a condition that always evaluates true.
* **Final Payload**: category=Gifts' OR 1=1 --