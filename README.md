# CINQ n8n Workshop - RSS AI Summary

Dit project bevat n8n workflows voor het automatisch samenvatten van RSS nieuws feeds met AI.

## 📁 Bestanden

### 1. CINQ_Workshop.json
Volledige workflow met:
- Meerdere RSS feeds (The Hacker News, SRE Weekly, Kubernetes, Azure Weekly)
- Filtering op artikelen van laatste 24 uur
- AI samenvatting met Ollama (Gemma3n model)
- Export naar RTF bestand

### 2. CINQ_Workshop_30min.json (✨ Aangepast)
Vereenvoudigde workshop versie (30 minuten) met:
- Enkele RSS feed voor snelle demo
- OpenAI integratie (GPT-3.5)
- Direct resultaat in browser
- **NIEUW: Export naar Markdown bestand** 📝

### 3. Workshop_Presentatie_Script.md
Presentatie script voor workshop leiders

## 🚀 Belangrijkste Aanpassing

De 30-minuten workshop workflow slaat nu automatisch de AI-gegenereerde samenvattingen op als Markdown bestanden:

- **Locatie**: `/home/node/files/`
- **Bestandsnaam**: `news-summary-yyyy-MM-dd_HH-mm-ss.md`
- **Format**: Markdown met timestamps en opmaak

## 📋 Vereisten

- n8n instance
- OpenAI API key (voor 30min versie) OF Ollama lokaal (voor volledige versie)
- Write permissions voor `/home/node/files/`

## 🛠️ Installatie

1. Import de gewenste workflow JSON in n8n
2. Configureer credentials:
   - OpenAI API voor `CINQ_Workshop_30min.json`
   - Ollama endpoint voor `CINQ_Workshop.json`
3. Maak de output folder aan: `mkdir -p /home/node/files/`
4. Test met Manual Trigger

## 💡 Workshop Tips

- Start met de 30-minuten versie voor beginners
- Laat deelnemers hun eigen RSS feeds toevoegen
- Experimenteer met verschillende AI prompts
- Demonstreer de markdown export functionaliteit

## 🔧 Aanpassingen

### Andere output folder gebruiken
Wijzig in de "Save as Markdown" node:
```javascript
'/home/node/files/news-summary-' + $now.toFormat('yyyy-MM-dd_HH-mm-ss') + '.md'
```

### Andere bestandsformaten
Pas de "Convert to Markdown" node aan:
- `text` voor .txt
- `json` voor .json
- `html` voor .html

## 📚 Meer Informatie

- [n8n Documentatie](https://docs.n8n.io)
- [RSS Feed Bronnen](https://github.com/plenaryapp/awesome-rss-feeds)
- [n8n Community](https://community.n8n.io)

---
*Workshop ontwikkeld voor CINQ*