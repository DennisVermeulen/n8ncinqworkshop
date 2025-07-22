# CINQ n8n Workshop - RSS AI Summary

This project contains n8n workflows for automatically summarizing RSS news feeds with AI.

## 📁 Files

### 1. CINQ_Workshop.json
Complete workflow with:
- Multiple RSS feeds (The Hacker News, SRE Weekly, Kubernetes, Azure Weekly)
- Filtering articles from last 24 hours
- AI summary with Ollama (Gemma3n model)
- Export to RTF file

### 2. CINQ_Workshop_30min.json (✨ Modified)
Simplified workshop version (30 minutes) with:
- Single RSS feed for quick demo
- OpenAI integration (GPT-3.5)
- Direct result in browser
- **NEW: Export to Markdown file** 📝

### 3. Workshop_Presentation_Script.md
Presentation script for workshop leaders

## 🚀 Key Modification

The 30-minute workshop workflow now automatically saves AI-generated summaries as Markdown files:

- **Location**: `/home/node/files/`
- **Filename**: `news-summary-yyyy-MM-dd_HH-mm-ss.md`
- **Format**: Markdown with timestamps and formatting

## 📋 Requirements

- n8n instance
- OpenAI API key (for 30min version) OR local Ollama (for full version)
- Write permissions for `/home/node/files/`

## 🛠️ Installation

1. Import desired workflow JSON into n8n
2. Configure credentials:
   - OpenAI API for `CINQ_Workshop_30min.json`
   - Ollama endpoint for `CINQ_Workshop.json`
3. Create output folder: `mkdir -p /home/node/files/`
4. Test with Manual Trigger

## 💡 Workshop Tips

- Start with 30-minute version for beginners
- Let participants add their own RSS feeds
- Experiment with different AI prompts
- Demonstrate the markdown export functionality

## 🔧 Customizations

### Using Different Output Folder
Change in the "Save as Markdown" node:
```javascript
'/home/node/files/news-summary-' + $now.toFormat('yyyy-MM-dd_HH-mm-ss') + '.md'
```

### Other File Formats
Adjust the "Convert to Markdown" node:
- `text` for .txt
- `json` for .json
- `html` for .html

## 📚 More Information

- [n8n Documentation](https://docs.n8n.io)
- [RSS Feed Sources](https://github.com/plenaryapp/awesome-rss-feeds)
- [n8n Community](https://community.n8n.io)

---
*Workshop developed for CINQ*