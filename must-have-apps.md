# Must‑Have Shopify Apps

Choosing the right apps is critical: too few and you miss functionality; too many and you bloat your site, hurt performance, and increase costs. This chapter curates the essential apps across categories, with selection criteria and implementation tips.

## 1. How to Choose Apps

Before installing any app, apply this checklist:

- **Necessity**: Does it directly increase revenue or reduce costs? Avoid "nice‑to‑have" features.
- **Performance impact**: Check app weight (JS size) and if it can be lazy‑loaded or disabled on certain pages.
- **Pricing model**: Avoid per‑order fees if you have high volume; prefer flat‑rate or tiered plans.
- **Support & updates**: Look for recent updates, good reviews, and responsive support.
- **Alternatives**: Could this be done via Shopify's native features, a custom snippet, or a lighter app?
- **App embedding**: Can you disable the app on specific pages via theme settings? Use this to limit impact.

## 2. Core Categories & Top Picks

### 2.1 Product Reviews & Trust

**Why**: Social proof drives conversion and SEO.

**Top picks**:
- **Loox** – Photo reviews with automated email prompts; easy installation, great for visual products.
- **Judge.me** – Free plan available, rich snippets, Q&A, and photo/video reviews. Very cost‑effective.
- **Yotpo** – Enterprise‑grade; includes loyalty, SMS, and visual marketing. Overkill for small stores but powerful for scaling brands.

**Implementation tip**: Automate review requests 7–14 days after delivery. Offer a small incentive (e.g., 10% off next purchase) but allow organic reviews too.

### 2.2 Email & SMS Marketing

**Why**: Email/SMS are highest‑ROI channels; automation recovers lost revenue.

**Top picks**:
- **Klaviyo** – Industry standard; deep Shopify integration, powerful segmentation, premade flows (welcome, abandoned cart, browse abandonment, winback, post‑purchase). Steep learning curve but worth it.
- **Omnisend** – All‑in‑one email + SMS + push; more user‑friendly; good for smaller catalogs.
- **Shopify Email** – Basic email campaigns; cheap but limited segmentation. Use only if you need minimal email.

**Implementation tip**: Set up these core flows within 30 days:
- Welcome series (3‑email sequence)
- Abandoned cart (1‑hour and 24‑hour reminders)
- Browse abandonment (if not oversaturating)
- Post‑purchase cross‑sell/thank you
- Winback (45/60/90 days)

### 2.3 Customer Support

**Why**: Support quality impacts retention and lifetime value.

**Top picks**:
- **Gorgias** – Unified inbox for email, chat, messenger, Instagram, WhatsApp; order context; automation rules; great for scaling support teams.
- **Zendesk** – Legacy powerhouse; robust but pricier; integrates with many tools.
- **Tidio** – Live chat + chatbots + email; good for SMBs; free plan available.

**Implementation tip**: Use saved replies and automation to handle common issues (tracking, returns, sizing). Integrate with Shopify to pull order data directly into support tickets.

### 2.4 Shipping & Fulfillment

**Why**: Accurate rates and smooth label printing reduce friction and support costs.

**Top picks**:
- **ShipStation** – Mature shipping platform; rate shopping, batch labels, tracking sync; works with many carriers.
- **Shippo** – Developer‑friendly; API first; good for multi‑carrier strategies.
- **Parcelify** – Custom shipping rules (e.g., free shipping over $50, dimensional weights) without code.

**Implementation tip**: If using a 3PL, ask which carrier integrations they support; many have dedicated apps (e.g., ShipHero, ShipBob). Set up live carrier rates on checkout to pass real‑time shipping costs to customers.

### 2.5 Accounting & Finance

**Why**: Automated bookkeeping saves hours and reduces errors.

**Top picks**:
- **QuickBooks Online** – Most popular; robust reporting; integrates with Shopify sync.
- **Xero** – Slightly more intuitive; strong in international markets.
- **A2X** – If using QuickBooks, A2X handles tax and settlement mapping from Shopify Payments.

**Implementation tip**: Reconcile daily or weekly. Map Shopify transaction types (order, refund, fee) to proper accounts automatically.

### 2.6 SEO & Content

**Why**: Organic search is a scalable, low‑cost acquisition channel.

**Top picks**:
- **Smart SEO** – Automated meta tags, alt text, structured data, sitemap, SEO health checks. Lightweight.
- **SEO Manager** – More advanced; includes keyword suggestions, 404 monitoring, canonical URL control.
- **Blog** – Use Shopify's native blog; don't install a separate CMS unless you need advanced features.

**Implementation tip**: Optimize product pages: unique titles/descriptions, long‑tail keywords, image alt text. Submit sitemap to Google Search Console. Use Google Analytics to track organic rankings and clicks.

### 2.7 Performance & Optimization

**Why**: Speed impacts conversion, SEO, and user experience.

**Top picks**:
- **Crush.pics** – Automatic image compression on upload; supports WebP; minimal impact.
- **Boost Filter & Search** – Instant, Algolia‑style search and smart collection filtering (only if you have >50 products).
- **PageSpeed Optimizer** (by Rocket Å fast) – Lazy load, defer JS, minify CSS/JS. Use sparingly; test after install.

**Implementation tip**: Always test performance improvements with PageSpeed Insights before and after. If performance worsened, remove the app.

### 2.8 Compliance & Legal

**Why**: Avoid costly legal issues; build trust.

**Top picks**:
- **TermsFeed** – Generate privacy policy, terms of service, cookie policy, return policy; auto‑update when laws change.
- **Lockdown** – Age verification, geographic restrictions, disclaimer acceptance.
- **Cookiebot** – Enterprise‑grade cookie consent management; auto‑blocks cookies until consent.

**Implementation tip**: Store policies should be easily accessible (footer, checkout). Enable SSL (Shopify provides free). For GDPR/CCPA, implement cookie banner before loading tracking scripts.

### 2.9 Upsells & Cross‑sells

**Why**: Increase average order value (AOV) with minimal friction.

**Top picks**:
- **ReConvert** – Post‑purchase upsell page (one‑click upsell after checkout). Extremely effective; easy to set up.
- **Hulk Upsell** – In‑cart upsell and post‑purchase offers; multiple offer types.
- **Bundable** or **Kit** – Create product bundles/kits with discounts.

**Implementation tip**: Test different offers: complementary products, "frequently bought together," or a one‑time discount on next purchase. Place upsells immediately after checkout purchase to capture impulse.

### 2.10 Push Notifications

**Why**: Re‑engage visitors and customers without email fatigue.

**Top picks**:
- **PushOwl** – Web push notifications; cart abandonment, back‑in‑stock, price drops. Good deliverability.
- **Klaviyo** – If already using Klaviyo, their push integration is seamless.

**Implementation tip**: Ask for push permission with a clear value (e.g., "Get notified when your item is back in stock" or "Exclusive deals"). Segment by activity and purchase history.

### 2.11 Affiliate & Referral Programs

**Why**: Leverage ambassadors to drive new customers at low cost.

**Top picks**:
- **ReferralCandy** – Automated referral program with rewards for both referrer and referee; easy to implement.
- **Rise** – More customizable; supports tiered rewards, leaderboards, ambassador management.
- **Affiliate** (by Refersion) – For influencer affiliate links; commission tracking.

**Implementation tip**: Offer a compelling reward (e.g., 15% off for both parties). Promote the program via post‑purchase emails and account dashboard.

### 2.12 Inventory & Wholesale

**Why**: Keep inventory in sync across channels; expand to B2B.

**Top picks**:
- **Stocky** – Shopify's own inventory management; demand forecasting, purchase orders, budget tracking (Shopify Plus only).
- **Brightpearl** – Full‑suite ERP for multichannel merchants; inventory, accounting, CRM.
- **Wholesale Gorilla** – Offer wholesale pricing, minimum order quantities, and separate wholesale storefront.

**Implementation tip**: If selling on multiple channels (Amazon, eBay), use a channel integration app like **Codisto** to sync inventory and orders back to Shopify.

## 3. App Hygiene & Maintenance

### 3.1 Monthly Audit
- List all installed apps (Settings > Apps)
- For each, check:
  - Usage: Is it active? Are we using all features?
  - Cost: Is the plan appropriate?
  - Performance: Does it slow down pages? Check via **PageSpeed Insights** or **GTmetrix**.
- Remove unused or redundant apps immediately.

### 3.2 Staging First
- Always test new apps in a duplicate theme or development store before installing on live.
- Check for conflicts with existing apps and theme code.
- Review app embed settings; disable on pages where not needed.

### 3.3 Tag Manager Discipline
- Use **Google Tag Manager** to load non‑essential scripts (heat‑maps, surveys, chat) only on specific pages.
- This reduces the need for apps that inject globally.

### 3.4 Negotiating Plans
- Many app vendors offer discounts for annual commitment or higher‑tier plans if you have high order volume. Ask sales.
- If an app's per‑order fees become burdensome, consider switching or building a custom solution.

## 4. Performance Impact – What to Watch

Every app adds JavaScript. Use these tools to measure impact:

- **PageSpeed Insights** – Look for "Reduce unused JavaScript"
- **Lighthouse** – Check "Reduce JavaScript execution time"
- **GTmetrix** – See "PageSpeed" and "YSlow" scores; view waterfall for script loading

**Red flags**:
- Total JS size > 500KB (excluding critical app bundles)
- Multiple apps loading the same library (e.g., jQuery duplicated)
- Apps that block rendering

If an app is causing performance issues:
1. Check if you can disable its frontend on certain pages (app embeds)
2. Contact developer for an async or lazy load option
3. Replace with a lighter alternative or custom code

## 5. Essential Free Apps

If you're bootstrapping, start with free plans:

- **Judge.me** (reviews) – free with paid upgrades
- **Klaviyo** – free for up to 250 contacts & 500 sends/month
- **Tidio** (chat) – free live chat + chatbots
- **PushOwl** – free for up to 500 subscribers
- **Smart SEO** – free with paid add‑ons
- **Crush.pics** – free for first 500 images/month
- **TermsFeed** – free basic policies; paid for auto‑update

## 6. When to Build Custom Instead of Installing

Consider custom development when:

- The app provides a single, simple feature (e.g., custom checkout field, metafield display)
- Performance budget is tight (< 300KB JS)
- You have in‑house developers and the cost of development < 12 months of app fees
- You need tight integration with existing systems

**Trade‑offs**: Custom code requires maintenance, testing across Shopify updates, and documentation. Apps come with support and updates but add bloat.

## 7. App Portfolio Example for a Mid‑Size Store (100k–500k revenue/month)

| Category | App | Monthly Cost | Notes |
|----------|-----|--------------|-------|
| Reviews | Loox | $99 | Photo reviews |
| Email/SMS | Klaviyo | $200 (based on contacts) | Core automation |
| Support | Gorgias | $360 | Unified inbox |
| Shipping | Shippo | $0–50 | Pay‑as‑you‑go labels |
| Accounting | QuickBooks Online | $150 | |
| SEO | Smart SEO | $20 | Lightweight |
| Performance | Crush.pics | $9.99 | Auto‑compress |
| Compliance | TermsFeed | $15 | Policy generator |
| Upsells | ReConvert | $29 | Post‑purchase |
| Push | PushOwl | $25 | Web push |
| Referral | ReferralCandy | $49 | Ambassador program |
| **Total** | | **~$957** | Approx. |

This stack can yield strong ROI if each app is actively used and contributes to revenue or cost savings.

---

**Navigation**

- [Table of Contents](TOC.md)
- Previous: [Growth & Marketing](growth-marketing.md)
- Next: [Product Photography & Visual Content](product-photography.md)

*End of Must‑Have Shopify Apps chapter*
