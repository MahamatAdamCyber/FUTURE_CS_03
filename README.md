# 🔐 API Security Risk Analysis

## 📌 Project Overview

This repository contains an API Security Risk Analysis conducted on a public testing API.

The objective of this assessment was to analyze how APIs expose data and identify common security risks such as missing authentication, excessive data exposure, and lack of security protections.

This project was completed as part of my cybersecurity learning and hands-on practice in API security testing.

---

# 🎯 Target API

Public Testing API

Base URL:

https://jsonplaceholder.typicode.com

Example endpoints tested:

/users  
/users/2  
/users/7

---

# 🎯 Scope of Assessment

The analysis focused on publicly accessible API endpoints.

The following activities were performed:

API request testing  
Response data analysis  
HTTP header inspection  
Authentication verification  
Rate limiting observation  

The following activities were not performed:

Exploitation of vulnerabilities  
Denial of Service (DoS) testing  
Authentication bypass attacks  
Automated aggressive scanning  

---

# 🛠 Tools Used

The API analysis was conducted using the following tools:

Postman – used to send API requests and inspect responses

 Browser DevTools – used to inspect HTTP headers and network responses

GitHub – used to document and share the project

---

# 🔎 Assessment Methodology

The security analysis followed these steps:

1. Identify available API endpoints
2. Send requests using Postman
3. Inspect API responses and returned data
4. Analyze HTTP response headers
5. Evaluate authentication mechanisms
6. Observe potential rate limiting behavior
7. Document findings and security risks

The methodology follows general principles inspired by the OWASP API Security Top 10.

---

# 📊 Summary of Findings

The analysis identified several security weaknesses related to access control, data exposure, and missing protections.

Severity Level | Number of Findings
---------------|------------------
🟠 Medium | 3
🟡 Low | 2

These issues demonstrate common API security risks that may increase the attack surface of an application.

---

# 🚨 Key Security Issues Identified

### Open API Endpoint

The `/users` endpoint was accessible without any authentication mechanism such as API keys or tokens.

This could allow unauthorized users to retrieve information from the API.

---

### Broken Object Level Authorization (BOLA)

Different user records could be accessed by simply modifying the ID in the request URL.

Example:

/users/2  
/users/7  

This behavior could allow attackers to access other users’ data.

---

### Excessive Data Exposure

The API responses include multiple user information fields such as:

email  
phone  
address  
company  

Returning unnecessary data increases privacy and security risks.

---

### Missing Security Headers

Several common HTTP security headers were not observed in the API responses.

Examples include:

Content-Security-Policy  
X-Frame-Options  
X-Content-Type-Options  
Strict-Transport-Security  

---

### Missing Rate Limiting

The API allowed multiple requests in a short time period without restricting the request frequency.

This could allow abuse or automated scraping.

---

# 🛡 Security Recommendations

To improve API security, the following measures are recommended:

### Implement Authentication

Require API authentication mechanisms such as:

API keys  
OAuth tokens  

---

### Enforce Access Control

Ensure users can only access their own resources to prevent Broken Object Level Authorization vulnerabilities.

---

### Reduce Data Exposure

Return only the necessary data fields required by the client application.

---

### Add Security Headers

Implement recommended HTTP security headers:

Content-Security-Policy  
X-Frame-Options  
X-Content-Type-Options  
Strict-Transport-Security  

---

### Apply Rate Limiting

Limit the number of requests per user or IP address to prevent API abuse.

---

# 📄 Full Report

The complete API security analysis report is available in this repository as a PDF document.

The report includes:

detailed vulnerability explanations  
evidence screenshots  
risk classification  
security recommendations  

---

# ⚖️ Ethical Notice

This security assessment was conducted:

For educational purposes  
Using a public testing API  
Without exploiting vulnerabilities  

No harmful actions were performed during the analysis.

---

# 👤 Author

Mahamat ADAM ADAM 
