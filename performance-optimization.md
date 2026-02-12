# Technical Debt & Performance Optimization

Shopify stores often accumulate technical debt that impacts user experience and SEO. This chapter covers diagnosing and solving performance issues, managing app bloat, and maintaining a lean, fast store.

## 1. Diagnosing Performance Problems

### 1.1 Core Web Vitals (CWV) Benchmarks
Google uses CWV as a ranking factor. Aim for:
- **LCP** (Largest Contentful Paint): < 2.5s
- **INP** (Interaction to Next Paint): < 200ms
- **CLS** (Cumulative Layout Shift): < 0.1

Use **PageSpeed Insights** (https://pagespeed.web.dev/) to test key pages (homepage, product, collection, cart, checkout).

### 1.2 Common Performance Bottlenecks
- **Large images** (>150KB, not WebP)
- **Unoptimized JavaScript** from multiple apps
- **Render-blocking resources** (non-critical CSS/JS)
- **Web fonts** loading slowly
- **Third-party scripts** (chat widgets, analytics, ads) firing on every page
- **Theme code bloat** (unused sections, heavy animations)

## 2. Image Optimization

### 2.1 Shopify CDN Basics
Shopify automatically serves images via CDN and converts to WebP when supported. However:
- Don't upload oversized images (>2000px). Shopify resizes but large originals increase processing time.
- Use **Shopify's image filters** (`resize: 800x800` etc.) to serve appropriate sizes.

### 2.2 Manual Optimization
- Pre-compress images using **Squoosh**, **ImageOptim**, or **TinyPNG** before uploading
- Use modern formats (WebP, AVIF) where supported
- Lazy load below‑the‑fold images (Shopify themes usually do this; verify)

### 2.3 Video Optimization
- Host videos on **YouTube** or **Vimeo** and embed (don't upload to Shopify)
- For self‑hosted, enable **adaptive streaming** or use a service like **Mux**

## 3. Reducing App Bloat

### 3.1 Audit Your Apps
- Go to **Apps** and list all installed apps
- For each app, ask: "Does this directly increase revenue or reduce costs?"
- Remove unused or redundant apps

### 3.2 App Script Loading
Many apps inject JavaScript on every page, even where not needed. Use:
- **App Embeds** (in your theme) to disable app scripts on specific pages
- **Google Tag Manager** to load certain tags only on specific pages/events
- **Manual script injection** via theme instead of app, if possible (e.g., custom pixel code)

### 3.3 Alternative: Custom Development
If an app provides a small feature, consider building it as a lightweight theme section or snippet. This avoids third‑party script overhead. Weigh development cost vs. ongoing app fees.

## 4. Theme Optimization

### 4.1 Choose a Fast Theme
- **Dawn** (free) is highly optimized; start here
- Paid themes: ensure they have a performance reputation
- Avoid "all‑in‑one" themes with hundreds of unused sections

### 4.2 Lazy Load Sections
Use Shopify's native lazy loading for images and sections:
```liquid
<div loading="lazy">...content...</div>
```
Or use **Scroll** sections that only load when in view.

### 4.3 Defer Non‑Critical JS
Move analytics and tracking scripts to load after `DOMContentLoaded` or via `requestIdleCallback()`.

### 4.4 Minimize Liquid Complexity
- Avoid deep nested loops
- Cache repeated queries using `{% render 'component' %}` with parameters
- Use `section` and `block` efficiently; don't create thousands of sections

## 5. Third‑Party Script Management

### 5.1 Tag Manager Approach
Load all non‑essential scripts (chat, heatmaps, surveys) through **Google Tag Manager** and fire them only on needed pages or after user interaction.

### 5.2 Privacy & Consent
- Implement a **cookie consent banner** (via app or custom)
- Delay tracking scripts until consent given (GDPR/CCPA compliance)
- Use **first‑party** data collection where possible

## 6. Checkout Performance

### 6.1 Shopify Checkout
Shopify's hosted checkout is already performance‑optimized. Don't customize it heavily (Shopify Plus only allows limited modifications). Ensure:
- No custom scripts added (Shopify blocks them by default for PCI compliance)
- Shipping and payment options are streamlined
- Mobile checkout is tested on real devices

### 6.2 Accelerated Checkout
Enable **Shop Pay** for one‑tap checkout – it dramatically improves conversion and reduces friction.

## 7. Continuous Monitoring

### 7.1 Automated Alerts
Set up **Google Search Console** to monitor Core Web Vitals and get alerts when they drop.
Use **Lighthouse CI** in your development workflow to catch regressions.

### 7.2 A/B Testing Performance
When making changes, test in a staging environment and measure impact using **PageSpeed Insights** or **WebPageTest**.

### 7.3 Regular Audits
- Monthly: Review installed apps and remove unused ones
- Quarterly: Run full performance audit and create a roadmap for improvements
- Before major sales/events: Stress test with load testing tools (e.g., **k6**, **Loader**)

## 8. Leveraging Shopify's Infrastructure

- Use **Shopify's CDN** for all assets (images, JS, CSS)
- Enable **HTTP/2** (automatic on Shopify)
- Minimize redirects; fix broken links
- Use **Shopify's search** (or Algolia if large catalog, but adds JS)

## 9. Case Study: Before & After

A store with 20+ apps, heavy theme, and unoptimized images achieved:
- LCP reduced from 4.2s to 1.8s
- INP improved from 350ms to 120ms
- Mobile conversion rate increased by 22%
- Search rankings improved for key terms

Actions taken:
- Removed 8 unused apps
- Compressed all images (WebP, <100KB)
- Disabled app embeds on non‑essential pages
- Switched to Dawn theme with minimal customizations
- Implemented GTM for analytics and chat

---

**Navigation**

- [Table of Contents](TOC.md)
- Previous: [Technical Setup](technical-setup.md)
- Next: [Marketing Attribution in a Privacy‑First World](marketing-attribution.md)

*End of Technical Debt & Performance Optimization chapter*
