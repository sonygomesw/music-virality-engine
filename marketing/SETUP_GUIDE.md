# CLIPTOKK - SETUP COMPLET

## 1. EMAIL OUTREACH SYSTEM

### Option A: Instantly.ai (Recommandé)
- **Prix:** $37/mois (Growth plan)
- **Pourquoi:** Meilleur deliverability, warm-up automatique
- **Setup:**
  1. Créer compte: https://instantly.ai
  2. Connecter domaine email (utiliser un domaine secondaire, pas @cliptokk.com principal)
  3. Acheter domaine dédié: cliptokk-outreach.com ou getcliptokk.com
  4. Créer 3 emails: sony@, contact@, team@
  5. Activer warm-up (2 semaines avant d'envoyer en masse)

### Option B: Apollo.io
- **Prix:** Free tier disponible, $49/mois pour plus
- **Avantage:** Base de données de prospects intégrée
- **Setup:**
  1. Créer compte: https://apollo.io
  2. Connecter email
  3. Utiliser leur base de données pour trouver prospects

### Configuration emails:
```
Domaine: getcliptokk.com (exemple)
Emails:
- sony@getcliptokk.com
- team@getcliptokk.com
- contact@getcliptokk.com

DNS à configurer:
- SPF record
- DKIM
- DMARC
```

---

## 2. SCRAPER PROSPECTS

### Apify - LinkedIn Scraper

**Compte:** https://apify.com (free tier = 5$/mois de crédits)

**Actor à utiliser:** "LinkedIn Profile Scraper" ou "LinkedIn Search Export"

**Recherches à faire:**

```
1. Artist Managers:
   - "artist manager" music
   - "talent manager" music industry
   - "manager" independent artist

2. Label A&R:
   - "A&R" record label
   - "A&R manager" music
   - "talent acquisition" music

3. Marketing Directors (Brands):
   - "head of marketing" DTC
   - "marketing director" e-commerce
   - "growth lead" consumer brand

4. Podcast Hosts:
   - "podcast host" + niche
   - "podcast producer"
   - "content creator" podcast
```

**Process:**
1. Scrape LinkedIn profiles
2. Export vers CSV
3. Enrichir emails avec Hunter.io ou Apollo
4. Import dans Instantly

### Hunter.io - Email Finder
- **Prix:** Free tier = 25 recherches/mois, $49/mois pour 500
- **Usage:** Trouver email depuis nom + domaine

### Script conceptuel Apify:
```javascript
// Input: Liste de recherches LinkedIn
// Output: CSV avec Name, Title, Company, LinkedIn URL

// Ensuite enrichir avec:
// Hunter.io API: GET https://api.hunter.io/v2/email-finder?domain={company}&first_name={first}&last_name={last}
```

---

## 3. CRM - NOTION TEMPLATE

### Structure Base de Données:

**Table: Prospects**
| Champ | Type |
|-------|------|
| Name | Text |
| Email | Email |
| Company | Text |
| Role | Select (Artist Manager, Label, Brand, Podcast) |
| Status | Select (New, Contacted, Replied, Call Booked, Closed, Lost) |
| Source | Select (LinkedIn, Instagram, Cold Email, Inbound) |
| Last Contact | Date |
| Notes | Text |
| Deal Value | Number |

**Views:**
1. **Pipeline** - Kanban par Status
2. **This Week** - Filtre par Last Contact
3. **Hot Leads** - Filtre Status = Replied ou Call Booked
4. **By Source** - Groupé par Source

### Formule Notion pour tracking:

```
// Conversion Rate
Closed / Total Contacted × 100

// Revenue Pipeline
Sum of Deal Value where Status = "Call Booked"
```

---

## 4. TRACKING DASHBOARD

### Google Sheets - Metrics Daily

| Date | Emails Sent | DMs Sent | TikTok Views | Calendly Clicks | Calls Booked | Deals Closed | Revenue |
|------|-------------|----------|--------------|-----------------|--------------|--------------|---------|
| J1 | 50 | 30 | 10K | 3 | 1 | 0 | €0 |
| J2 | 50 | 30 | 15K | 5 | 2 | 0 | €0 |
| ... | ... | ... | ... | ... | ... | ... | ... |

### KPIs à tracker:

**Weekly:**
- Total outreach (emails + DMs)
- Response rate
- Calls booked
- Calls completed
- Deals closed
- Revenue

**Monthly:**
- Total revenue
- Average deal size
- CAC (coût acquisition client)
- Close rate (calls → deals)

---

## 5. OUTILS COMPLETS - STACK

### Outreach:
- **Instantly.ai** - Email automation ($37/mois)
- **Hunter.io** - Email finding ($49/mois)
- **Apify** - Scraping ($49/mois)

### Content:
- **CapCut** - Video editing (gratuit)
- **Canva Pro** - Graphics ($12/mois)
- **Later** - Scheduling ($18/mois)

### CRM & Tracking:
- **Notion** - CRM (gratuit)
- **Google Sheets** - Metrics (gratuit)
- **Calendly** - Booking (gratuit tier)

### Communication:
- **Slack** - Team (gratuit)
- **Loom** - Video messages (gratuit)

### Total coût mensuel: ~$165/mois

---

## 6. SETUP JOUR 1 - CHECKLIST

### Morning (2h):
- [ ] Acheter domaine outreach (Namecheap, ~$10)
- [ ] Créer compte Instantly.ai
- [ ] Setup 3 emails sur le domaine
- [ ] Configurer DNS (SPF, DKIM, DMARC)
- [ ] Activer warm-up emails

### Afternoon (2h):
- [ ] Créer compte Apify
- [ ] Faire premier scrape LinkedIn (100 prospects test)
- [ ] Créer compte Hunter.io
- [ ] Enrichir 50 prospects avec emails

### Evening (2h):
- [ ] Setup Notion CRM
- [ ] Importer premiers prospects
- [ ] Créer Google Sheet tracking
- [ ] Programmer premiers emails (pour J+14 après warm-up)

---

## 7. SETUP JOUR 2 - CONTENT

### Morning (3h):
- [ ] Filmer 3 vidéos controverse (scripts prêts)
- [ ] Filmer 2 vidéos explicatives courtes

### Afternoon (2h):
- [ ] Éditer vidéos (CapCut)
- [ ] Créer thumbnails/covers
- [ ] Préparer 10 posts Threads
- [ ] Préparer 5 posts Twitter

### Evening (1h):
- [ ] Poster premier batch TikTok
- [ ] Poster premiers Threads
- [ ] Setup Later pour scheduling

---

## 8. SEMAINE 1 - OBJECTIFS

| Jour | Emails | DMs | TikToks | Threads |
|------|--------|-----|---------|---------|
| L | 50 | 30 | 10 | 10 |
| M | 50 | 30 | 10 | 10 |
| M | 50 | 30 | 10 | 10 |
| J | 50 | 30 | 10 | 10 |
| V | 50 | 30 | 10 | 10 |
| S | 25 | 15 | 5 | 5 |
| D | Batch content | - | - | - |

**Total Semaine 1:**
- 275 emails
- 165 DMs
- 55 TikToks
- 55 Threads

**Expected results:**
- 10-15 réponses positives
- 3-5 calls booked
- 0-1 deal (early days)

---

## 9. TEMPLATES PRÊTS À COPIER

### Email Subject Lines (rotation):
```
1. How we got Drake to #2 Billboard
2. Quick question about [Company]'s TikTok
3. 30,000 posts in 7 days - here's what happened
4. [Name], saw your work on [Platform]
5. TikTok distribution for [Artist/Brand]
```

### DM Opener (rotation):
```
1. "Hey! Love your work. Quick question about TikTok distribution..."
2. "Hey [Name], been following you. Do you work with distribution networks?"
3. "Fire content! Are you scaling on TikTok right now?"
```

### Calendly Message:
```
Thanks for booking!

Before our call, a few things:
1. This is a 15-min strategy call, not a sales pitch
2. Come with questions about your TikTok goals
3. I'll share some insights regardless of whether we work together

See you soon!
[Name]
```

---

## 10. AUTOMATION FLOWS

### Email Sequence (3-touch):

**Email 1 (Day 0):**
Subject: How we got Drake to #2 Billboard
[Main pitch]

**Email 2 (Day 3):**
Subject: Re: Quick follow-up
"Hey [Name], just floating this back up. Worth a quick chat?"

**Email 3 (Day 7):**
Subject: Last one from me
"Hey, I'll stop here. If TikTok distribution ever becomes a priority, I'm around. Good luck!"

### Response triggers:
- If reply contains "interested" → Move to "Call Booked" + send Calendly
- If reply contains "not now" → Move to "Nurture" + add to newsletter
- If reply contains "unsubscribe" → Remove immediately

---

## READY TO EXECUTE

Tout est documenté. Maintenant c'est l'exécution.

**Premier milestone:**
- 1000 emails envoyés
- 500 DMs envoyés
- 100 contenus postés
- 10 calls bookés
- 2 deals closés

**Timeline:** 30 jours

Let's go.
