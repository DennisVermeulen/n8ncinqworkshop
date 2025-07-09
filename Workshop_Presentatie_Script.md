# 📋 CINQ Workshop Script - 30 Minuten

## 🎯 Workshop Doel
Deelnemers leren in 30 minuten een praktische n8n workflow bouwen die RSS feeds leest, AI samenvattingen maakt en output genereert.

---

## ⏱️ TIJDSCHEMA

### **[0-5 min] Opening & Demo**
```
✅ "Welkom! Vandaag bouwen we samen een AI News Bot"
✅ Toon eindresultaat (1 min demo)
✅ "Van RSS feed naar Nederlandse samenvatting in 5 nodes"
✅ Check: Iedereen n8n open? → /CINQ_Workshop_30min.json geïmporteerd?
```

### **[5-15 min] Stap-voor-Stap Uitleg**

#### 1️⃣ Manual Trigger (1 min)
```
"We starten simpel met een manual trigger"
- Klik → Execute Workflow
- "Later maken we dit een daily schedule"
```

#### 2️⃣ RSS Feed Node (3 min)
```
"Deze leest tech nieuws van The Hacker News"
- Toon: URL veld = https://feeds.feedburner.com/TheHackersNews
- Execute → Laat output zien
- "Straks gaan jullie deze URL aanpassen"
```

#### 3️⃣ Limit + Aggregate (2 min)
```
"We pakken top 5 artikelen en combineren ze"
- Limit: waarom maar 5? (kosten & snelheid)
- Aggregate: maakt één data object voor AI
```

#### 4️⃣ AI Summary (4 min)
```
"Het brein van onze workflow"
- Toon de prompt (lees voor)
- Leg uit: {{ $json.data }} template syntax
- "AI vertaalt en vat samen in Nederlands"
- Execute → Toon resultaat
```

### **[15-25 min] Hands-On Time! 🛠️**

#### Opdracht 1: Wijzig RSS Feed (3 min)
```
"Kies een andere RSS feed:"
Option A: https://www.nu.nl/rss/Tech (Nederlandse tech)
Option B: https://tweakers.net/feeds/nieuws.xml (Tweakers)
Option C: Eigen keuze!

→ Help mensen die vastlopen
→ "Vergeet niet te saven!"
```

#### Opdracht 2: Personaliseer AI Prompt (4 min)
```
"Maak het je eigen:"
- Wijzig taal: "Make an English summary"
- Wijzig focus: "Focus alleen op AI en Cloud nieuws"
- Wijzig toon: "Schrijf als een tech influencer"

→ Moedig creativiteit aan!
```

#### Opdracht 3: Test & Deel (3 min)
```
"Execute je workflow!"
- Bekijk elkaar's resultaten
- Wat werkt goed? Wat niet?
- Quick troubleshooting
```

### **[25-30 min] Wrap-up & Next Steps**

#### Praktische Tips
```
✨ "3 dingen om te onthouden:"
1. Start klein, bouw uit
2. Test vaak met Manual Trigger
3. Hergebruik nodes uit templates
```

#### Uitbreidingen
```
🚀 "Volgende stappen:"
- Schedule Trigger voor dagelijks nieuws
- Slack/Email integratie
- Meerdere RSS feeds tegelijk
- Filter op keywords
```

#### Resources
```
📚 "Waar verder leren:"
- n8n.io/workflows (1000+ templates)
- community.n8n.io (vragen stellen)
- Deze workflow: [github-link]
```

---

## 🎤 PRESENTER TIPS

### Do's ✅
- **Enthousiast blijven** - Het is maar 30 min!
- **Live troubleshooten** - Fouten maken het echt
- **Tijd bewaken** - Gebruik timer op telefoon
- **Simpel houden** - Geen advanced features

### Don'ts ❌
- Niet te diep op techniek ingaan
- Geen complexe authenticatie setup
- Niet alle nodes uitleggen
- Geen perfectie verwachten

### Backup Plan 🆘
- Pre-built workflow klaar als backup
- Screenshot van werkend resultaat
- Offline API mock (als internet faalt)
- Co-presenter voor chat support

---

## 💬 VEEL GESTELDE VRAGEN

**"Waarom werkt mijn AI niet?"**
→ Check: AI node connected? Credentials ingevuld?

**"Kan dit ook met ChatGPT?"**
→ Ja! Wijzig OpenAI node naar ChatGPT node

**"Hoe schedulen?"**
→ Vervang Manual Trigger met Schedule Trigger

**"Kosten?"**
→ ~€0.01 per run met GPT-3.5

**"Kan dit on-premise?"**
→ Ja! Gebruik Ollama voor lokale AI

---

## 📊 SUCCES METRICS

Workshop is geslaagd als:
- [ ] 80% deelnemers krijgt workflow werkend
- [ ] 60% personaliseert succesvol de prompt  
- [ ] 50% wil n8n verder verkennen
- [ ] Niemand gefrustreerd raakt
- [ ] Tijd niet uitloopt

---

## 🎁 BONUS (als tijd over)

Toon snel één van deze:
1. Slack integratie (2 min)
2. Error handling (2 min)
3. Multiple RSS feeds (3 min)
4. Schedule trigger (1 min)

**Eindig altijd met:**
"Bedankt! Ga thuis verder experimenteren. Join onze Slack voor vragen!"