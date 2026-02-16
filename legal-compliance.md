# Legal & Compliance Deep Dive

Running a Shopify store comes with significant legal responsibilities. Non-compliance can result in hefty fines, payment processor termination, and damage to reputation. This chapter covers the essential compliance areas every store owner must address.

## 1. Privacy Regulations

### GDPR (General Data Protection Regulation) – EU
**Applies to**: Any business serving EU customers, regardless of location.

**Key Requirements**:
- **Lawful basis for processing**: Typically "consent" for marketing, "legitimate interest" for order fulfillment
- **Privacy policy**: Must be clear, concise, written in plain language; disclose what data you collect, why, how long you keep it, and who you share it with (e.g., Shopify, payment gateways, apps)
- **Cookie consent**: Must obtain opt-in consent before setting non-essential cookies (marketing, analytics). Use a compliant banner (e.g., Cookiebot, CookieYes, or custom with explicit accept/decline)
- **Data subject rights**: Provide mechanisms for users to:
  - Request access to their data (data export)
  - Request correction or deletion (right to be forgotten)
  - Object to processing
  - Data portability
- **Data processing agreements (DPAs)**: Ensure all third-party services (Shopify, apps, email platforms) have GDPR-compliant DPAs in place (most do automatically)
- **Breach notification**: Notify authorities within 72 hours of a data breach affecting EU residents

**Penalties**: Up to €20 million or 4% of global annual revenue (whichever is higher)

### CCPA (California Consumer Privacy Act) – California, USA
**Applies to**: For-profit businesses operating in California with >$25M revenue or handling data of >50,000 consumers.

**Key Requirements**:
- **Notice at collection**: Inform consumers what categories of personal information are collected and the purposes
- **Right to opt-out**: Allow users to opt-out of the sale/sharing of personal data (includes targeted advertising)
- **Right to delete**: Must delete personal information upon verified request (with some exceptions)
- **Right to know**: Provide a copy of personal data upon request
- **Do Not Sell/Share** link on homepage (even if you don't sell data, you must have the link that either honors opt-out or explains why not)
- **Privacy policy** must include a description of CCPA rights and how to exercise them

**Penalties**: Up to $7,500 per intentional violation; $2,500 per unintentional violation (enforced by California Attorney General)

### Other US State Laws
- **Virginia CDPA**, **Colorado CPA**, **Utah UCPA**, **Connecticut CTDPA** – Similar to CCPA; many states adopting. If you sell nationwide, treat CCPA as the baseline and extend similar rights to all states.

## 2. Terms of Service & Refund Policy

### Terms of Service (ToS)
- Defines rules for using your store
- Limits your liability
- Governs dispute resolution (governing law, arbitration)
- Should include:
  - Intellectual property rights (your content, trademarks)
  - User account terms (if applicable)
  - Prohibited uses
  - Disclaimer of warranties
  - Limitation of liability
  - Indemnification clause
  - Changes to terms

**Tip**: Use a lawyer or a reputable template (e.g., Termly, Legal Templates) and customize for your business.

### Refund & Returns Policy
- Mandatory in many jurisdictions (EU consumer law: 14-day right of withdrawal)
- Should clearly state:
  - Timeframe for returns/exchanges (e.g., 14 days, 30 days)
  - Condition requirements (unused, tags attached)
  - Who pays return shipping (you vs customer)
  - Refund method (original payment, store credit)
  - Exceptions (final sale, custom items, underwear)
- Display prominently (footer, checkout, product page for expensive items)

## 3. Accessibility (ADA & WCAG)

### Why It Matters
- The Americans with Disabilities Act (ADA) requires websites to be accessible to people with disabilities
- Thousands of e-commerce accessibility lawsuits have been filed
- Even if not explicitly legislated for websites, courts apply ADA Title III to online stores

### WCAG 2.1 AA Level (Recommended Standard)
Follow the Web Content Accessibility Guidelines:
- **Perceivable**:
  - Text alternatives for non-text content (alt text for images, aria-labels for buttons)
  - Captions for videos
  - Sufficient color contrast (4.5:1 for normal text)
- **Operable**:
  - Keyboard accessible (all interactive elements reachable via Tab)
  - No time limits (or ability to extend)
  - No flashing content (>3 flashes per second)
- **Understandable**:
  - Readable text (clear language)
  - Predictable navigation and consistency
- **Robust**:
  - Proper HTML semantics (headings, landmarks)
  - ARIA attributes where needed but not overused

### Practical Steps for Shopify
- Choose an accessible theme (Dawn is WCAG AA compliant out of the box)
- Audit with tools: axe DevTools, WAVE, Lighthouse accessibility
- Fix common issues: missing alt text, improper heading structure, low contrast
- Test with keyboard-only navigation
- Add an accessibility statement page

## 4. Payment Security & PCI Compliance

### PCI DSS (Payment Card Industry Data Security Standard)
**Good news**: Shopify is PCI DSS Level 1 certified, meaning they handle most of the burden. You don’t store credit card data on your servers.

**Your responsibilities**:
- Use Shopify Payments or a PCI-compliant gateway
- Do not attempt to collect, store, or process raw credit card data yourself
- Keep your Shopify admin secure (strong password, 2FA)
- Ensure any custom code or apps do not intercept payment data

**What to avoid**:
- Adding custom forms that collect credit card numbers
- Using non-HTTPS pages for checkout (Shopify enforces HTTPS automatically)
- Storing order confirmations with full card numbers in plain text

## 5. Email & SMS Marketing Compliance

### CAN-SPAM Act (US)
- No false or misleading header/subject lines
- Clear identification as advertisement
- Provide physical mailing address
- Include a clear unsubscribe mechanism (one-click opt-out)
- Honor opt-outs within 10 business days

### TCPA (Telephone Consumer Protection Act) – SMS
- Prior express written consent required for autodialed SMS
- Clear opt-in language (no pre-checked boxes)
- Include STOP/HELP instructions in each message
- Honor STOP requests immediately

### GDPR for Email
- Explicit opt-in required (pre-checked boxes are not consent)
- Double opt-in recommended
- Include unsubscribe link in every email
- Keep records of consent (timestamp, IP, version of privacy policy)

### Shopify / Klaviyo Best Practices
- Use Klaviyo's built-in consent management
- Segment by consent status (marketing vs transactional)
- Never buy or rent email lists
- Clean your list regularly (remove hard bounces, inactive subscribers)

## 6. Copyright & Trademark

### Images & Content
- Only use images you own or have a license for
- Stock photos: ensure license allows commercial use (e.g., Unsplash, Pexels are free; Shutterstock, Adobe Stock require purchase)
- User-generated content: get explicit permission to repost; credit creators when possible
- Videos: same rules; be cautious with music ( royalty-free or properly licensed)

### Brand Assets
- Your store name and logo should be trademarked if you're building a brand
- Don't use other brands' trademarks in your product titles or descriptions (e.g., "compatible with iPhone" is okay; "iPhone" is Apple's trademark but descriptive use is generally fine; avoid implying affiliation)
- Respect design patents (don't copy competitor's product design if patented)

## 7. Age-Restricted Products

If selling:
- Alcohol, tobacco, vaping, cannabis (where legal)
- Firearms, ammunition
- Adult content

You must:
- Implement age verification at checkout (e.g., AgeChecker, AgeVerifier)
- Collect date of birth and verify with third-party service
- Ship only to jurisdictions where legal
- Include required warnings and disclaimers
- Keep records of age verification

## 8. Environmental Claims (Greenwashing)

If making environmental claims ("eco-friendly", "sustainable", "recycled"):
- Ensure claims are truthful and not misleading
- Have evidence to back them up (certifications, material sourcing info)
- Follow FTC Green Guides (US) or EU Unfair Commercial Practices Directive
- Avoid vague terms; be specific (e.g., "100% recycled polyester" vs "green")

## 9. Compliance Checklist by Launch

- [ ] Privacy policy published and linked in footer/checkout
- [ ] Cookie consent banner implemented (GDPR/CCPA compliant)
- [ ] Terms of service and refund policy in place
- [ ] Accessibility audit completed and major issues fixed
- [ ] SSL/HTTPS active (Shopify provides automatically)
- [ ] PCI compliance verified (use Shopify Payments)
- [ ] Email/SMS consent collected properly (double opt-in if EU)
- [ ] Age verification for restricted products (if applicable)
- [ ] Copyright clearances for all media
- [ ] Data processing agreements with third parties reviewed (Shopify, apps)
- [ ] Cookie policy distinct or included in privacy policy
- [ ] Right to opt-out link present (CCPA) in footer if required
- [ ] Accessibility statement page published (optional but good practice)

## 10. Ongoing Maintenance

Compliance is not a one-time task. Revisit quarterly:
- Review changes in privacy laws (new state laws in US, updates to GDPR guidance)
- Update policies when adding new data collection (new app, feature)
- Audit third-party apps for compliance (check their privacy policies)
- Refresh accessibility testing after theme updates
- Ensure consent records are retained (Shopify/Klaviyo handle this)
- Conduct a privacy impact assessment (PIA) for new marketing initiatives

---

**Navigation**

- [Table of Contents](TOC.md)
- Previous: [Customer Service & Support Systems](customer-support.md)

*End of Legal & Compliance Deep Dive chapter*
