Web Application Security 

This repository contains a detailed report on Web Application Security, focusing on identifying, exploiting, and understanding common vulnerabilities using OWASP tools like WebGoat and OWASP ZAP.

Project Overview

This project explores real-world web application vulnerabilities in a safe, test environment. Using WebGoat (a vulnerable application) and OWASP ZAP (a security scanner), I practiced detecting and exploiting:

SQL Injection (SQLi)

Cross-Site Scripting (XSS)

Cross-Site Request Forgery (CSRF)

The goal was to learn how attacks work and how to protect applications from them.

Tools and Technologies Used

WebGoat

OWASP ZAP

Mozilla Firefox (with proxy configuration)

Manual penetration testing techniques

Setup and Configuration

Installing WebGoat:

Install Java JDK and verify using java -version

Download WebGoat .jar file from GitHub

Run it with: java -jar webgoat-2025.3.jar

Open: http://localhost:8080/WebGoat

Installing OWASP ZAP:

Download from https://www.zaproxy.org/download

Set proxy port to 8888 (to avoid conflict with WebGoat)

Configure Firefox to use proxy at 127.0.0.1:8888

Focus Areas for Vulnerability Identification

SQL Injection:

Injected payloads like ' OR '1'='1 into login fields to bypass authentication

XSS:

Inserted harmless scripts like <script>alert(1)</script> to test for input validation

CSRF:

Created fake forms to send unauthorized POST requests using active login sessions

Manual Exploitation Summary

SQL Injection:

Username: tom

Password: thisisasecretfortomonly

Login was bypassed using SQL injection techniques

XSS:

Payload: <script>alert("1")</script>

Demonstrated poor input sanitization

CSRF:

HTML form used to perform actions without the user’s consent

WebGoat allowed unauthorized requests due to missing CSRF tokens

Mitigation Measures

SQL Injection:

Use parameterized queries

Sanitize and validate all input

Limit database user permissions

XSS:

Escape and encode all outputs

Sanitize inputs before processing

Use Content Security Policy (CSP)

CSRF:

Implement CSRF tokens in all forms

Use SameSite cookie attributes

Require re-authentication for sensitive actions

Reflections

This task helped me understand the real impact of insecure code. Even simple web applications can be exposed to serious attacks if proper security measures are not followed. I learned how to simulate attacks, how they work technically, and how to apply security controls to prevent them. This project improved both my practical skills and understanding of ethical hacking and web security.

Included File

TASK 2 REPORT (REDYNOX).pdf – A complete PDF report including:

Setup and configuration steps

Testing screenshots

Payloads used

Manual exploitation walkthroughs

Security best practices and conclusions

Helpful References

OWASP WebGoat: https://owasp.org/www-project-webgoat
OWASP ZAP: https://owasp.org/www-project-zap
OWASP Top 10: https://owasp.org/www-project-top-ten
