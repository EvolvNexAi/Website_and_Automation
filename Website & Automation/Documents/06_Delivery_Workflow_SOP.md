# EVOLVNEX - Delivery Workflow SOP

**Purpose:** Standard operating procedure for delivering client websites in 4-6 days

---

## Phase 1: Client Onboarding (Day 0)

### Checklist:
- [ ] Client fills onboarding form (Google Form/WhatsApp)
- [ ] Collect: Business name, services, contact info, photos, logo
- [ ] Confirm package tier (1/2/3)
- [ ] Confirm domain name preference
- [ ] Receive 50% advance payment
- [ ] Sign service agreement
- [ ] Create client folder (Google Drive)
- [ ] Assign Client ID: EVOL-2026-[XXX]

### Owner: Avishek/Ankur
### Output: Complete client brief ready for build

---

## Phase 2: AI Website Generation (Day 1-2)

### Step 1: Select Prompt Template
- Open `04_Base44_AI_Prompts.md`
- Choose template based on client type (Clinic/Salon/Cafe/Coaching/Real Estate)
- Fill in client details from onboarding form

### Step 2: Generate in Base44
- Login to Base44
- Start new project
- Paste prompt into Builder Chat
- Review generated site

### Step 3: Customize
- Adjust colors per client brand
- Upload client logo
- Replace placeholder images (if client provided)
- Update content with client info

### Step 4: Mobile Check
- Preview on mobile view
- Test all buttons (CTA, WhatsApp, phone)
- Ensure fast loading

### Owner: [Builder]
### Output: Draft website ready for client review

---

## Phase 3: Client Review (Day 3)

### Step 1: Share Preview
- Send Base44 preview link via WhatsApp
- Message template:
  ```
  Hi [Name], your website draft is ready!
  Preview: [link]
  Please review and share feedback within 24-48 hours.
  We include 2 rounds of revisions.
  Let us know:
  1. Design okay?
  2. Content accurate?
  3. Any changes needed?
  Thanks!
  ```

### Step 2: Collect Feedback
- Client reviews on their device
- Note all change requests
- Categorize: Design / Content / Functionality

### Step 3: Implement Revisions (Round 1)
- Make approved changes
- Update Base44 project
- Send revised preview

### Step 4: Final Review (Round 2 if needed)
- Client confirms final version
- Get written approval ("Looks good, proceed")

### Owner: Avishek/Ankur
### Output: Approved website ready for launch

---

## Phase 4: Domain & Hosting Setup (Day 4)

### Step 1: Domain Registration
- Purchase domain via Base44 or registrar
- Format: [clientbusiness].com or .in
- Cost: ₹800-1,500/year
- Register in client's name

### Step 2: Connect to Base44
- In Base44 dashboard: Settings → Custom Domain
- Add domain
- Update DNS records (Base44 guides this)
- Wait for propagation (2-24 hours)

### Step 3: SSL Activation
- Base44 auto-provisions SSL
- Verify HTTPS works
- Test all pages load securely

### Step 4: Hosting Verification
- Confirm site is live on Base44 hosting
- Test uptime
- Bookmark client dashboard

### Owner: [Tech Lead]
### Output: Live website with custom domain

---

## Phase 5: Feature Integration (Day 4-5)

### For Tier 1 (Website Only):
- [ ] Verify contact form works
- [ ] Test email notifications
- [ ] Check WhatsApp button
- [ ] Verify Google Maps embed
- [ ] Submit sitemap to Google Search Console (optional)

### For Tier 2 (Website + Chatbot):
- [ ] All Tier 1 checks
- [ ] Configure chatbot in Base44
- [ ] Upload client FAQ list
- [ ] Set lead capture fields (name, phone, email)
- [ ] Configure human handoff (WhatsApp/phone)
- [ ] Test chatbot with sample queries
- [ ] Set up lead dashboard
- [ ] Train client on chatbot monitoring

### For Tier 3 (Full Automation):
- [ ] All Tier 2 checks
- [ ] Set up WhatsApp Business API (Interakt/WATI/Gupshup)
- [ ] Client signs contract with API provider
- [ ] Configure automation flows:
  - Auto-reply to new leads
  - Booking confirmations
  - After-hours messages
- [ ] Connect CRM (Google Sheets/Airtable)
- [ ] Test end-to-end lead flow
- [ ] Set up analytics dashboard
- [ ] Train client on WhatsApp dashboard

### Owner: [Tech Lead]
### Output: All features functional and tested

---

## Phase 6: Training & Handoff (Day 5-6)

### Step 1: Schedule Training Call
- Book 30-min call (Tier 1) / 1 hour (Tier 2) / 2 hours (Tier 3)
- Send calendar invite with Base44 login details

### Step 2: Training Agenda
**Tier 1:**
- How to login to Base44
- How to update content
- How to view form submissions
- How to contact support

**Tier 2:**
- All Tier 1 topics
- Chatbot dashboard walkthrough
- How to view captured leads
- How to update FAQ list
- How to monitor chatbot performance

**Tier 3:**
- All Tier 2 topics
- WhatsApp automation dashboard
- How to view campaign analytics
- How to create broadcast campaigns
- CRM integration overview

### Step 3: Provide Documentation
- Share recorded training video (Loom/Zoom recording)
- Send quick reference guide (1-pager)
- Share WhatsApp support group link

### Step 4: Final Payment
- Send invoice for remaining 50%
- Receive payment
- Confirm receipt

### Step 5: Go-Live Announcement
- Message template:
  ```
  🎉 Your website is LIVE!
  URL: [www.clientdomain.com]
  Login: [Base44 credentials]
  Support: [Your WhatsApp]
  Thanks for choosing EVOLVNEX!
  ```

### Owner: Avishek/Ankur
### Output: Client trained, site live, payment complete

---

## Phase 7: Post-Launch Support (Day 7-30)

### Warranty Period (30 Days):
- [ ] Monitor uptime (Base44 dashboard)
- [ ] Respond to support tickets within 24 hours
- [ ] Fix any bugs free of cost
- [ ] Help with minor content tweaks
- [ ] Check in at Day 15: "Everything working well?"

### Handoff to Maintenance (After 30 Days):
- Offer maintenance plan
- If client opts in:
  - Add to maintenance client list
  - Set up monthly check-ins
  - Schedule monthly updates
- If client opts out:
  - Pay-per-support (₹500/hour)
  - Self-manage via Base44

### Owner: [Support Lead]
### Output: Happy client, recurring revenue or closed project

---

## Turnaround Time Summary

| Phase | Duration | Owner |
|-------|----------|-------|
| Onboarding | Day 0 | Both |
| AI Build | Day 1-2 | Builder |
| Client Review | Day 3 | Both |
| Domain/Hosting | Day 4 | Tech |
| Feature Setup | Day 4-5 | Tech |
| Training/Handoff | Day 5-6 | Both |
| **Total** | **4-6 days** | - |

---

## Tools Used

| Tool | Purpose | Cost |
|------|---------|------|
| Base44 | Website builder + hosting | Client pays |
| Google Forms | Client onboarding | Free |
| Google Drive | Client file storage | Free |
| WhatsApp Business | Client communication | Free |
| Razorpay | Payment collection | 2% per txn |
| Loom/Zoom | Training recording | Free |
| Google Search Console | SEO submission | Free |

---

## Quality Checklist (Before Launch)

- [ ] All pages load correctly
- [ ] Mobile view tested
- [ ] All CTAs working (phone, WhatsApp, forms)
- [ ] Domain connected + SSL active
- [ ] Chatbot tested (if Tier 2/3)
- [ ] WhatsApp automation tested (if Tier 3)
- [ ] Form submissions working
- [ ] Client trained
- [ ] Final payment received
- [ ] Support group added

---

**Document Version:** 1.0 | **Created:** March 2026 | **EVOLVNEX**
