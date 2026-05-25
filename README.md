# DOI Validator Skill

A robust, highly accurate academic reference validator designed for LLM agents. It fetches real, verified metadata directly from live **CrossRef** and **PubMed** APIs to prevent citation hallucinations and ensure reference integrity.

## 🌟 Features

- 🛑 **Anti-Hallucination:** Guarantees that every cited DOI actually exists by resolving it against live APIs before writing.
- 🎓 **APA 7th Edition Formatting:** Formats verified citations perfectly according to the latest APA 7th Edition style, including sentence case and full-url DOIs.
- 📂 **RIS Format Generation:** Generates standardized Research Information Systems (RIS) export blocks compatible with Zotero, Mendeley, EndNote, and other reference managers.
- 🔀 **Smart Fallback Architecture:** Automatically falls back to the PubMed API for clinical, open-access, or specialized biomedical papers not yet indexed by CrossRef.
- 📬 **API Polite Pool Etiquette:** Uses a customizable `User-Agent` header to process requests through CrossRef's higher-rate polite pool.

## 🛠️ Repository Contents

- [doi-validator/SKILL.md](file:///doi-validator/SKILL.md) — The core executable instructions and API mapping schema.
- `doi-validator.skill` — The packaged, ready-to-load ZIP file for integration with AI platforms/agents.

## 🚀 How to Use

### Integrating with an AI Agent
You can load this skill directory or zip file into your AI programming workspace/agent platform. The system will read `SKILL.md` as an executable skill instruction block when requested to validate references, fetch DOIs, or compile a bibliography.

### Manual API Resolution (Example)

To manually resolve a DOI using the CrossRef API polite pool, you can run:

```bash
curl -s "https://api.crossref.org/works/{YOUR_DOI}" \
  -H "User-Agent: DOIValidator/1.0 (mailto:your-email@example.com)"
```

## ⚖️ License & Copyright

Copyright (c) 2026 Muhammed Elnaggar. All rights reserved.

Licensed under the [MIT License](LICENSE). Under this license, anyone is free to use, modify, and distribute this software, provided that the original copyright notice and permission notice are included in all copies or substantial portions of the software.
