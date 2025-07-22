# 📋 CINQ Workshop Script - 30 Minutes

## 🎯 Workshop Goal
Participants learn to build a practical n8n workflow in 30 minutes that reads RSS feeds, creates AI summaries, and generates output.

---

## ⏱️ TIME SCHEDULE

### **[0-5 min] Opening & Demo**
```
✅ "Welcome! Today we're building an AI News Bot together"
✅ Show end result (1 min demo)
✅ "From RSS feed to AI summary in 5 nodes"
✅ Check: Everyone has n8n open? → /n8n/CINQ n8n workshop.json imported?
```

### **[5-15 min] Step-by-Step Explanation**

#### 1️⃣ Manual Trigger (1 min)
```
"We start simple with a manual trigger"
- Click → Execute Workflow
- "Later we'll make this a daily schedule"
```

#### 2️⃣ RSS Feed Node (3 min)
```
"This reads tech news from The Hacker News"
- Show: URL field = https://feeds.feedburner.com/TheHackersNews
- Execute → Show output
- "Soon you'll customize this URL"
```

#### 3️⃣ Limit + Aggregate (2 min)
```
"We take top 5 articles and combine them"
- Limit: why only 5? (cost & speed)
- Aggregate: creates one data object for AI
```

#### 4️⃣ AI Summary (4 min)
```
"The brain of our workflow"
- Show the prompt (read aloud)
- Explain: {{ $json.data }} template syntax
- "AI translates and summarizes"
- Execute → Show result
```

### **[15-25 min] Hands-On Time! 🛠️**

#### Assignment 1: Change RSS Feed (3 min)
```
"Choose a different RSS feed:"
Option A: https://techcrunch.com/feed/ (Tech news)
Option B: https://www.bright.nl/feed/news.xml?tag=AI (Bright)
Option C: Your own choice!

→ Help people who get stuck
→ "Don't forget to save!"
```

#### Assignment 2: Personalize AI Prompt (4 min)
```
"Make it your own:"
- Change language: "Maak een Nederlandse samenvatting"
- Change focus: "Focus only on AI and Cloud news"
- Change tone: "Write like a tech influencer"

→ Encourage creativity!
```

#### Assignment 3: Test & Share (3 min)
```
"Execute your workflow!"
- Look at each other's results
- What works well? What doesn't?
- Quick troubleshooting
```

### **[25-30 min] Wrap-up & Next Steps**

#### Practical Tips
```
✨ "3 things to remember:"
1. Start small, build out
2. Test often with Manual Trigger
3. Reuse nodes from templates
```

#### Extensions
```
🚀 "Next steps:"
- Schedule Trigger for daily news
- Slack/Email integration
- Multiple RSS feeds simultaneously
- Filter by keywords
```

#### Resources
```
📚 "Where to learn more:"
- n8n.io/workflows (1000+ templates)
- community.n8n.io (ask questions)
- This workflow: [github-link]
```

---

## 🎤 PRESENTER TIPS

### Do's ✅
- **Stay enthusiastic** - It's only 30 min!
- **Live troubleshoot** - Mistakes make it real
- **Watch the time** - Use timer on phone
- **Keep it simple** - No advanced features

### Don'ts ❌
- Don't go too deep into technicals
- No complex authentication setup
- Don't explain all nodes
- Don't expect perfection

### Backup Plan 🆘
- Pre-built workflow ready as backup
- Screenshot of working result
- Offline API mock (if internet fails)
- Co-presenter for chat support

---

## 💬 FREQUENTLY ASKED QUESTIONS

**"Why isn't my AI working?"**
→ Check: AI node connected? Credentials filled in?

**"Can this work with ChatGPT?"**
→ Yes! Change OpenAI node to ChatGPT node

**"How to schedule?"**
→ Replace Manual Trigger with Schedule Trigger

**"Costs?"**
→ ~€0.01 per run with GPT-3.5

**"Can this run on-premise?"**
→ Yes! Use Ollama for local AI

---

## 📊 SUCCESS METRICS

Workshop is successful if:
- [ ] 80% of participants get workflow running
- [ ] 60% successfully personalize the prompt  
- [ ] 50% want to explore n8n further
- [ ] Nobody gets frustrated
- [ ] Time doesn't run out

---

## 🎁 BONUS (if time permits)

Quickly show one of these:
1. Slack integration (2 min)
2. Error handling (2 min)  
3. Multiple RSS feeds (3 min)
4. Schedule trigger (1 min)

**Always end with:**
"Thank you! Continue experimenting at home. Join our Slack for questions!"