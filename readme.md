# Microsoft Threat Intelligence Plugin for Security Copilot

This Security Copilot plugin integrates with [VirusTotal](https://www.virustotal.com/) to provide fast, filtered threat intelligence for file hashes, URLs, IP addresses, and domain names.

## 🔍 Features

- 🔒 File hash lookup (SHA256, MD5, SHA1)
- 🌐 URL scanning and reputation check
- 🛰️ IP address threat analysis
- 🌎 Domain reputation and category lookup
- 🎯 Filtered outputs: Only the most relevant indicators (malicious, suspicious, undetected counts, reputation, categories, etc.)

## 📦 API Hosting

The plugin uses a static API key for VirusTotal and is hosted using OpenAPI 3.1 specification.

- **OpenAPI spec:** [`openapi.yaml`](./openapi.yaml)
- **Plugin manifest:** [`.well-known/ai-plugin.json`](./.well-known/ai-plugin.json)

## 🚀 Deployment Instructions

1. **Clone this repo and host it publicly** on GitHub Pages, Azure Static Web Apps, or any public HTTPS endpoint.
2. Replace the placeholder in `openapi.yaml` with your VirusTotal API key:

   ```yaml
   Authorization:
