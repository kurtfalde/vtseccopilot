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

- **OpenAPI spec:** `openapi.yaml`
- **Plugin manifest:** `.well-known/ai-plugin.json`

## 🚀 Deployment Instructions

1. **Host the files** on GitHub Pages, Azure Static Web Apps, or any public HTTPS endpoint.
2. Update the `url` field in `ai-plugin.json` with the full path to your hosted `openapi.yaml`.
3. Add the plugin to Security Copilot using:
   ```
   https://yourdomain.com/.well-known/ai-plugin.json
   ```

## 🔐 Authentication

- The plugin uses a pre-configured VirusTotal API key.
- End-users do **not** need to provide their own keys.

## 📄 Example Query Prompts

- “Check this hash: `44d88612fea8a8f36de82e1278abb02f`”
- “Analyze `https://suspicious-site.biz`”
- “Get threat intel on IP `8.8.8.8`”
- “What’s the reputation of domain `example.com`?”

## 📬 Contact

- Maintainer: Microsoft Threat Engineering (generic)
- Email: [support@microsoft.com](mailto:support@microsoft.com)
- Legal: [Microsoft Legal Terms](https://www.microsoft.com/en-us/legal)