# Mohamed Gomaa Portfolio — Result-Focused Implementation Plan

**Goal:** Build a premium, futuristic, mobile-first portfolio that proves Mohamed Gomaa's engineering value through case studies, contribution clarity, measurable targets, SEO, accessibility, and fast performance.

**Core shift from the first plan:** The 3D/network animation is now optional polish, not the product. The site should win even with JavaScript disabled: strong copy, strong case studies, fast loading, clear proof.

---

## 1. Strategic Positioning

### Primary positioning

> Mohamed Gomaa builds secure, scalable systems behind serious products: APIs, healthcare integrations, AI-powered workflows, admin platforms, and business-critical web applications.

### Audience

- Hiring managers
- Technical leads
- Founders needing a full-stack/backend-heavy engineer
- Clients evaluating delivery credibility

### What the site must prove

1. Mohamed can work on production systems, not just demos.
2. Mohamed understands business workflows and domain problems.
3. Mohamed can explain his contribution clearly.
4. Mohamed has backend, architecture, API, integration, and full-stack strength.
5. Mohamed cares about quality: performance, accessibility, SEO, and maintainability.

---

## 2. Site Structure — Same Sections as Ahmed, Stronger Execution

Ahmed's portfolio sections:

1. Hero
2. Overview
3. Experience
4. Skills
5. Projects
6. Contact

Mohamed's implementation keeps that structure, but upgrades the project section into **case-study cards**.

---

## 3. Design System

### Visual style

- Premium dark interface
- Futuristic but restrained
- Technical dashboard accents
- Clear case-study layout
- Classy motion, no circus

### Palette

- Background: deep black/navy
- Surfaces: dark graphite
- Borders: subtle blue/white transparency
- Accent: cyan + emerald, small violet highlights
- Text: high-contrast white and soft slate

### Typography

- System font stack for performance
- Big confident hero headline
- Compact case-study cards with strong labels
- Monospace only for technical tags and system labels

---

## 4. Lightweight Optional 3D / Motion

### Rule

The 3D element must be **optional, lightweight, and non-blocking**.

### Implementation choice

Use a small `<canvas>` service-mesh animation drawn with vanilla JavaScript:

- No Three.js
- No React Three Fiber
- No heavy model files
- Disabled automatically when `prefers-reduced-motion: reduce`
- Hidden or simplified on small/mobile screens if needed

### Motion budget

- Scroll reveal with CSS only where possible
- Hover/focus transitions under 200ms
- No animation required to understand the content
- No layout shift

---

## 5. Case Study System

Each project card must answer:

| Field | Purpose |
|---|---|
| Problem | What business/user problem existed? |
| Contribution | What Mohamed personally/team contributed? |
| Engineering | What technical work mattered? |
| Result | What improved? |
| Stack | What tools/technologies were used? |
| Status | Public, private, internal, NDA, team project |

### Contribution wording rules

Do not overclaim solo ownership. Use honest language:

- “Contributed to…”
- “Built backend/API services for…”
- “Collaborated with frontend/backend teams…”
- “Part of the Digi Crafterz delivery team…”
- “Implemented…” only where CV supports direct implementation

### Shared/team projects from Medo

These must be marked as collaborative/team contributions:

- APA Admin
- APA Patient
- APA Doctor
- Shippingify Admin

---

## 6. Featured Project Order

### 1. AIMY — AI-Powered Services Platform

**Why first:** strongest modern positioning: AI, MCP, microservices, messaging, automation.

Focus:

- Clean architecture
- Microservices
- MCP integrations
- Third-party sync
- Messaging/event-driven workflows
- AI helpers and knowledge retrieval

### 2. MyAPA / APA Suite — Healthcare Systems

Cluster:

- APA Admin
- APA Doctor
- APA Patient
- MyAPA Health

Focus:

- AdvancedMD integration
- Secure patient data synchronization
- Clinic/patient/doctor workflows
- HIPAA-aware data handling
- Team contribution clarity

### 3. Shippingify Admin — Logistics Operations

Focus:

- Shipping management admin workflows
- API integration
- Operational dashboards
- Team contribution clarity

### 4. Real Estate Evaluation Management System

Focus:

- Dynamic forms
- Role-based approvals
- Workflow transparency
- Accurate valuation process

### Secondary projects

- IWingo — Educational platform
- SM Printing & Translation App
- GCC Customs Union Authority
- Digitization project for holy-site contracting work
- Advanced Psychiatry Associates Website
- Mad-era Website & Management System

---

## 7. Performance Targets

### Hard targets for v1

| Metric | Target |
|---|---|
| HTML/CSS/JS weight | Keep small; no heavy frameworks for v1 |
| JS dependencies | Zero for static version |
| First meaningful content | Immediate static render |
| Mobile layout | Primary design target, not afterthought |
| Images | Avoid heavy images unless supplied |
| Animation | Canvas only, optional, reduced-motion safe |

### Verification

- Check file sizes
- Open locally
- Test mobile viewport screenshot
- Confirm no console errors
- Confirm site works without remote dependencies

---

## 8. SEO Plan

Add:

- Semantic `<title>`
- Meta description
- Open Graph title/description/type
- Twitter card metadata
- Canonical placeholder to update after deployment
- Structured JSON-LD Person data
- One clear `<h1>`
- Logical heading hierarchy
- Descriptive section IDs

SEO copy target:

> Mohamed Gomaa is a Full-Stack Software Engineer in Egypt building scalable .NET, React, Next.js, AI-powered, and enterprise web systems.

---

## 9. Accessibility Plan

Requirements:

- Semantic landmarks: header, main, section, footer
- Skip link
- Keyboard-visible focus states
- Buttons/links at least 44px on mobile
- Sufficient contrast
- Reduced motion support
- Canvas marked decorative with `aria-hidden="true"`
- Contact links have descriptive labels
- No text hidden only in images
- Form uses real labels if a form is included

For v1, use direct email/LinkedIn/GitHub links instead of a fake form backend.

---

## 10. Implementation Approach

### v1 artifact

Build as a static portfolio first:

```text
/opt/data/mohamed-gomaa-portfolio/
  index.html
  README.md
  PLAN.md
  public/
    Mohamed_Gomaa_FlowCV_Resume_2026-06-23.pdf
```

Why static first:

- Fast
- SEO-friendly
- Vercel deploys it easily
- GitHub Pages deploys it easily
- No dependency goblins hiding in `node_modules`

If Medo later wants a React/Next.js version, convert after content/design is approved.

### Build steps

1. Write accessible semantic HTML.
2. Add premium mobile-first CSS.
3. Add project data manually as structured case-study cards.
4. Add small optional canvas animation.
5. Add SEO/OG/JSON-LD metadata.
6. Verify desktop/mobile screenshots.
7. Prepare for GitHub/Vercel deployment.

---

## 11. Deployment Plan

### What can be done now

- Build locally.
- Run it on a local port for preview.
- Provide screenshot and local artifact path.

### What is needed for public deployment

To push to Mohamed's GitHub and deploy to Vercel, Medo must provide:

1. GitHub username
2. Repo name or permission to create a new repo
3. GitHub token with repo permission
4. Vercel token or browser/login access to Vercel
5. Vercel project/team choice if multiple teams exist

### Recommended deployment

- Push static site to GitHub repo.
- Import repo into Vercel.
- Set output as static root.
- Verify public URL.
- Update canonical/OG URL to final Vercel link.

---

## 12. Definition of Done

The build is complete only when:

- Site opens locally.
- Desktop screenshot looks correct.
- Mobile screenshot looks correct.
- Basic SEO tags exist.
- Basic accessibility checks pass.
- No browser console errors.
- CV download link works locally.
- User receives deployment requirements or public Vercel link if credentials are provided.
