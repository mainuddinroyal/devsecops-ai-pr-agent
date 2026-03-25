# 🔐 DevSecOps AI PR Security Agent

## 🎯 Problem

Code reviews often miss security vulnerabilities due to time constraints and lack of expertise. This leads to insecure code being merged into production.

---

## 💡 Solution

An AI-powered DevSecOps agent that automatically analyzes GitHub Pull Requests, detects security issues, and posts structured feedback before code is merged.

---

## ⚡ What It Does

- Triggers automatically on Pull Requests  
- Fetches changed files using GitHub API  
- Filters relevant source code files  
- Uses AI to detect security vulnerabilities (OWASP-focused)  
- Generates structured findings (Severity, Issue, Fix)  
- Posts automated comments directly on the PR  

---

## 🏗 Architecture

- **n8n** → Workflow orchestration  
- **GitHub API** → PR data & comments  
- **OpenAI API** → Security analysis  

---

## 🔄 Workflow

1. Pull Request is created  
2. GitHub webhook triggers n8n  
3. Changed files are fetched  
4. Code files are filtered (.js, .ts, .java, .py)  
5. Each file is analyzed using AI  
6. Results are aggregated  
7. Security report is posted on the PR  

---

## 🧪 Example Output

```
## 🔐 Security Report

Total Files: 3

---

HIGH - SQL Injection vulnerability  
Fix: Use prepared statements  

---

MEDIUM - Missing input validation  
Fix: Validate user inputs  

---

LOW - Logging sensitive data  
Fix: Remove sensitive logs  
```

---

## ⚙️ Setup

Follow the detailed setup guide:

👉 `docs/setup.md`

---

## 📸 Demo

(Add screenshot of PR comment here)

---

## 🚀 Impact

- Detects security issues early in the PR stage  
- Reduces manual code review effort  
- Prevents vulnerabilities before merge  
- Improves overall code quality automatically  

---

## 📊 Status

- Production-ready (basic level)  
- End-to-end workflow functional  

---

## 👨‍💻 Author

Built as a real-world DevSecOps + AI automation project