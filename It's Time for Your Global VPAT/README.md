# It's Time for Your Global VPAT
Presented by Deque

## Presenters
- Will Creedle, Senior Accessibility Consultant, CPWA
- John Piotrowski, Enterprise Customer Success Manager, CPACC

## Agenda
- Review the basics
- Understand your obligations
- Develop a strategy

## Why Now?
- The EAA and Title II are in the news and driving companies to ask, "How accessible are our products?"
- The most common question is, "Do you have a VPAT?"

## What is an ACR?
- Do I need both a VPAT and an ACR?
  - **VPAT:** *Voluntary Product Accessibility Template*. The keyword is "Template"
    - The unfinished document is a VPAT
    - The finished work is your ACR
  - **ACR:** *Accessibility Conformance Report*
    - It's for companies and people to quickly understand your accessibility status

## What *isn't* an ACR?
- It's not...
  - a roadmap to all your faults
  - an intensely detailed accounting of issues
  - a place to muddle the truth
- It's...
  - a standardized form used to document how a product meets accessibility standards
- A VPAT should be clear, concise, and written for customers who know about accesibility but not necessarily understand terms like NVDA, screen reader, dialing wand, etc.
  - The person reading this is a requisitions officer going through an RFP for your product; it's not necessarily for a screen reader user

##  Concepts vs. Standards vs. Regulation
- Concepts:
  - ex. Design for All, POUR, etc.
- Standards:
  - ex. EN 301 549, WCAG, WAD, RGAA, etc.
- Regulation:
  - ex. EAA, ADA, AODA, etc.
- Concepts are the basis for Standards, which are used to prove conformance for Policy/Regulation
- We test for conformance *then* report accordingly
  - Test conformance to Standards
    - Standards
      - ex. EN 301 549, WCAG, WAD, RGAA, etc.
  - Then determine who you are reporting to
    - Audience
      - ex. Regulator, potential B2B customer, etc.
  - Which determines the format
    - Format
      - ex. VPAT 2.5Rev WCAG, VPAT 2.5Rev 508, VPAT 2.5Rev EU, VPAT 2.5Rev INT

##  There are 4 types of VPATs
- VPAT 2.5Rev WCAG
- VPAT 2.5Rev 508
- VPAT 2.5Rev EU
- VPAT 2.5Rev INT

|              | VPAT 2.5Rev WCAG | VPAT 2.5Rev 508 | VPAT 2.5Rev EU | VPAT 2.5Rev INT |
|--------------|------------------|-----------------|----------------|-----------------|
| WCAG 2.0-2.2 | ✅               | ✅               | ✅             | ✅              |
| Section 508  |                  | ✅              |                | ✅              |
| EN 301 549.  |                  |                 | ✅             | ✅              |

## EN 301 5949 & The EAA
- What is the EAA?
  - The **EAA** (*European Accessibility Act*) is a landmark directive requiring many private sector products and services (ex. banking, e-commerce, transport) to be accessible by June 2025
- What is EN 301 549?
  - It is the "Harmonised Standard" for the EAA. It contains all of WCAG 2.1/2.2 and several extra clauses
- There is a ton of overlap
  - WCAG 2.1 A and AA at the center
  - EN 301 549 encompasses WCAG 2.1/2.2
  - EAA
    - applies to private sector + public sector direct to consumer
    - adds electronic programme guides and product packaging
  - WAD
    - applies to public sector
    - adds accessibility statement and feedback mechanism
    - excludes live video
  - EN 301 549 is the recommended baseline technical requirement for both regulations
  - WCAG 2.1 A and AA is the core web accessibility standard
  - Each regulation adds its own specific requirements beyond EN 301 549
    - This does not include each EU-member state's unique EAA Transposition requirements which may add additional criteria

## Do I need a VPAT / ACR?
- There are many reasons for a VPAT
  - Compliance with government procurement requirements
  - Winning B2B contracts; many companies require a VPAT to even submit an RFP
  - Brand reputation and differentiation
  - Creating your roadmap to improving accessibility and showing historical commitment to improvement
  - Impriving UX and SEO - Accessibility *is* usability at this point
- There are specific reasons for an INT VPAT
  - One and done! You don't have to come back when an RFP requires INT as opposed to EU, WCAG, or Section 508
  - Same document applies to your RFP in Washington D.C. and Brussels
  - Future-proofing
  - International corporations like 'enterprise-ready' companies, and the INT VPAT shows that
  - Only one version to control going forward. Updating and maintaining many VPAT types is difficult and needlessly expensive
- VPAT/ACR representative examples
  - **WCAG section:** Clear, concise, honest, but not a roadmap to lawsuits
  - **EN 301 549 section:** Direct, honest. "N/A" does a lot of the work in EN 301 549

### Do I need an international ACR?
- This affects a lot of businesses!
  - Websites that sell goods or services to EU customers
  - Online and mobile banking
  - Streaming services
  - Transport services
  - E-books, vendors
  - Applications
- Don't just think websites!
  - Software, SAAS products
  - Hardware like rack servers, handheld devices, remote controls, robots
  - Kiosks, terminals
  - Smart TVs
- Who is exempt?
  - Microenterprises (fewer than 10 employees)
  - Annual balance sheet total under 2 million euros

## Who is going to look at this thing?
- Business side
  - Procurement buyers at government agencies, higher ed, multinational corporations
  - B2B procurement - many large companies will require third parties that they wish to integrate with to have an ACR showing their accessibility conformance. The bigger the company, the more likely it needs to be an INT
- Legal and personal side
  - More and more VPATs/ACRs are used by legal teams to show due diligence, effort, and the roadmap to conformance
  - Many companies like Microsoft and Google make their VPATs readily available to the public, allowing persons with disabilities to make informed decisions when buying their products like Excel and cloud services

## Understanding your obligations

### Audits
- What do I test?
  - You can test the entirety of your product, like a mobile application or website
  - You can test only the part that integrates with potential clients
  - Commonly, companies test specific important user journeys like registration, login, product page, search, and checkout flow
  - Just don't limit the scope to 'hide' potential problems
  - There is no need to test anything that isn't facing the client or user
    - Just test the rendered page, not the load-bearing capabilities of your server
- If you've already had an audit
  - Make sure it covers what it needs to for the RFPs you may submit
  - Make sure it's less than a year old or the product hasn't changed substantially
  - Make sure it was done to WCAG, EN 301 549 and Section 508 standards
- If you need an audit
  - You can do it in house
  - You can hire professionals

### What to expect from an audit
- **Phase one:** Audit
  - Define scope
  - Complete audit
- **Phase two:** Remediation
  - Audit report and ACR
  - Remediation
- **Phase three:** Conformance
  - Validation
  - Updated ACR

## Deque digital accessibility services

### Deque digital accessibility audits
- Most teams lack the tools, expertise, or resources to evaluate their digital accessibility, but Deque can help
- **Fast results:** Expert insights and detailed reports in 1-2 weeks, without sacrificing quality
- **Trusted findings:** W3C contributors and IAAP-certified expertis who have conducted 8,000+ audits using a proven methodology refined over 20+ years
- **Actionable guidance:** Prioritized recommendations so you can fix issues fast, with optional rescan and fix verification via Axe Dev Tools Extension

### Full suite of services
- Deque provides reliable audit results and guidance for faster remediation and reduced compliance risk
- **Evaluate any asset:** audit web, mobile apps, design systems, documents, kiosks, and beyond
- **Remediate and prove compliance:** Get tailored guidance or have Deque remediate directly; receive an ACR when ready
- **Demonstrate commitment:** Earn the Accessibility Commitmennt Badge with continuous scanning and detailed reporting