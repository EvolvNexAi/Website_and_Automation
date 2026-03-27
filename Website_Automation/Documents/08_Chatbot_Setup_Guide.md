# EVOLVNEX - Chatbot Setup Guide (Base44)

**For:** Tier 2 & Tier 3 packages
**Platform:** Base44 AI Chatbot
**Turnaround:** 1 day setup

---

## Prerequisites

Before starting chatbot setup:
- [ ] Website is built and live (or in preview)
- [ ] Client has provided FAQ list (10-20 questions)
- [ ] Client has provided contact info for lead capture
- [ ] Base44 project is created

---

## Step 1: Access Base44 Chatbot Builder

1. Login to Base44 dashboard
2. Open client project
3. Go to: **Features → AI Chatbot** (or "Builder Chat")
4. Click: **Add Chatbot** or **Configure**

---

## Step 2: Configure Chatbot Personality

### Basic Settings:
| Field | Value |
|-------|-------|
| Bot Name | [Clinic Name] Assistant |
| Tone | Professional, Friendly, Helpful |
| Language | English + Hindi (bilingual) |
| Response Style | Concise, patient-friendly |

### System Prompt (for Base44 AI):
```
You are a helpful assistant for [Business Name], a [clinic/salon/cafe] in [City].

Your role:
1. Answer common FAQs (see knowledge base below)
2. Collect visitor information (name, phone, email, service interest)
3. Guide visitors to book appointments via WhatsApp/phone
4. Be polite, professional, and helpful

When you don't know an answer:
- Politely say you'll connect them with a team member
- Offer WhatsApp number or callback request

Always end with a CTA:
- "Would you like to book an appointment?"
- "Can I share our WhatsApp number for quick booking?"
```

---

## Step 3: Upload Knowledge Base (FAQs)

### Client FAQ Template (Collect this in onboarding):

**For Clinics:**
```
Q: What are your clinic hours?
A: We're open Mon-Sat, 10am-7pm. Sundays closed.

Q: Do you accept walk-in patients?
A: Yes, we accept walk-ins, but appointments are preferred for shorter wait times.

Q: What services do you offer?
A: We offer [list main services]. See our Services page for details.

Q: Do you accept insurance?
A: [Yes/No - as per client]

Q: What's the consultation fee?
A: ₹[X] for general consultation. Procedure costs vary.

Q: How do I book an appointment?
A: Click the WhatsApp button or call us at [number].

Q: Where is your clinic located?
A: [Full address]. We're near [landmark].

Q: Do you offer emergency services?
A: [Yes/No - as per client]

Q: Can I consult online?
A: Yes, we offer video consultations. Book via WhatsApp.

Q: What safety protocols do you follow?
A: We follow all government health guidelines. Masks and sanitization available.
```

**For Salons:**
```
Q: What are your operating hours?
A: We're open Mon-Sun, 10am-8pm.

Q: Do I need an appointment?
A: Walk-ins welcome, but booking ensures no wait time.

Q: What services do you offer?
A: Hair styling, coloring, facials, manicure, pedicure, bridal makeup, and more.

Q: What's the price for [service]?
A: Starting at ₹[X]. Exact price depends on hair length/style.

Q: Do you use branded products?
A: Yes, we use [L'Oréal/Olvera/etc.] professional products.

Q: Can I see your work portfolio?
A: Check our Gallery page for before/after photos.

Q: How do I book a bridal package?
A: WhatsApp us at [number] for a consultation.

Q: Do you offer home services?
A: [Yes/No - as per client]
```

### Upload to Base44:
1. In Chatbot settings: **Knowledge Base**
2. Paste FAQs as text or upload document
3. Base44 AI will index these
4. Test: Ask sample questions to verify answers

---

## Step 4: Configure Lead Capture Form

### Fields to Collect:
| Field | Type | Required? |
|-------|------|-----------|
| Full Name | Text | Yes |
| Phone Number | Phone | Yes |
| Email | Email | Optional |
| Service Interest | Dropdown | Yes |
| Preferred Date | Date | Optional |
| Message | Text | Optional |

### Form Setup:
1. In Chatbot: **Lead Capture** settings
2. Add fields as above
3. Map to Base44 database (auto-created)
4. Set notification: Email client when new lead captured
5. Test: Submit a test lead

---

## Step 5: Configure Human Handoff

### When Chatbot Can't Help:
```
If query is complex or visitor asks for human:

"I'd be happy to connect you with our team!
You can reach us directly:
📞 Call: [Client Phone]
💬 WhatsApp: [Client WhatsApp]

Or leave your details and we'll call you back within 2 hours."
```

### Setup:
1. In Chatbot: **Escalation** settings
2. Add handoff message as above
3. Show WhatsApp/phone buttons prominently
4. Optionally: Create "Request Callback" form

---

## Step 6: Test Chatbot

### Test Scenarios:
| Scenario | Expected Result |
|----------|-----------------|
| Ask about clinic hours | Bot shows correct hours |
| Ask about service price | Bot gives price range |
| Ask about location | Bot shows address + map link |
| Request appointment | Bot asks for name, phone, date |
| Complex medical question | Bot offers human handoff |
| Submit lead form | Lead saved in database, client notified |

### Testing Checklist:
- [ ] All FAQs answered correctly
- [ ] Lead form captures all fields
- [ ] Handoff works (shows phone/WhatsApp)
- [ ] Mobile view: Chatbot widget visible
- [ ] Desktop view: Chatbot widget visible
- [ ] No errors in console

---

## Step 7: Customize Chatbot Widget

### Widget Settings:
| Property | Value |
|----------|-------|
| Position | Bottom-right |
| Color | Match website theme |
| Size | Standard (not too large) |
| Greeting Message | "Hi! 👋 How can I help you today?" |
| Icon | Chat bubble or clinic logo |

### Customization (Base44):
1. Go to: **Chatbot → Widget Settings**
2. Adjust colors to match site
3. Set greeting message
4. Upload logo (if client has)
5. Save and preview

---

## Step 8: Go Live

### Pre-Launch Checklist:
- [ ] All FAQs configured
- [ ] Lead capture working
- [ ] Handoff configured
- [ ] Widget styled correctly
- [ ] Tested on mobile + desktop
- [ ] Client notified of test completion

### Launch:
1. Publish Base44 project
2. Chatbot goes live on site
3. Verify widget appears on live domain
4. Send test lead to client (confirm receipt)

---

## Step 9: Client Training

### Training Agenda (30 min):
1. **Show chatbot dashboard**
   - Where to view captured leads
   - How to export lead data (CSV)

2. **Update FAQs**
   - How to add new questions
   - How to edit existing answers

3. **Monitor performance**
   - Check chatbot conversations
   - Review common queries
   - Identify gaps (add new FAQs)

4. **Human handoff process**
   - When visitor requests human
   - How to follow up on leads

### Provide:
- 1-page quick reference guide
- Recorded Loom video of dashboard walkthrough
- WhatsApp support group link

---

## Step 10: Ongoing Monitoring (Monthly)

### Monthly Checks:
- [ ] Review chatbot conversation logs
- [ ] Identify unanswered queries (add to FAQ)
- [ ] Check lead conversion rate
- [ ] Update seasonal info (hours, offers)
- [ ] Report to client: "X leads captured this month"

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Chatbot not appearing | Check widget settings, publish project |
| FAQs not answering | Re-upload knowledge base, retrain AI |
| Lead form not working | Check field mapping, test submission |
| Client not receiving leads | Verify email notification setup |
| Chatbot giving wrong answers | Review knowledge base, refine system prompt |

---

## Chatbot Performance Metrics

Track monthly:
- **Total conversations:** [X]
- **Leads captured:** [X]
- **FAQ accuracy:** ~80-90%
- **Human handoffs:** [X]% of conversations
- **Visitor → Lead conversion:** [X]%

---

**Document Version:** 1.0 | **Created:** March 2026 | **EVOLVNEX**
