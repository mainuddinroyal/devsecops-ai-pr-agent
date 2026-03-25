# DevSecOps AI PR Security Agent

A production-oriented AI agent that reviews GitHub Pull Requests and identifies security vulnerabilities before merge.

## Problem
Code reviews miss security issues due to time constraints and lack of expertise.

## Solution
This agent automatically analyzes PR changes and posts structured security findings.

## Features
- PR-based trigger
- File-level analysis
- OWASP Top 10 detection
- Structured output (severity, issue, fix)
- Automated PR comments

## Architecture
- n8n (workflow engine)
- GitHub API
- AI model for analysis

## Project Structure
```
/workflows
/docs
/scripts
```

## Setup
1. Import workflow into n8n
2. Configure GitHub credentials
3. Add OpenAI API key
4. Connect webhook to PR events

## Output Example
```
[HIGH] SQL Injection risk in UserService.java
Fix: Use prepared statements
```

## Status
Initial production-ready structure
