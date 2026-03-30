# n8n-vuln-automation
Automate vulnerability remediation using AI agents
- The workflow is triggered by an uploaded vulnerability report (CSV or TXT).
- The raw vulnerability data is fed to the Gemini LLM. Gemini determines the core issue and generates the appropriate fix or update instructions.
- The validated `build.gradle` changes are committed and pushed to the designated branch in your GitHub repository, ready for review and deployment.

## Running n8n using docker
```docker run -it -d --rm \
 --name n8n \
 -p 5678:5678 \
 -e GENERIC_TIMEZONE="TW" \
 -e TZ="TW" \
 -e N8N_ENFORCE_SETTINGS_FILE_PERMISSIONS=true \
 -e N8N_RUNNERS_ENABLED=true \
 -v /scripts \
 -v n8n_data:/home/node/.n8n \
 docker.n8n.io/n8nio/n8n start --tunnel
```
Note: `--tunnel` is used only for TESTING purposes.

## Prerequisites
