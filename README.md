# 🔐 DevSecOps AI PR Security Agent

## 🚀 Overview
An AI-powered DevSecOps agent that automatically analyzes GitHub Pull Requests for security vulnerabilities and posts structured feedback directly on the PR.

## ⚡ What It Does
- Triggers on Pull Request events
- Fetches changed files using GitHub API
- Filters relevant source code files
- Uses AI to detect security issues (OWASP-focused)
- Generates structured findings (Severity, Issue, Fix)
- Posts automated comments on the PR

## 🏗 Architecture
- n8n (workflow orchestration)
- GitHub API
- OpenAI API

## 🔄 Workflow
1. PR is created
2. Webhook triggers n8n
3. Fetch changed files
4. Filter code files
5. Analyze each file using AI
6. Aggregate results
7. Post security report to PR

## 🧪 Example Output
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

## ⚙️ Setup
1. Import workflow into n8n
2. Configure credentials (GitHub + OpenAI)
3. Add GitHub webhook
4. Test with PR

## 📊 Status
Production-ready (basic)
