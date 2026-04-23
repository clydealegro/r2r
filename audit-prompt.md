# CRO AUDIT MASTER PROMPT
# Version 2.4 — Persona Threading + Sticky Nav Layer Added
# Use this entire document as your prompt. Paste it, then provide inputs below.

---

## 🚨 STEP 0 — MANDATORY PRE-EXECUTION (DO THIS FIRST, ALWAYS)

Before doing ANYTHING else, you MUST execute the following steps in order.
These are not optional. Do not skip them. Do not proceed to the audit until all are complete.

**STEP 0A — READ THE SKILL FILE:**
Use the `view` tool to read `/mnt/skills/public/frontend-design/SKILL.md`
This file contains the design system rules you MUST follow when building the HTML report.
Confirm you have read it before proceeding.

**STEP 0B — CONFIRM INPUTS:**
Confirm that BOTH of the following are present before starting:
- ✅ Screenshot (image) — REQUIRED
- ✅ Context block (filled in below) — REQUIRED
- ⚙️ HTML — Optional but use it if provided

If either required input is missing, stop and ask for it. Do not proceed without both.

**STEP 0C — IDENTIFY BUYER PERSONAS:**
Before calibrating the copy register, identify the distinct buyer personas for this product.
A persona is a specific role at a specific company type with a specific primary anxiety —
not a demographic profile or a made-up name.

For each persona, extract or derive:
- **Role and seniority** — specific title and level, not "senior decision-maker"
- **Company type and size signal** — e.g. AUM, ARR, headcount, industry vertical
- **Primary anxiety** — the specific pain that makes them look for this product
- **Buying trigger** — the event that makes them act now rather than next quarter
- **Vocabulary** — the exact terms they use that must appear on the page
- **Three questions before converting** — the specific objections that block the booking
- **Urgency hook** — the real calendar event or deadline that creates genuine time pressure

**Sources:** Use the context block first. Then cross-reference the page's existing case study
attributions, testimonial roles, and vertical-specific copy from the HTML and screenshot.
If the context block field says "Derive from context," use the page content as your source.

**Rules:**
- Minimum 2 personas, maximum 4. Most B2B products have 2–3 distinct buyer types.
- Do not invent roles, company types, or anxieties not supported by the inputs.
- Do not use fictional names (no "Derek the Data Director").
- Each persona must be meaningfully different — different anxiety, different urgency hook,
  different questions. If two personas have identical anxieties, they are one persona.

Confirm personas identified before proceeding to Step 0D.

**STEP 0D — CALIBRATE COPY REGISTER:**
Before writing a single line of copy, extract from the context block:
- **Industry / niche** — What sector is this? (e.g. ESG consulting, SaaS, fintech, marketplace)
- **Audience** — Who is the buyer? What is their role, seniority, and primary anxiety?
- **Traffic source** — Where are visitors coming from? (cold paid traffic vs. warm referral vs. branded search changes copy posture entirely)
- **Goal** — What is the conversion event? (lead form, demo request, purchase, sign-up)

Use these four inputs to set the copy register for the entire audit BEFORE producing any copy rewrites.
Confirm your register calibration in a brief internal note before proceeding.
See Section 2.5 — Strategic Copy Standards for the full calibration framework.

---

## 🚨 STEP 0E — MANDATORY OUTPUT FORMAT

You MUST always produce a downloadable HTML file as the final deliverable.
This is NOT optional and is NOT negotiable under any circumstances.

**Execution steps for the file:**
1. Use `create_file` to write the complete HTML to `/home/claude/cro-audit-[clientname].html`
2. Use `present_files` to deliver it to the user
3. The file must implement the full Design System defined in Section 9 of this prompt
4. The file must contain ALL 8 report sections — no sections may be skipped or merged

Do not output the audit as text in the chat.
Do not output the audit as markdown.
The ONLY valid output format is the downloadable HTML file.

---

## 📥 INPUT FORMAT

Screenshot:
[Attach image]

Context:
- Product name:
- What it does:
- Target audience: (include role, seniority, and primary anxiety if known)
- Industry / niche: (be specific — e.g. "ESG consulting" not just "consulting")
- Traffic source: (e.g. cold paid, branded search, warm referral, organic SEO)
- Goal of the page: (e.g. book a discovery call, request a demo, sign up free)
- Buyer personas / ICP segments: (list known sub-segments with role, seniority, company type, and primary anxiety — e.g. "Head of Operations at hedge funds, VP Technology at mid-market PE firms." If unknown, write "Derive from context.")
- Notes / constraints:

HTML (Optional):
[Paste HTML or leave blank]

---

## 🎯 PRIMARY OBJECTIVE

Deliver a comprehensive CRO audit covering UX, messaging, structure, and conversion strategy.
The output must be a production-grade, visually polished HTML report that:
- Identifies what's working and what's broken
- Grounds every finding in the specific buyer personas the page must convert
- Improves messaging and UX with specific rewrites built on conversion copywriting principles
- Prioritizes changes by conversion impact and persona relevance
- Provides a clear visual blueprint for implementation
- Looks and feels like a premium agency deliverable

---

## 🚨 MANDATORY AUDIT AREAS (ALL 10 — NEVER SKIP)

You MUST audit ALL 10 of the following areas.
DO NOT skip, merge, rename, or replace any of them.

1. Hero / Above the Fold
2. Messaging Clarity
3. Social Proof
4. CTA Strategy
5. Page Flow & Structure
6. Trust & Credibility
7. Visual Design / UX
8. Objection Handling
9. Audience Segmentation
10. Urgency / Compliance Hook

---

## 📊 SECTION 1 — CRO PERFORMANCE DASHBOARD

For EACH of the 10 areas, produce a dashboard card containing:

- Area name
- Score: X/10
- Visual score bar (CSS width % = score × 10)
- Status: 🟢 Strong (8–10) | 🟡 Needs Work (5–7) | 🔴 Critical (1–4)
- Key Insight: 1–2 sharp sentences, specific to this page

Then output:
- OVERALL SCORE: Sum of all 10 area scores (max 100)
- Verdict: Strong (75+) | Needs Work (50–74) | Critical (<50)
- Score summary: count of Critical / Needs Work / Strong areas — verify this count against actual scores before writing it
- 1–2 sentence overall assessment

---

## 👤 SECTION 2 — BUYER PERSONAS

Position: After Dashboard (Section 1), before Detailed Analysis (Section 3).
Section label in the HTML: "02 — Buyer Personas"

This section reframes all subsequent findings through the lens of who the page must convert.
Every persona is grounded in the context block, the page's existing case study attributions,
testimonial roles, and vertical-specific copy. No invented roles or anxieties.

**For each persona, produce a card containing:**

HEADER:
- Persona number
- Role + company type (e.g. "Head of Operations / COO · Multi-Strategy Hedge Fund · $5B–$50B AUM")
- "Page serves this persona" rating: Poorly / Partially / Well

ATTRIBUTES GRID (2-column):
- Primary Anxiety
- Buying Trigger
- Decision Process
- Vocabulary (the exact terms this persona uses that must appear on the page)

THREE QUESTIONS BEFORE THEY BOOK:
Specific, role-relevant questions this persona needs answered before clicking the CTA.
Not generic objections — specific to this role, this company type, this product.
Formatted with a question marker per item.

URGENCY HOOK:
The real calendar event, regulatory deadline, or operational trigger that creates genuine
time pressure for this persona. Connected directly to the urgency recommendations in Area 10.

PAGE ASSESSMENT (2–3 sentences):
How well the current page serves this persona. Reference specific page elements by name.
State exactly what's missing for this persona. Tag which audit areas are most critical.

**After all persona cards, produce a PERSONA × AUDIT AREA PRIORITY MATRIX:**
A table mapping each persona against all 10 audit areas.
Per-cell priority: CRITICAL / HIGH / MEDIUM
- CRITICAL: this area directly addresses the persona's primary anxiety or buying trigger
- HIGH: this area addresses a significant secondary concern for this persona
- MEDIUM: this area matters but is not the deciding factor for this persona

Every cell must be justifiable from the persona card. Do not assign CRITICAL uniformly.
The matrix gives the client a persona-filtered implementation sequence.

**Quality rules for this section:**
- Minimum 2 personas, maximum 4
- Each persona grounded in context block or page content — no invented profiles
- Each persona must be meaningfully distinct (different anxiety, different urgency hook)
- Do not use fictional names
- The "Page serves this persona" rating must be honest — most pages serve 0–1 personas well
- Page Assessment must name specific page elements, not speak in generalities

---

## 🧩 SECTION 3 — DETAILED ANALYSIS (ALL 10 AREAS)

For EACH of the 10 areas use this exact structure:

---
[AREA NAME]
Score: X/10
Status: 🟢 / 🟡 / 🔴

Summary:
- 2–4 sentence paragraph. Specific to this page. No generic filler.

What's Working:
- Bullet list. Specific observations only. Min 2, max 6.

Issues:
- Bullet list. Each issue must be specific and actionable. Min 2, max 8.
- All spatial, technical, and factual claims must be verified against the HTML
  and screenshot before inclusion. Do not infer rendering behavior from CSS class
  names alone — verify against what is actually visible.

Solutions:
- Each issue MUST have a corresponding direct fix.
- ALL copy rewrites must conform to the Strategic Copy Standards defined in Section 2.5.
  Apply the calibrated register from Step 0D. Do not write copy before reading Section 2.5.
- Write actual copy rewrites where relevant — not instructions.
  e.g. Instead of "improve the headline" → write the improved headline using the correct
  headline type from the Headline Taxonomy in Section 2.5.
- Every CTA rewrite must follow the CTA Engineering framework in Section 2.5.
- Every claim-heavy copy block must apply the Credibility Architecture rules in Section 2.5.
- **Persona threading:** Where a solution primarily serves one or two personas rather than all,
  tag it inline using this format: `(Primary: P1 · Secondary: P2)`. Only tag where personas
  have meaningfully different priorities for that fix — do not tag solutions that serve all
  personas equally. The tag appears after the solution bullet text, before the copy-tag.
  Examples of when to tag: a Bloomberg-specific diagram fix → Primary: P1; a diligence
  case study move → Primary: P2; a regulatory FAQ addition → Primary: P3.
  Examples of when NOT to tag: rewriting the hero H1 (all personas benefit equally);
  adding friction-reduction microcopy to the CTA (all personas benefit equally).

Estimated Conversion Impact:
- Impact Range: +X% to +Y% (realistic, not inflated)
- Confidence: High / Medium / Low
- Reasoning: Why this area affects conversion at this funnel stage

Why It Matters:
- 1–2 sentences connecting this area to revenue/lead outcomes
---

### 3A — HERO VISUAL ELEMENT RECOMMENDATIONS (MANDATORY SUB-SECTION)

Inside the Hero / Above the Fold detailed analysis card, after the Solutions list and before
the Impact Box, you MUST include a dedicated visual element recommendation block.

This block addresses the RIGHT-SIDE VISUAL or primary hero imagery.

**Format:** A visually distinct panel containing:

1. **Context line:** 1–2 sentences describing what the current hero visual is and why it fails to convert.

2. **Three recommended visual approaches**, each containing:
   - **Title** — Clear name for the approach
   - **Description** — 3–5 sentences covering: what the visual IS, WHY it drives conversion,
     how it answers a specific visitor question, any dynamic/personalization opportunities

**Quality rules:**
- Each recommendation must be specific to the product category — no generic "add a better image" advice
- At least one recommendation should involve PRODUCT UI
- At least one recommendation should involve SOCIAL PROOF as a visual element
- At least one recommendation should involve a DATA VISUALIZATION or COMPARISON
- Every recommendation must explain the conversion reasoning, not just describe the visual
- Do not recommend stock photography replacements

---

## ✍️ SECTION 2.5 — STRATEGIC COPY STANDARDS

This section defines the copywriting framework that governs ALL copy produced in this audit.
Every headline, subheadline, CTA, body copy block, microcopy, and objection response
written anywhere in this report must conform to these standards.

Do not begin writing copy until you have read this section in full.

---

### 2.5A — COPY PHILOSOPHY (GOVERNING PRINCIPLES)

**1. Specificity beats vagueness — always.**
"Reduce compliance risk by 40%" is more credible and more persuasive than "reduce compliance risk."
When rewriting copy, the first question is always: what is the most specific, true thing we can say here?

**2. Outcome-first framing.**
Visitors do not buy products or services. They buy the outcome of using them.
Copy must lead with what the buyer gains, avoids, or becomes — not what the product does.

**3. The "So What" test.**
Every claim must survive the "so what?" challenge.
"We use AI-powered analysis" → so what? → "your audit is ready in 48 hours, not 3 weeks."
Keep asking "so what" until you reach a concrete, personally relevant outcome for the buyer.

**4. Clarity before cleverness.**
A clear headline that converts beats a clever one that confuses.
If a visitor cannot understand what the page offers within 5 seconds, the copy has failed.

---

### 2.5B — HEADLINE TAXONOMY

**CONTRAST HEADLINE**
- Job: Open a gap between current state and desired state
- Structure: "[Current painful reality] — [New possibility]"
- When to use: Hero H1 when the audience has a clear, known frustration
- Example: "Compliance Audits Used to Take 6 Weeks. Ours Take 6 Days."

**PROOF HEADLINE**
- Job: Lead with a verifiable result to establish credibility immediately
- Structure: "[Specific metric] [outcome verb] [timeframe/qualifier]"
- When to use: Hero H1 when the client has strong quantified results; warm traffic
- Example: "173 ESG Reports Delivered. Zero Missed Deadlines."

**BENEFIT-FORWARD HEADLINE**
- Job: State the primary value proposition as a direct benefit to the reader
- Structure: "[You/Your] + [specific outcome] + [speed or ease signal]"
- When to use: Hero H1 for cold traffic; section intros
- Example: "Your ESG Framework, Board-Ready in 2 Weeks"

**URGENCY HEADLINE**
- Job: Activate time-pressure without manufactured scarcity
- Structure: "[Real deadline/event] + [consequence of missing it]"
- When to use: Hero or BOFU CTA sections; compliance-driven niches
- Example: "CSRD Reporting Opens in Q1. Are Your Disclosures Ready?"

**CURIOSITY HEADLINE**
- Job: Create an information gap that makes the visitor want to read on
- Structure: "[Counter-intuitive or incomplete claim] — [resolution below the fold]"
- When to use: Mid-page section intros; blog-to-landing page bridges
- Example: "Most ESG Consultants Are Solving the Wrong Problem"

**Selection rule:** Match headline type to funnel stage and audience temperature.
- Cold traffic → Benefit-Forward or Contrast
- Warm traffic (knows the category) → Proof or Urgency
- Retargeting / already-engaged → Urgency or Curiosity
- Mid-page section headers → Benefit-Forward or Curiosity

---

### 2.5C — CTA ENGINEERING

**Rule 1 — First-person ownership language.**
- ❌ "Get Started" → ✅ "Start My Assessment"
- ❌ "Book a Call" → ✅ "Book My Strategy Session"
- ❌ "Learn More" → ✅ "See How It Works"

**Rule 2 — Value-forward over action-forward.**
- ❌ "Submit" → ✅ "Get My Free ESG Gap Analysis"
- ❌ "Sign Up" → ✅ "Claim My Compliance Roadmap"

**Rule 3 — Friction-reduction signals.**
Pair primary CTAs with a single line of microcopy that removes the biggest perceived risk.
The microcopy line should address the most likely objection for this funnel stage.

**Rule 4 — CTA hierarchy.**
Every page section needs at most one primary CTA and optionally one secondary CTA.
Never put two primary CTAs of equal visual weight side by side. One must dominate.

**Rule 5 — CTA-to-offer alignment.**
The CTA wording must precisely match what happens next.
If clicking leads to a calendar booking, say "Book" — not "Get Started."

---

### 2.5D — FUNNEL-STAGE CALIBRATION

**TOFU — Top of Funnel (Problem Aware, Not Solution Aware)**
Copy job: educate, empathize, name the problem precisely, introduce the category
Tone: teaching, not pitching | Best headline types: Contrast, Benefit-Forward

**MOFU — Middle of Funnel (Solution Aware, Evaluating Options)**
Copy job: differentiate, demonstrate, prove, address objections, show results
Tone: confident, specific, proof-driven | Best headline types: Proof, Benefit-Forward, Curiosity

**BOFU — Bottom of Funnel (Purchase/Conversion Ready)**
Copy job: confirm the right choice, reduce perceived risk, simplify the next step, close
Tone: reassuring, direct, low-pressure but clear | Best headline types: Urgency, Proof

**Traffic source calibration:**
- Cold paid traffic → assume TOFU regardless of page position
- Branded search → assume MOFU/BOFU
- Warm referral → assume MOFU
- Organic SEO → depends on keyword intent

---

### 2.5E — CREDIBILITY ARCHITECTURE

**Specificity as proof.**
Specific claims are more credible than general ones, even when the specific claim is stronger.

**Qualifier placement.**
Place believability signals immediately adjacent to ambitious claims — not at the bottom of the page.

**Proof integration, not proof segregation.**
Testimonials and case study stats woven into narrative copy are more effective than isolated proof sections.

**The believability stack.**
When making a significant claim, deploy at least two of these in close proximity:
1. Specific metric or number
2. Named client, industry, or recognizable outcome
3. Mechanism (brief explanation of how/why it works)
4. Social signal (number of clients, volume, reviews)
5. Risk reversal (guarantee, free first step, no-commitment offer)

**Jargon calibration.**
Industry-specific language signals expertise to in-category buyers (MOFU/BOFU) and alienates out-of-category buyers (TOFU).
When in doubt, lead with the outcome, follow with the mechanism.

---

### 2.5F — VOICE & REGISTER SYSTEM

**REGISTER: B2B Professional Services (Consulting, Legal, Compliance)**
- Authority signaling over enthusiasm
- Precision over aspiration
- Risk-reduction language prominent
- Short sentences. Declarative tone. No exclamation points.
- Avoid: "game-changing," "revolutionary," "passionate," "holistic"

**REGISTER: ESG / Sustainability Consulting**
- Reference real frameworks (CSRD, GRI, TCFD, EU Taxonomy) by name
- Avoid greenwashing-adjacent language
- Lead with compliance urgency and reputational risk reduction
- Pair technical credibility with implementation specificity

**REGISTER: B2B SaaS**
- Feature-benefit pairing: name the feature, immediately follow with its outcome
- Speed and ease signals prominent
- Integration and compatibility are high-anxiety topics — address proactively
- Social proof format: number of users, G2/Capterra ratings, named enterprise logos

**REGISTER: B2C Marketplace / Consumer**
- Conversational, warm, accessible
- Price transparency or savings framing prominent
- Community and peer validation powerful
- Speed and simplicity signals prominent

**Register selection rule:**
If the client's niche doesn't match one exactly, identify the closest match and note the delta.
For hybrid niches, blend the relevant registers with the primary buyer profile as the anchor.

---

## 🚀 SECTION 4 — HIGH-IMPACT ACTION PLAN

Group ALL recommendations into three priority tiers:

**P0 — Immediate (highest impact, fix first)**
**P1 — Important (high return, fix second)**
**P2 — Nice to Have (incremental, fix third)**

For each recommendation include:
- Sequential index number
- Action name (specific, not vague)
- Impact range (+X–Y%)
- Short justification (1 sentence)

All copy-related action items must reference which Strategic Copy Standard (2.5A–F) applies.
Example: "Rewrite hero H1 using Contrast Headline structure (§2.5B) with ESG Register (§2.5F)"

Where a recommendation primarily serves specific personas, note which: (P1) (P2) (P3) etc.

**Mandatory P1 action item — Persona self-selection routing:**
Every audit with 2+ personas MUST include a P1 action item for adding a persona
self-selection mechanism to the hero or navigation area. This is the structural fix
that makes all other persona-specific recommendations implementable — without a routing
mechanism, the client cannot serve persona-specific copy to the right visitor.
Format: "Add Persona Self-Selection Row to Hero — [label 1] / [label 2] / [label 3]"

---

## 🎯 SECTION 5 — VISUAL PAGE RECONSTRUCTION (TOP → BOTTOM)

Produce a wireframe-style visual layout of the RECOMMENDED page.
Work section by section from top to bottom.

ALL copy in wireframes must conform to the Strategic Copy Standards in Section 2.5.
Headlines must use a named headline type from the Taxonomy (§2.5B).
CTAs must apply the CTA Engineering rules (§2.5C).
Any claim-bearing copy must follow the Credibility Architecture (§2.5E).
Register must match the calibration set in Step 0D (§2.5F).

For each section block include:
- Section label
- Wireframe content blocks showing:
  - Rewritten headlines (actual copy, not placeholders) — label headline type used
  - Rewritten subheadlines (actual copy)
  - CTA button wording + microcopy line beneath
  - Supporting elements (trust chips, stat bars, logos, steps, etc.)
- Aligned Areas: list which of the 10 audit areas this section addresses
- Estimated Impact: +X–Y%

**Persona routing element (MANDATORY in Hero wireframe):**
The Hero wireframe MUST include a persona self-selection row positioned between the
navigation bar and the hero headline. Format: a compact inline selector row reading
"I work in: [Persona 1 label] [Persona 2 label] [Persona 3 label]" with each option
as a distinct clickable chip. This element routes visitors to persona-specific hero copy
and can also be triggered via UTM parameter on inbound links.

**Persona H1 variants (MANDATORY in Hero wireframe):**
After the primary H1 (which should be optimized for the highest-priority or broadest
persona), include a clearly labeled variants block showing persona-specific H1 alternatives.
Format: for each persona, show the variant H1 with:
- A persona label (e.g. P1 — HEDGE FUND OPERATIONS)
- The variant headline text
- A one-line note on which headline type it uses and why it works for this persona

The variants block is a reference for the client's development implementation —
it shows which copy to serve based on the self-selection or UTM signal.

Sections to always include (add more if the page warrants):
1. Hero Section
2. Trust Bar (stats + logos)
3. How It Works
4. Service / Product Section
5. Social Proof / Testimonials
6. Objection Handling / FAQ
7. Final CTA Section

**IMPORTANT — Fabricated Statistics Caveat:**
If wireframes include specific numbers not verifiable from the provided inputs, add a visible
caveat at the top of Section 5 stating they are illustrative estimates to be replaced with
verified metrics before implementation.

---

## 🔁 SECTION 6 — RECOMMENDED PAGE FLOW (VISUAL COMPARISON)

Produce a side-by-side comparison: Current Flow vs Recommended Flow.

Use this narrative framework for the Recommended Flow:
Problem Awareness (TOFU) → Pain Amplification → Solution Introduction
→ How It Works (MOFU) → Proof & Social Validation → Objection Handling
→ Urgency / Compliance Hook → Primary CTA (BOFU)

For the Current Flow:
- Map out what the page actually does, in order
- Mark broken steps with [BROKEN] or [MISSING]
- Add short notes where the flow fails

For the Recommended Flow:
- Mark new sections with [NEW]
- Mark updated sections with [UPDATED]
- Keep existing sections that work marked as [KEEP]

The recommended flow must be consistent with the flow described in Section 3 (Detailed Analysis
Area 05) and Section 4 (Action Plan). All three references to page flow must match exactly.

---

## ✅ SECTION 7 — WHAT'S WORKING VS WHAT'S BROKEN

Two-column visual comparison:

What's Working ✅          |  Critical Issues ❌
- Bullet list              |  - Bullet list
- Minimum 6 items each     |  - Minimum 6 items each
- Specific observations    |  - Specific problems

Only include items that are grounded in the HTML or screenshot.
Do not list an issue as broken if it has not been verified.

---

## 🎯 SECTION 8 — THE 3 BIGGEST BETS

One strategic summary paragraph (2–3 sentences, sharp assessment).

Then 3 strategic bets in this exact format:

Bet [N] — [High-impact change title]
- What to change: [Specific action]
- Why it matters: [Buyer psychology / conversion reasoning]
- Expected impact: +X–Y%
- Copy standard applied: [Reference §2.5A–F if copy is involved]
- Primary persona: [Which persona/s this bet primarily converts, and why the others
  are secondary or served by a different bet. Use format: "PRIMARY: P1 · HIGH: P2"
  or "PRIMARY: P2 · PRIMARY: P3" for bets that equally serve two personas.
  Explain the persona-specific logic in 1–2 sentences.]

Focus on highest-leverage, highest-confidence changes only.
Think like a growth strategist, not a checklist auditor.

---

## 🎨 SECTION 9 — MANDATORY DESIGN SYSTEM FOR HTML OUTPUT

### 9A — CSS Variables (copy exactly)
```css
:root {
  --bg: #0b0d0f;
  --surface: #131618;
  --surface2: #1a1d21;
  --border: #252a2f;
  --green: #45A735;
  --green-dim: rgba(69,167,53,0.12);
  --green-mid: rgba(69,167,53,0.25);
  --red: #f04747;
  --red-dim: rgba(240,71,71,0.12);
  --amber: #f5a623;
  --amber-dim: rgba(245,166,35,0.12);
  --text: #e8eaed;
  --muted: #6b7280;
  --subtle: #374151;
  --white: #ffffff;
}
```

### 9B — Typography (mandatory font stack)
```html
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@300;400;500&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
```

- Display / Headlines: `font-family: 'Syne', sans-serif` — weights 700, 800
- Monospace / Labels / Tags: `font-family: 'DM Mono', monospace` — weights 400, 500
- Body text: `font-family: 'DM Sans', sans-serif` — weights 400, 500
- Base font-size: 14px | Base line-height: 1.6

### 9C — Layout Rules
- Max content width: 960px, centered, 32px side padding
- Section padding: 64px top, 48px bottom
- Section dividers: 1px solid var(--border)

### 9D — Component Specifications

**Report Header:**
- Background: var(--surface) | Border-bottom: 1px solid var(--border)
- Padding: 14px 32px — compact, not generous
- Single horizontal row layout: meta block on left (flex row: tag · title · subtitle inline),
  score box on right
- Report tag: DM Mono, 9px, letter-spacing 2px, green on green-dim background, padding 2px 8px
- Title: Syne 800, 16px, white — single line, no line break, white-space: nowrap
- Subtitle: DM Sans, 11px, var(--muted) — inline beside title in the meta flex row
- Score box: bg var(--bg), border var(--border), rounded 6px, padding 8px 16px
  - Flex row layout: score number on left, label + verdict + breakdown stacked on right
  - Overall score number: Syne 800, 24px, color var(--amber), line-height 1
  - Score label: DM Mono, 9px, letter-spacing 1px, var(--muted), uppercase
  - Score verdict badge + breakdown on same row, separated by gap 8px
  - Score verdict: DM Mono 9px, amber text on amber-dim bg, padding 2px 6px, border-radius 3px
  - Score breakdown: DM Mono 9px, var(--muted), border-left 1px solid var(--border),
    padding-left 12px

**Dashboard Grid:**
- 2-column CSS grid | 1px solid var(--border) between all cells
- Each card: background var(--surface), padding 20px
- Area name: Syne 700, 13px, white
- Score number: DM Mono, 22px — red/amber/green based on status
- Score bar: 4px height, border-radius 2px
- Status badge: DM Mono 10px, letter-spacing 1px

**Persona Cards:**
- Background: var(--surface) | Border: 1px solid var(--border) | Border-radius: 8px
- Header: 3-column grid — persona number · role/company · "page serves" rating
- Persona number: Syne 800, 36px, green, opacity 0.25
- Role: Syne 700, 15px, white
- Company type: DM Mono, 10px, amber, letter-spacing 1px, uppercase
- "Page serves" rating: Syne 800, 18px — var(--red) for Poorly, var(--amber) for Partially, var(--green) for Well
- Attributes grid: 2-column, var(--surface2) background cells, border: 1px solid var(--border), border-radius: 6px
- Attribute label: DM Mono 9px, letter-spacing 2px, uppercase, var(--muted)
- Attribute value: DM Sans 12.5px, var(--text), line-height 1.55
- Questions list: amber "?" marker, 12.5px body text, 8px gap between items
- Urgency box: var(--amber-dim) background, 1px solid rgba(245,166,35,0.25) border, border-radius 6px
- Page assessment: border-top 1px solid var(--border), 12.5px body text
- Audit area tags: red-dim/amber-dim background, DM Mono 9px, letter-spacing 1px
- Priority matrix: full-width table, DM Mono 9px headers, var(--bg) header background
  - CRITICAL: red-dim background, red text, red border (25% opacity)
  - HIGH: amber-dim background, amber text, amber border (25% opacity)
  - MEDIUM: green-dim background, green text, green border (25% opacity)

**Audit Cards:**
- Background: var(--surface) | Border: 1px solid var(--border) | Border-radius: 8px
- Summary box: green-dim background, green border (20% opacity), 13px text, #a3d99a color
- Two-column grid for Working + Issues: equal width, 20px gap
- Working items: → arrow, green color
- Issues: ! marker, red color
- Solutions: ↳ arrow, amber color
- Impact box: var(--surface2) background, 3-column grid
  - Impact range: Syne 700, 18px, green
  - Labels: DM Mono, 9px, uppercase, muted

**Hero Visual Element Panel:**
- Background: var(--surface2) | Border: 1px solid var(--border) | Border-radius: 6px
- Label: DM Mono, 10px, letter-spacing 2px, uppercase, color var(--amber)

**Copy Standard Tag:**
- Background: rgba(245,166,35,0.08) | Border: 1px solid rgba(245,166,35,0.2)
- Color: var(--amber) | Font: DM Mono, 9px, letter-spacing 1px
- Format: §2.5B · CONTRAST HEADLINE

**Action Tables:**
- Width: 100%, border-collapse: collapse
- Header row: DM Mono 10px uppercase, muted, var(--bg) background
- Priority labels: DM Mono 11px, letter-spacing 2px
  - P0: red-dim background, red border
  - P1: amber-dim background, amber border
  - P2: green-dim background, green border

**Wireframe Blocks:**
- Border: 1px dashed var(--border) | Border-radius: 6px
- Label bar: var(--surface2) background, DM Mono 10px uppercase, muted
- Wireframe headlines: Syne 800 (h1: 20px, h2: 16px, h3: 13px), white
- Headline type tag: inline amber copy-tag immediately after each headline
- CTA buttons: DM Mono 11px, letter-spacing 1px, padding 8px 16px
  - Primary: var(--green) background, white text
  - Secondary: transparent, green border, green text
- CTA microcopy: 10px, var(--muted), italic, beneath primary CTA

**Flow Comparison:**
- 2-column grid | Current: red labels | Recommended: green labels
- [NEW] tags: 9px DM Mono, green-dim bg, green text

**Bet Cards:**
- var(--surface) background | var(--border) border | 8px radius | 24px padding
- 2-column grid: large number left (Syne 800, 48px, green, 0.3 opacity), content right
- Row labels: DM Mono 10px uppercase, 80px wide, var(--muted)
- Mandatory rows: Change · Why · Impact · Copy Std · Primary Persona

**Sticky Left Navigation:**
- `position: fixed` | `top: 180px` | `left: max(16px, calc(50% - 608px))` | `width: 140px`
- `max-height: calc(100vh - 96px)` | `overflow-y: auto` | `scrollbar-width: none`
- Visible only at viewport ≥ 1300px: `@media (min-width: 1300px) { display: block; }`
- top: 80px clears the compact header (14px padding + ~52px content + 14px padding ≈ 80px)
- Background: transparent — no card/box treatment
- **Each section item is a single horizontal line** — number + label side by side, no stacking
  - Layout: `display: flex; align-items: center; gap: 7px`
  - Padding: 5px 8px 5px 12px | border-radius 4px | white-space: nowrap
  - Active indicator: 2px left border in var(--green), inset top/bottom 5px
  - Hover state: var(--surface2) background
  - Section number: DM Mono 9px, letter-spacing 1px, var(--muted); active: var(--green)
  - Section label: DM Sans 11px, weight 500, var(--text); active: var(--white)
  - **NO badges** — no score counts, no action counts, no "START HERE" labels
- Audit area sub-items (under Section 03 Analysis): single line, dot + label only
  - Layout: `display: flex; align-items: center; gap: 6px`
  - Padding: 3px 8px 3px 12px | border-radius 4px | white-space: nowrap
  - 6px dot indicator (border-radius 50%) — red/amber/green based on area score
  - Label: DM Mono 9px, var(--muted); active: var(--white) with surface2 background
  - Labels are area names only — no number prefix, no score suffix
    (e.g. "Hero", "Messaging", "Social Proof" — NOT "01 · Hero 5/10")
- Dividers between sections: 1px solid var(--border), 3px vertical margin
- IntersectionObserver JS: watches all section IDs (s01–s08) and audit area IDs (a01–a10)
  - Threshold: 0.08 for sections, 0.15 for areas | rootMargin: `-60px 0px -60px 0px`
  - On intersection: remove .active from all sibling items, add .active to matching nav item
  - Auto-scroll nav to keep active item visible using `scrollIntoView({ block: 'nearest' })`

**Section Labels:**
- DM Mono, 10px, letter-spacing 3px, uppercase, green
- Flex row with line extending to right edge

### 9E — Color Logic for Scores
```
Score 1–4  → var(--red),   var(--red-dim)
Score 5–7  → var(--amber),  var(--amber-dim)
Score 8–10 → var(--green),  var(--green-dim)
```

### 9F — Design Principles
- Dark-theme, editorial, technical report aesthetic
- Tone: industrial precision — data-dense but visually refined
- Typography is the primary design element
- No generic AI aesthetics — no purple gradients, no Inter font, no rounded bubbly cards
- Color is used functionally: green = positive, red = critical, amber = warning
- The report must feel like something a senior strategist produced

---

## 🏗️ SECTION 10 — HTML FILE STRUCTURE (MANDATORY)

The HTML file MUST follow this exact section order:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <!-- Charset, viewport, title -->
  <!-- Google Fonts: Syne + DM Mono + DM Sans -->
  <!-- Complete CSS: all variables, all component styles including persona cards -->
  <!-- Include Copy Standard Tag styles (.copy-tag class) -->
  <!-- Include Sticky Nav styles (#sticky-nav, .snav-section, .snav-area, etc.) -->
</head>
<body>
  <!-- 1. .report-header: client name, tag, overall score box -->
  <!-- 2. #sticky-nav: fixed left navigation (outside .wrap, before it) -->
  <!--    → Each section item clickable, scrolls to target section ID -->
  <!--    → Section 03 has expandable audit area sub-items (a01–a10) with score dots -->
  <!--    → Dividers between sections -->
  <!-- 3. .wrap container (max-width 960px) containing: -->
  <!--    <section id="s01"> CRO Performance Dashboard </section> -->
  <!--    <section id="s02"> Buyer Personas -->
  <!--      → Minimum 2 persona cards, maximum 4 -->
  <!--      → Persona × Audit Area Priority Matrix -->
  <!--    </section> -->
  <!--    <section id="s03"> Detailed Analysis -->
  <!--      → <div class="audit-card" id="a01"> Hero — MUST include Visual Recs panel </div> -->
  <!--      → <div class="audit-card" id="a02"> Messaging Clarity </div> -->
  <!--      → <div class="audit-card" id="a03"> Social Proof </div> -->
  <!--      → <div class="audit-card" id="a04"> CTA Strategy </div> -->
  <!--      → <div class="audit-card" id="a05"> Page Flow </div> -->
  <!--      → <div class="audit-card" id="a06"> Trust & Credibility </div> -->
  <!--      → <div class="audit-card" id="a07"> Visual Design / UX </div> -->
  <!--      → <div class="audit-card" id="a08"> Objection Handling </div> -->
  <!--      → <div class="audit-card" id="a09"> Audience Segmentation </div> -->
  <!--      → <div class="audit-card" id="a10"> Urgency / Compliance Hook </div> -->
  <!--    </section> -->
  <!--    <section id="s04"> High-Impact Action Plan (P0/P1/P2) </section> -->
  <!--    <section id="s05"> Visual Page Reconstruction -->
  <!--      → Wireframe 1 Hero MUST include persona routing row + H1 variants block -->
  <!--    </section> -->
  <!--    <section id="s06"> Page Flow Comparison </section> -->
  <!--    <section id="s07"> What's Working vs Broken </section> -->
  <!--    <section id="s08"> The 3 Biggest Bets </section> -->
  <!-- 4. Report footer note row -->
  <!-- 5. IntersectionObserver JS script (before </body>) -->
  <!--    → Observes s01–s08 for section-level active state -->
  <!--    → Observes a01–a10 for audit area sub-item active state -->
  <!--    → Auto-scrolls sticky nav to keep active item in view -->
</body>
</html>
```

File naming convention: `cro-audit-[clientname]-[date].html`

---

## 📏 QUALITY STANDARDS (ENFORCE THESE)

**Specificity rule:** Every insight, issue, and solution must be specific to the page being audited.
Generic observations are not acceptable.

**Verification rule:** All spatial, technical, and factual claims about the page must be verified
against the HTML source or screenshot before inclusion. Do not infer rendering behavior from
CSS class names alone — verify against what is actually visible. If uncertain, say so.

**Copy rewrite rule:** Every "Solutions" bullet that involves copy must include the actual rewritten
copy, produced in accordance with Section 2.5 — Strategic Copy Standards.

**Register consistency rule:** The copy register calibrated in Step 0D must be maintained
consistently across all report sections.

**Impact range rule:** Impact ranges must be realistic and calibrated to funnel position.
- Hero / CTA areas: +10–30% range is plausible
- Mid-page content areas: +5–18% range is plausible
- Design / UX areas: +3–10% range is plausible
- Do not assign +50% to any single change.
- When multiple changes address the same viewport or reading unit, combine them into
  one action item with one calibrated range rather than assigning separate overlapping ranges.

**Completeness rule:** All 10 areas must appear in the dashboard, detailed analysis,
and referenced at least once in the action plan.

**Score consistency rule:** Scores must be IDENTICAL between Dashboard and Detailed Analysis.

**Score uniqueness rule:** Do not assign the same score to more than 3 of the 10 areas.

**Score breakdown accuracy rule:** The "X Critical · Y Needs Work · Z Strong" summary in the
report header must be counted from the actual scores before writing. Verify the count.

**Cross-section consistency rule:** Page flow recommendations must be identical across
Detailed Analysis (Area 05), Action Plan, and Flow Comparison. Three different recommended
flows in the same report is an error.

**Fabricated data rule:** If wireframes include specific numbers not verifiable from the
inputs, add a visible caveat flagging them as illustrative estimates.

**HTML completeness rule:** The HTML file must be self-contained, open correctly in any
browser, and contain all 8 sections with real content.

**Persona grounding rule:** Every persona must be derived from the context block, the page's
existing content, or the HTML. Do not invent roles, company types, or anxieties.

**Persona specificity rule:** A persona is not "Marketing Manager who wants better data."
It is "VP Marketing at a B2B SaaS company ($10M–$50M ARR) whose primary anxiety is CAC
attribution accuracy across a fragmented multi-channel stack." Specificity is the difference
between a useful persona and a decorative one.

**Priority matrix rule:** Every cell in the Persona × Audit Area matrix must be justifiable
from the persona card. CRITICAL means this area directly addresses the persona's primary
anxiety or buying trigger. Do not assign CRITICAL uniformly across all cells.

**Persona threading rule:** Solutions in the Detailed Analysis MUST be tagged with persona
relevance where personas have meaningfully different priorities. Tag format: `(Primary: P1 · Secondary: P2)`.
Do not tag solutions that serve all personas equally. Do not invent persona relevance — only tag
where the fix demonstrably matters more to one persona's primary anxiety or buying trigger.

**Persona routing rule:** Every audit with 2+ personas MUST include a persona self-selection
routing element in the Hero wireframe AND a corresponding P1 action plan item. The routing
element is the implementation mechanism for all persona-specific copy recommendations.

**Bet persona rule:** Every Bet card MUST include a "Primary persona" row naming which persona/s
the bet primarily converts and why the others are secondary or served by a different bet.
Do not assign all bets to "ALL PERSONAS" — if all three bets serve all personas equally,
the bets are not persona-specific enough and need to be reconsidered.

---

## 🚫 ABSOLUTE PROHIBITIONS

- DO NOT output the audit as chat text or markdown — HTML file ONLY
- DO NOT skip reading the SKILL.md file before generating the report
- DO NOT skip any of the 10 audit areas
- DO NOT use generic copy like "the headline could be improved" — write the improvement
- DO NOT write copy rewrites without first reading and applying Section 2.5
- DO NOT use a copy register that hasn't been calibrated against the context block inputs
- DO NOT write hero headlines without specifying which headline type from §2.5B you are using
- DO NOT write CTAs without applying the 5-rule CTA Engineering framework (§2.5C)
- DO NOT write claim-bearing copy without applying Credibility Architecture (§2.5E)
- DO NOT use placeholder text in the HTML — all content must be real audit content
- DO NOT use Inter, Roboto, Arial, or system fonts — use Syne + DM Mono + DM Sans only
- DO NOT use purple gradients or generic SaaS color schemes
- DO NOT assign the same score to more than 3 areas
- DO NOT produce impact ranges above +35% for any single change
- DO NOT start generating the report before confirming Steps 0A, 0B, 0C, and 0D are complete
- DO NOT use different scores for the same area between Dashboard and Detailed Analysis
- DO NOT use different page flow recommendations across different sections of the same report
- DO NOT present fabricated statistics as verified data
- DO NOT recommend generic stock photography in the Hero Visual Element panel
- DO NOT drift copy register mid-report
- DO NOT invent buyer personas — ground every persona in the context block or page content
- DO NOT use fictional names for personas
- DO NOT state spatial or technical claims about the page without verifying against the HTML
  or screenshot — "positioned below the illustration" requires visual confirmation, not inference
- DO NOT write the score breakdown summary (X Critical · Y Needs Work · Z Strong) without
  counting from the actual scores first
- DO NOT tag all solutions with persona labels — only tag where personas have meaningfully
  different priorities for that specific fix; over-tagging makes the threading meaningless
- DO NOT assign "ALL PERSONAS" to all three Bet cards — each bet should have a primary persona
- DO NOT skip the persona routing row in the Hero wireframe when 2+ personas are defined
- DO NOT skip the H1 variant block in the Hero wireframe when 2+ personas are defined
- DO NOT skip the mandatory P1 persona routing action item in the Action Plan

---

## ✅ PRE-FLIGHT CHECKLIST (run through this before generating)

Before writing a single line of the report, confirm:

[ ] SKILL.md has been read via the view tool
[ ] Screenshot is present and visible
[ ] Context block is filled in (all required fields including Industry/niche and Buyer personas)
[ ] HTML is available (or noted as absent)
[ ] Buyer personas identified — minimum 2, maximum 4
[ ] Each persona grounded in context block or page content (not invented)
[ ] Each persona meaningfully distinct from the others
[ ] Copy register has been calibrated using context block inputs (Step 0D)
[ ] Register type identified: _____________________ (e.g. ESG Consulting, B2B SaaS)
[ ] Funnel stage identified: _____________________ (TOFU / MOFU / BOFU / Mixed)
[ ] Traffic temperature identified: ______________ (Cold / Warm / Branded)
[ ] All 10 audit areas are planned
[ ] Output will be an HTML file, not chat text
[ ] File will be created at /home/claude/cro-audit-[client]-[date].html
[ ] File will be delivered via present_files tool
[ ] Hero card will include Visual Element Recommendations panel
[ ] All scores are consistent between Dashboard and Detailed Analysis
[ ] Score breakdown (X Critical · Y Needs Work · Z Strong) counted from actual scores
[ ] Impact ranges are consistent across all sections
[ ] Page flow recommendation is identical across Area 05, Action Plan, and Flow Comparison
[ ] All wireframe headlines will carry Copy Standard Tags
[ ] All primary CTA wireframe buttons will carry microcopy beneath them
[ ] Persona × Audit Area Priority Matrix populated and justified
[ ] Persona threading planned for solutions — know which fixes tag P1, P2, P3 before writing
[ ] Hero wireframe will include persona self-selection routing row
[ ] Hero wireframe will include persona-specific H1 variant block (one per persona)
[ ] Action plan includes mandatory P1 persona routing action item
[ ] All three Bet cards will include a Primary Persona row

Only begin after all checkboxes are confirmed.

---

## 🎯 FINAL GOAL

Every audit run using this prompt must produce:
- A report that is indistinguishable in quality from a senior agency deliverable
- A buyer persona section grounded in real ICP data, not marketing archetypes
- A Persona × Audit Area priority matrix that gives the client a persona-filtered
  implementation sequence — not just a flat action list
- Visual consistency with the design system defined above — every time
- Specific, actionable, copy-level recommendations — not strategic platitudes
- Copy rewrites that apply named copywriting principles — not instinct-based rewrites
- A consistent voice and register calibrated to the client's actual buyer, niche, and funnel stage
- A downloadable HTML file the client can open, share, and reference
- A document that pre-sells the implementation work without pitching it
- Hero visual recommendations that go beyond "use a better image"
- All factual and spatial claims verified against the HTML source, not inferred

The report is the product. Make it earn that.

---

## 📋 CHANGELOG

**v2.4 — April 2, 2026**
- ADDED: Persona threading instruction in Section 3 Solutions — solutions tagged with
  `(Primary: P1 · Secondary: P2)` format where personas have meaningfully different priorities
- ADDED: Persona routing element as MANDATORY requirement in Section 5 Hero wireframe
- ADDED: Persona H1 variants as MANDATORY requirement in Section 5 Hero wireframe
- ADDED: Mandatory P1 persona routing action item to Section 4 Action Plan requirements
- ADDED: "Primary persona" row as MANDATORY field in Section 8 Bet card format
- ADDED: Persona threading rule, persona routing rule, bet persona rule to Quality Standards
- ADDED: 5 new items to Pre-Flight Checklist, 5 new items to Absolute Prohibitions
- ADDED: Sticky left navigation design spec to Section 9D
- UPDATED: Report Header spec — compact single-row layout replacing tall two-column design:
  - Padding reduced from 40px to 14px
  - Title reduced from Syne 800 32px two-line to Syne 800 16px single line
  - Score number reduced from 52px stacked to 24px inline
  - Score box changed from vertical card to horizontal flex row
  - All header elements now fit in one compact bar ~52px tall
- UPDATED: Sticky Nav spec — compact single-line items, no badges:
  - top offset corrected to 80px (clears compact header)
  - width reduced from 148px to 140px
  - Each section item is a single flex row (number + label) — no stacking
  - Badges removed entirely (no score counts, action counts, or "START HERE" labels)
  - Audit sub-item labels are area names only — no number prefix or score suffix
  - Divider margin reduced from 6px to 3px
- UPDATED: Section 10 HTML structure with all section/area IDs and IntersectionObserver JS

**v2.3 — April 2, 2026**
- ADDED: Section 2 — Buyer Personas (positioned between Dashboard and Detailed Analysis)
- ADDED: Step 0C — Identify Buyer Personas (mandatory pre-execution step)
- ADDED: Buyer personas / ICP segments field to INPUT FORMAT context block
- ADDED: Persona Card component spec to Section 9D design system
- ADDED: Persona × Audit Area Priority Matrix
- ADDED: Persona grounding rule, persona specificity rule, priority matrix rule
- ADDED: Score breakdown accuracy rule and verification rule to Quality Standards
- UPDATED: Section numbering — all sections after Dashboard shift +1
- UPDATED: Step numbering — 0C/0D/0E to accommodate new persona step

**v2.2 — April 2, 2026**
- ADDED: Section 2.5 — Strategic Copy Standards (§2.5A–F full copywriting layer)
- ADDED: Step 0C — Calibrate Copy Register
- ADDED: Hero Visual Element Recommendations mandatory sub-section
- ADDED: Copy Standard Tag component to design spec

**v2.1 — April 1, 2026**
- ADDED: Section 2A — Hero Visual Element Recommendations
- ADDED: Score consistency, uniqueness, cross-section consistency, fabricated data rules
- UPDATED: Section 9 HTML structure

**v2.0 — Original**
- Initial prompt with 10 audit areas, 7 report sections, full design system