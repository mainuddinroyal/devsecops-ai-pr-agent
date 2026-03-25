# Setup Guide

## 1. n8n
- Import `workflows/devsecops-agent.json`
- Set Webhook URL and activate workflow

## 2. GitHub
- Create a webhook on your repo
- Events: Pull Request
- Payload URL: your n8n webhook URL

## 3. Credentials
- Add GitHub token in n8n (for future PR comments)
- Add OpenAI API key

## 4. Test
- Open a PR with sample changes
- Verify webhook hits n8n
- Check AI output in execution logs
