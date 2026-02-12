# Technical Setup

This chapter walks through the technical foundation of a Shopify store: from initial store setup to must-have apps and performance best practices.

## 1. Setting Up Your Shopify Store

### 1.1 Create Your Store
- Sign up for a Shopify plan (14-day free trial available)
- Choose a store name (this becomes your default `*.myshopify.com` URL)
- Verify your email and set up two-factor authentication

### 1.2 Custom Domain
- Purchase a custom domain through Shopify or your registrar
- Connect the domain in **Online Store > Domains**
- Enable SSL (Shopify provides free SSL automatically)
- Set primary domain to your custom domain (not the `.myshopify.com`)

### 1.3 Store Configuration Basics
- **General settings**: Store address, currency, time zone, units of measurement
- **Notifications**: Customize email templates (order confirmations, shipping updates)
- **Payments**: Enable Shopify Payments (if available) and complementary gateways (PayPal, Stripe)
- **Shipping**: Configure shipping zones, rates, and package dimensions
- **Taxes**: Set up automatic tax rates or manual overrides as needed
- **Checkout**: Customize checkout options (account creation, order comments, social login)

## 2. Essential Shopify Apps

A minimal, high-performing store uses only necessary apps. Avoid bloat.

### 2.1 Product Reviews & Social Proof
- **Loox** or **Judge.me** – Photo & text reviews with automated email prompts
- Key features: automated review requests, review attachments, Q&A, syndication to Google Shopping

### 2.2 Email & SMS Marketing
- **Klaviyo** – Advanced segmentation, automation flows (welcome series, abandoned cart, browse abandonment, winback)
- Alternative: **Omnisend** for multi-channel campaigns
- Integrate with Shopify data (purchases, browsing behavior) for personalization

### 2.3 Customer Support
- **Gorgias** or **Zendesk** – Unified support inbox (email, chat, messenger, Instagram, WhatsApp)
- Features: macros, automation, order context, FAQ self-service

### 2.4 Shipping & Fulfillment
- **ShipStation** or **Shippo** – Rate shopping, label printing, tracking sync
- For 3PL: **ShipHero** or **Cogolligan** (depending on provider)
- Consider **Parcelify** for custom shipping rules

### 2.5 Accounting & Finance
- **QuickBooks Online** or **Xero** – Sync orders, taxes, refunds
- For Stripe/Shopify Payments: built-in payouts tracking

### 2.6 SEO & Content
- **Smart SEO** or **SEO Manager** – Meta tags, structured data, sitemap, SEO audits
- **Blog** – Use Shopify's native blog for content marketing

### 2.7 Performance & Optimization
- **Crush.pics** or **ImageOptim** – Automatically compress images on upload
- **Boost Filter & Search** – Instant search, smart collections filtering (if many products)
- **PageSpeed optimization** – Use a fast, well-coded theme and minimize app script bloat

### 2.8 Compliance & Legal
- **TermsFeed** or **Lockdown** – Generate privacy policy, terms of service, cookie consent (GDPR/CCPA)
- **Age verifier** if selling restricted products

### 2.9 Upsells & Cross-sells
- **ReConvert** or **Hulk Upsell** – Post-purchase upsells (one-click post-purchase upsell is native to Shopify Plus)
- In-cart upsell apps: **Upsell.io**, **CartHook**

## 3. Theme Selection & Customization

### 3.1 Choose a Fast Theme
- Recommended: **Dawn** (free, headless-ready, performant)
- Other quality options: **Turbo**, **Warehouse**, **Venus**, **Motion** (paid themes from reputable developers)
- Avoid heavily bloated themes with hundreds of unused features

### 3.2 Theme Customization
- Use **Online Store > Themes > Customize** for point-and-click changes
- For advanced changes, duplicate the theme and edit Liquid templates / CSS
- Always test on staging before pushing to live

### 3.3 Mobile-First & Accessibility
- Ensure theme is responsive (Shopify themes are, but verify content readability)
- Check color contrast, font sizes, keyboard navigation
- Use Lighthouse to audit accessibility

## 4. Performance Best Practices

### 4.1 Core Web Vitals
- **LCP** (< 2.5s): Optimize images (WebP, size < 150KB), lazy load, use CDN
- **CLS** (< 0.1): Reserve space for dynamic elements (ads, embeds), set explicit dimensions
- **INP** (< 200ms): Minimize main thread work, reduce JavaScript size, defer non-critical tasks

### 4.2 Image Optimization
- Use **Shopify's CDN** for images; it automatically resizes and serves WebP
- Limit apps that inject heavy scripts (analytics, chat widgets); use tag manager to control load
- Enable **gzip compression** (Shopify does this by default)

### 4.3 App Hygiene
- Regularly audit installed apps; remove unused ones
- Check app impact via **Online Store > Themes > App embeds** and disable where not needed
- Use **Google Tag Manager** to manage third-party scripts and fire on specific pages only

## 5. Security & Compliance

- Enforce **strong passwords** for staff accounts; limit staff permissions
- Keep **Shopify and apps updated** (Shopify updates automatically; apps update via dashboard)
- Use **IP restrictions** for staff logins if possible (Shopify Plus feature)
- **PCI compliance** is Shopify's responsibility; ensure you're on a Shopify plan that covers this
- **GDPR/CCPA**: Add cookie consent banner (via app), update privacy policy, enable data deletion requests

## 6. Testing Before Launch

- Place **test orders** (using Shopify's Bogus Gateway) to validate checkout flow, emails, inventory
- Test **mobile checkout** on multiple devices
- Verify **shipping rates**, tax calculation, and payment capture/refund
- Check **email notifications** (order confirmation, shipping, canceled, fulfilled)
- Ensure **Google Analytics/Meta Pixel** are firing correctly (use tag assistant)
- Perform a **Lighthouse audit** and fix major issues

---

**Navigation**

- [Table of Contents](TOC.md)
- Next: [Growth & Marketing](growth-marketing.md)

*End of Technical Setup chapter*
