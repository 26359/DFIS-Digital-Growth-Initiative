# DFIS Website Prompt — Intelligent Coverage Companion

## Project Overview

Build a modern, trust-focused website for **DFIS** (Daher Financial Insurance Services), a U.S.-based insurance and financial-services agency. The website must do more than display information — it must function as an interactive digital tool that educates visitors, captures qualified leads, and connects users with the right human agent.

**Primary Goal:** Transform the website from a passive brochure into an active lead-generation and education platform.
**Budget Constraint:** Zero incremental cost at MVP stage. Use existing technology stack and no paid third-party integrations unless explicitly approved.
**Compliance Requirement:** All insurance-related content must be educational only. No automated quotes, no binding coverage, no definitive policy interpretations. All AI outputs must use DFIS-approved content with clear boundaries.

---

## Brand Voice & Tone

- **Professional but approachable** — like a knowledgeable agent explaining coverage in plain English
- **Trustworthy and transparent** — no fine-print surprises, clear disclaimers
- **Empathetic and human** — acknowledges that insurance decisions are personal and sometimes stressful
- **U.S.-focused** — all examples, laws, and references align with U.S. insurance norms and regulations
- **No jargon without explanation** — if a term like "deductible" or "rider" appears, it must be defined in plain English

---

## Core Innovation: DFIS Coverage Compass™

**Tagline:** *Understand your coverage. Identify what to review. Connect with the right professional.*

Coverage Compass™ is the signature interactive feature of the website. It replaces a static contact form with a guided digital journey that produces context-rich leads for DFIS agents.

### Coverage Compass Architecture

```
                 DFIS WEBSITE
                      │
                      ▼
             ┌─────────────────┐
             │ Coverage Compass│
             └────────┬────────┘
                      │
             Quick Assessment
                      │
          ┌───────────┼───────────┐
          ▼           ▼           ▼
       Auto        Home       Life/Family
          │           │           │
          └───────────┼───────────┘
                      ▼
             Educational Results
                      │
              AI Q&A / Resources
                      │
                      ▼
              Lead Information
                      │
             ┌────────┴────────┐
             ▼                 ▼
       Book an Agent       Request Contact
```

### Step 1 — Quick Assessment

The visitor answers a short series of simple, non-intrusive questions. The form must feel like a conversation, not a legal document. Questions include:

- **Individual / Family / Business** — coverage scope
- **Homeowner / Renter** — property status
- **Vehicle ownership** — auto coverage need
- **Current insurance status** — already covered or shopping
- **Major financial priorities** — protection goals
- **Life stage** — young professional, family, retirement, etc.
- **Preferred contact method** — phone, email, text, or online booking

**UX Requirement:** Progress indicator. Allow save-and-resume. No required fields beyond what is necessary to generate a useful checklist.

### Step 2 — Personalized Coverage Checklist

Based on the visitor's answers, generate an educational checklist titled:

> **Your DFIS Coverage Checkup**
> *Areas you may want to review*

Checklist categories (selected dynamically based on assessment):

- Auto insurance
- Homeowners / renters insurance
- Life insurance
- Health-related protection
- Business protection
- Umbrella / liability coverage
- Disability insurance
- Long-term care considerations

**Questions to discuss with an agent** (always included):

- What risks am I currently protected against?
- What exclusions should I understand?
- Are my current limits still appropriate?
- Have any recent life changes affected my coverage?

**Important:** The checklist is educational. It does not recommend a specific policy, carrier, or coverage amount. It identifies areas the visitor should review with a professional.

### Step 3 — AI Education

After receiving the checklist, the visitor can ask questions in plain English. Example prompt:

> *"I just bought a house. What types of insurance should I understand?"*

The AI companion:

- Explains insurance concepts using DFIS-approved educational material
- References relevant checklist items
- Provides links to DFIS resources, articles, or glossaries
- Never recommends a specific policy, carrier, or premium amount
- Never provides definitive coverage advice or legal interpretations
- Discloses clearly: *"This is educational information, not personalized insurance advice. A DFIS agent can help you determine what's right for your situation."*

**Technical Approach (MVP):** Rule-based response system with DFIS-approved content blocks. No external AI API required. Responses are structured, reviewed, and maintained by DFIS. This avoids compliance risk and keeps the solution at $0 incremental cost.

### Step 4 — Human Agent Handoff

At the end of the Coverage Compass journey, the visitor is presented with clear options:

> **Want to review your situation with a DFIS professional?**
>
> 📅 Book an appointment  
> 📞 Request a callback  
> 📋 Submit your information

The agent receives a structured summary including:

- Assessment answers
- Generated coverage checklist
- AI questions asked during the session
- Visitor contact preferences and timing

This gives the agent context before the first conversation, improving the quality of the interaction and reducing repetitive intake questions.

---

## Website Structure

### Homepage

- **Hero section:** Clear value proposition. "Coverage Compass™ — Understand your coverage. Identify what to review. Connect with the right professional."
- **Coverage Compass CTA:** Prominent button: "Start Your Free Coverage Checkup"
- **Trust signals:** Testimonials, licenses, carrier partnerships, community presence
- **Service overview:** Auto, Home, Life, Business — with educational descriptions
- **Why DFIS:** Differentiators (local, personal, educational approach)
- **Footer:** Contact info, licenses, disclaimers, privacy policy

### Coverage Compass Page

- Full interactive experience (Steps 1–4 as described above)
- Branded with DFIS logo, colors, and tone
- Mobile-responsive
- Accessible (WCAG 2.1 AA minimum)
- Shareable URL for saved progress (optional at MVP)

### Resources / Learn Page

- Insurance glossary
- Blog / articles (educational, DFIS-approved)
- FAQ section
- Video library (optional)
- Checklist downloads (PDF)

### About Page

- DFIS story and mission
- Agent profiles with photos and bios
- Community involvement
- Carrier partnerships

### Contact Page

- Traditional contact form (for visitors who skip Coverage Compass)
- Phone number, email, address, hours
- Map embed
- Request callback form

---

## Design Requirements

### Visual Style

- Clean, modern, professional
- Blue / navy primary palette (trust, stability) with warm accent color (approachability)
- Generous white space
- High-quality, relevant photography (local community, not stock clichés)
- Mobile-first responsive design
- Fast load times (under 3 seconds on 4G)

### Typography

- One primary sans-serif font family (e.g., Inter, Open Sans, or similar)
- Clear hierarchy: H1 for value props, H2 for sections, H3 for subsections
- Body text minimum 16px for readability
- Line height 1.5–1.6 for comfortable reading

### Imagery

- Authentic, diverse, U.S.-based
- Show real people in relatable situations (family at home, small business owner, etc.)
- Avoid generic corporate stock photography
- Icons for service categories (auto, home, life, business)

---

## Technical Requirements

### Platform

- WordPress or equivalent CMS (use existing if available)
- Custom theme or child theme to match DFIS branding
- No mandatory page builder dependencies that lock the site into a specific tool

### Coverage Compass Implementation

- Multi-step form with conditional logic (show/hide questions based on prior answers)
- Results generated dynamically from a structured content database
- AI Q&A component: rule-based with DFIS content blocks (no external AI service required)
- Lead data stored securely and routed to DFIS CRM or email
- GDPR / CCPA compliant data handling (if applicable)
- SSL required

### Performance & SEO

- Semantic HTML5
- Schema markup for LocalBusiness and FAQ
- Meta descriptions and Open Graph tags on all pages
- Image optimization (WebP, lazy loading, alt text)
- Sitemap and robots.txt
- Google Analytics 4 or equivalent (privacy-compliant)
- Fast hosting with CDN

### Accessibility

- WCAG 2.1 AA compliance
- Keyboard navigation support
- Screen reader tested
- Color contrast ratios meet standards
- Form labels and error messages accessible

### Security

- Regular WordPress / CMS updates
- Security plugin configured
- HTTPS enforced
- Contact forms protected against spam (honeypot + rate limiting)
- No sensitive data exposed in URLs or client-side code

---

## Content Rules

### Insurance Compliance

- No promise of specific coverage outcomes
- No comparison of carriers that could be construed as unfair or deceptive
- All rates and availability statements qualified with "may vary" or "subject to underwriting"
- Clear distinction between educational content and personalized advice
- Privacy policy and terms of service visible and accessible

### AI Content Boundaries

The AI Q&A component MUST include the following disclosure and MUST NOT:

- ✅ Use only DFIS-approved educational content
- ✅ Explain insurance concepts in plain English
- ✅ Direct users to human agents for personalized advice
- ✅ Disclose that it is educational, not advisory
- ❌ Recommend a specific policy, carrier, or coverage amount
- ❌ Provide definitive coverage interpretations
- ❌ Generate automated quotes or bind coverage
- ❌ Store or misuse visitor personal data

**Required disclosure text (displayed on AI Q&A section):**
> *"Coverage Compass AI provides educational information only. It is not a substitute for personalized insurance advice. A DFIS agent can help you understand what coverage is right for your situation."*

---

## Success Metrics (Post-Launch)

- Coverage Compass completion rate (target: >40% of visitors who start the assessment complete it)
- Lead quality score (agent feedback on incoming leads)
- Time on site (expect increase vs. current site)
- Mobile vs. desktop usage (ensure mobile experience is equal or better)
- Organic search traffic growth
- Agent feedback on lead context usefulness

---

## Deliverables

1. **Website Design Mockups** — Homepage, Coverage Compass, Resources, About, Contact
2. **Coverage Compass Interactive Prototype** — Working demo of the assessment flow
3. **AI Content Database** — Structured DFIS-approved educational content blocks for Q&A component
4. **Full Website Build** — Responsive, accessible, SEO-optimized, production-ready
5. **Agent Dashboard** (optional MVP) — Simple interface for agents to view lead submissions from Coverage Compass
6. **Documentation** — Content update guide, CMS user guide, maintenance checklist

---

## Prompt Summary for AI Website Generation

> Build a modern, U.S.-focused insurance agency website for **DFIS** with a signature interactive feature called **Coverage Compass™**.
>
> Coverage Compass™ is a free, guided digital tool that:
> 1. Asks visitors simple questions about their insurance needs (individual/family/business, home/rent, auto, life stage, etc.)
> 2. Generates a personalized educational coverage checklist (not a policy recommendation)
> 3. Offers an AI Q&A component that explains insurance concepts in plain English using DFIS-approved content, with clear boundaries against giving personalized advice
> 4. Connects the visitor to a human DFIS agent through appointment booking, callback requests, or contact forms — delivering the visitor's context to the agent so they start the conversation informed
>
> The website should feel trustworthy, educational, and modern. The AI component must include clear disclosures that it is educational only and not a substitute for personalized insurance advice. No automated quotes, no binding coverage, no definitive policy interpretations.
>
> Tagline: *"Understand your coverage. Identify what to review. Connect with the right professional."*
>
> Design: Clean, professional, mobile-first, blue/navy palette with warm accents. WCAG 2.1 AA accessible. Fast load times. SEO optimized.
>
> Technical: Use existing CMS if available. Rule-based AI content for MVP (no external AI API). Secure, compliant, spam-protected forms. SSL required.

---

*Document prepared for DFIS Digital Growth Initiative*
*Coverage Compass™ is a signature product concept for DFIS*
