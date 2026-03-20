# EVOLVNEX - WhatsApp Automation Setup Guide

**For:** Tier 3 packages only
**Platforms:** Interakt / WATI / Gupshup (Meta BSPs)
**Turnaround:** 1-2 days setup

---

## Overview

### What We're Building:
1. **WhatsApp Business API** integration
2. **Automated message flows:**
   - Auto-reply to new inquiries
   - Booking confirmations
   - Appointment reminders
   - After-hours responses
3. **CRM sync:** Leads → Google Sheets/Airtable
4. **Broadcast campaigns:** Promotional messages (optional)

### Costs (Client Pays Directly):
| Provider | Monthly Cost | Setup Fee |
|----------|--------------|-----------|
| Interakt | ~₹2,000-3,000 | Sometimes free |
| WATI | ~₹2,500-4,000 | Free |
| Gupshup | ~₹2,000-5,000 | Varies |
| Meta Direct | Conversation-based pricing | N/A |

**Note:** Client contracts directly with provider. EVOLVNEX handles setup.

---

## Phase 1: Provider Selection & Signup

### Step 1: Recommend Provider to Client
**Recommendation:** **Interakt** or **WATI**
- India-focused
- Easy setup
- Good support
- Affordable for SMBs

### Step 2: Client Signs Up
**Client Actions:**
1. Visit: [interakt.ai](https://interakt.ai) or [wati.io](https://wati.io)
2. Click: "Get Started" / "Start Free Trial"
3. Fill business details:
   - Business name
   - GSTIN (if applicable)
   - Business website (your EVOLVNEX site!)
   - Contact person details
4. Submit documents:
   - Business proof (GST cert / Udyam / Shop Act)
   - ID proof (Aadhar/PAN of owner)
   - WhatsApp number (will be verified)

### Step 3: Approval (2-5 days)
- Provider reviews application
- WhatsApp verifies number
- API access granted

**Owner:** Client (with your guidance)
**Timeline:** 2-5 days for approval

---

## Phase 2: WhatsApp Number Verification

### Requirements:
- Dedicated WhatsApp number (can be same as business number)
- Number should NOT be on regular WhatsApp app (need to logout)
- Or use new number entirely

### Process:
1. **Backup existing chats** (if using current number)
2. **Logout from WhatsApp** on that number
3. **Provider sends OTP** to verify number
4. **Enter OTP** in provider dashboard
5. **Number verified** for WhatsApp API

### Important:
- Once on API, can't use regular WhatsApp app for that number
- All messages go through provider dashboard
- Use provider's WhatsApp Web interface

---

## Phase 3: Integration with Base44 Website

### Step 1: Get API Credentials from Provider
After approval, client gets:
- **API Key**
- **API Secret**
- **Webhook URL**
- **Phone Number ID**

### Step 2: Connect to Base44
**Option A: Native Integration (if Base44 supports)**
1. In Base44: **Integrations → WhatsApp**
2. Select provider (Interakt/WATI)
3. Paste API credentials
4. Test connection

**Option B: Webhook Integration**
1. In Base44: **Forms → Webhook**
2. Set webhook URL to provider's endpoint
3. Map form fields (name, phone, service, message)
4. Test: Submit form → check if WhatsApp message sent

**Option C: Zapier Integration**
1. Create Zapier account (free tier works)
2. Zap: **Base44 (Webhook) → WhatsApp (Interakt/WATI)**
3. Trigger: New form submission
4. Action: Send WhatsApp message
5. Test end-to-end

---

## Phase 4: Configure Automation Flows

### Flow 1: New Lead Auto-Reply

**Trigger:** Visitor submits contact form / chatbot captures lead

**Message Template:**
```
Hi [Name]! 👋

Thanks for reaching out to [Business Name].

We received your inquiry about [Service Interest].

Our team will contact you within 2 hours during business hours.

For urgent requests, call us: [Phone Number]

Clinic Hours: Mon-Sat, 10am-7pm

📍 [Business Address]
```

**Setup:**
1. In provider dashboard: **Automations**
2. Create: "New Lead Auto-Reply"
3. Trigger: Form submission / Lead captured
4. Message: Template above
5. Activate

---

### Flow 2: Booking Confirmation

**Trigger:** Appointment booked (via form or chatbot)

**Message Template:**
```
Hi [Name]! ✅

Your appointment is CONFIRMED.

📅 Date: [Appointment Date]
⏰ Time: [Time]
👨‍⚕️ Doctor: Dr. [Name]
📍 Location: [Clinic Address]

Please arrive 10 minutes early.

To reschedule, reply "RESCHEDULE" or call [Phone].

See you soon!
-[Business Name]
```

**Setup:**
1. Create: "Booking Confirmation" automation
2. Trigger: Booking form submission
3. Message: Template above
4. Activate

---

### Flow 3: Appointment Reminder (1 day before)

**Trigger:** Scheduled (1 day before appointment date)

**Message Template:**
```
Hi [Name]! 🔔

Friendly reminder:

Your appointment at [Business Name] is TOMORROW.

📅 Date: [Date]
⏰ Time: [Time]

Please confirm your attendance by replying "YES".

To reschedule, call us: [Phone]

Thanks!
```

**Setup:**
1. Create: "Appointment Reminder" automation
2. Trigger: Scheduled (1 day before, 10am)
3. Message: Template above
4. Activate

---

### Flow 4: After-Hours Auto-Reply

**Trigger:** Lead received outside business hours

**Message Template:**
```
Hi [Name]! 🌙

Thanks for contacting [Business Name].

Our clinic is currently CLOSED.

We're open: Mon-Sat, 10am-7pm

We'll respond to your inquiry first thing tomorrow morning.

For emergencies, please visit [nearest hospital] or call [emergency number].

Thanks for understanding!
```

**Setup:**
1. Create: "After-Hours Reply" automation
2. Trigger: Lead received (time condition: outside 10am-7pm)
3. Message: Template above
4. Activate

---

### Flow 5: Broadcast Campaign (Optional)

**Use Case:** Promotional offers, health tips, re-engagement

**Message Template (Example - Dental Clinic):**
```
Hi [Name]! 😁

Special Offer from [Business Name]!

🦷 FREE Dental Checkup Camp
📅 This Saturday, 10am-4pm
📍 [Clinic Address]

No consultation fee! Just ₹499 for cleaning.

Limited slots. Reply "BOOK" to reserve yours.

See you there!
-[Business Name]
```

**Setup:**
1. Create: "Broadcast Campaign"
2. Upload contact list (CSV of past leads/patients)
3. Message: Template above
4. Schedule send time
5. **Compliance:** Ensure recipients opted in

**Note:** Meta policies require opt-in for promotional messages.

---

## Phase 5: CRM Integration

### Google Sheets Integration

**Setup:**
1. Create Google Sheet:
   - Columns: Date, Name, Phone, Email, Service, Status
2. In provider dashboard: **Integrations → Google Sheets**
3. Connect Google account
4. Map fields:
   - WhatsApp name → Name column
   - Phone → Phone column
   - etc.
5. Test: Submit lead → check Sheet updates

### Airtable Integration (Alternative)

**Setup:**
1. Create Airtable base
2. In provider: **Integrations → Airtable**
3. Connect API key
4. Map fields
5. Test

---

## Phase 6: Testing End-to-End

### Test Scenarios:
| Scenario | Expected Result |
|----------|-----------------|
| Submit contact form | Auto-reply WhatsApp within 1 min |
| Book appointment | Confirmation message received |
| Submit after 7pm | After-hours reply received |
| Check Google Sheet | Lead data synced |

### Testing Checklist:
- [ ] All flows tested with real phone number
- [ ] Messages received within 1 minute
- [ ] CRM sync working (check Sheet/Airtable)
- [ ] Client trained on dashboard
- [ ] Broadcast test sent (internal team only)

---

## Phase 7: Client Training

### Training Agenda (1 hour):

**1. Dashboard Walkthrough**
- Show provider dashboard
- Where to view conversations
- How to respond manually
- How to export data

**2. Automation Management**
- How to view active automations
- How to pause/resume flows
- How to edit message templates

**3. Broadcast Campaigns**
- How to create broadcast
- Upload contact list
- Schedule send
- View analytics (delivered, opened, replied)

**4. Compliance**
- Meta messaging policies
- Opt-in requirements
- Block/report handling

**5. Billing**
- Monthly cost overview
- Conversation-based pricing (if applicable)
- Payment method setup

### Provide:
- Recorded Loom video
- Quick reference guide (1-pager)
- Provider support contact

---

## Phase 8: Go Live

### Pre-Launch Checklist:
- [ ] WhatsApp API approved
- [ ] All flows configured
- [ ] CRM integration working
- [ ] Client trained
- [ ] Test messages successful
- [ ] Client billing setup

### Launch:
1. Activate all automations
2. Confirm client can access dashboard
3. Add EVOLVNEX to support group
4. Monitor first 48 hours for issues

---

## Monthly Monitoring

### Checks (Monthly):
- [ ] Review automation performance
- [ ] Check message delivery rates
- [ ] Review broadcast campaign results
- [ ] Update message templates (seasonal)
- [ ] Report to client: "X messages sent, Y leads converted"

### Metrics to Track:
| Metric | Target |
|--------|--------|
| Auto-reply delivery rate | 95%+ |
| Response rate (broadcasts) | 10-20% |
| Lead → Patient conversion | Track % |
| Customer satisfaction | Monitor replies |

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Messages not sending | Check API credentials, account status |
| Client billed unexpectedly | Review conversation pricing, explain Meta policies |
| Automation not triggering | Check trigger conditions, test webhook |
| CRM not syncing | Reconnect integration, check field mapping |
| Broadcast rejected | Review Meta policies, ensure opt-in |

---

## Meta Messaging Policies (Important)

### Do's:
✅ Service messages (bookings, reminders, confirmations)
✅ Opted-in promotional messages
✅ Clear opt-out option ("Reply STOP to unsubscribe")

### Don'ts:
❌ Spam unsold contacts
❌ Misleading content
❌ Restricted categories (gambling, adult, etc.)

### Template Approval:
- Some providers require template approval
- Allow 24-48 hours for approval
- Keep templates evergreen (avoid time-sensitive content)

---

## Cost Summary for Client

| Cost Item | Amount | Paid By |
|-----------|--------|---------|
| Provider Setup | Free-₹2,000 | Client |
| Monthly Subscription | ₹2,000-5,000 | Client |
| Conversation Charges | As per Meta | Client |
| EVOLVNEX Setup | Included in Tier 3 | Prepaid |
| EVOLVNEX Maintenance | ₹6,000/mo (optional) | Client |

---

**Document Version:** 1.0 | **Created:** March 2026 | **EVOLVNEX**
