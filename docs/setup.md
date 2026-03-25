# ⚙️ Setup Guide (Production v3)

## 🚀 Overview
This guide helps you set up the DevSecOps AI PR Security Agent using n8n, GitHub, and OpenAI.

---

## 1. n8n Setup

- Import the workflow: workflows/devsecops-agent-v3.json
- Activate the workflow
- Copy the generated Webhook URL

---

## 2. GitHub Webhook Setup

Go to your repository:

Settings → Webhooks → Add Webhook

Fill the details:

- Payload URL: your n8n webhook URL  
- Content type: application/json  
- Events: Pull requests  

Click "Add webhook"

---

## 3. Credentials Configuration (Critical Step)

### GitHub API

In n8n:
- Create credential → HTTP Header Auth

Add:
Authorization: Bearer YOUR_GITHUB_TOKEN  
Accept: application/vnd.github+json  

---

### OpenAI API

In n8n:
- Create credential → HTTP Header Auth

Add:
Authorization: Bearer YOUR_OPENAI_API_KEY  
Content-Type: application/json  

---

## 4. How the System Works

1. A Pull Request is created  
2. GitHub webhook triggers n8n  
3. Changed files are fetched via GitHub API  
4. Code files are filtered (.js, .ts, .java, .py)  
5. Each file is analyzed using AI  
6. Security findings are generated  
7. A structured report is posted as a PR comment  

---

## 5. Testing the Setup

- Create a sample Pull Request with small code changes  
- Open n8n → Executions  
- Verify:
  - Workflow is triggered  
  - AI response is generated  
  - Comment is posted on the PR  

---

## 📌 Notes

- Only supported file types are analyzed  
- Large PRs may take longer (batch processing)  
- Ensure API keys are valid  
- Use small PRs for initial testing  

---

## ⚠️ Common Issues

Webhook not triggering:
- Check webhook URL  
- Ensure workflow is active  

No PR comment:
- Verify GitHub token permissions  
- Check n8n logs  

AI not responding:
- Verify OpenAI API key  
- Check usage limits  

---

## ✅ Status

Production-ready (basic level)  
End-to-end workflow functional