# Analytics & Reporting Deep Dive

Data is the lifeblood of e-commerce. Without proper analytics, you're flying blind—optimizing based on gut feelings rather than evidence. This chapter covers everything from basic setup to advanced analysis, helping you make informed decisions that grow your business.

## 1. Why Analytics Matter

### The Data-Driven Advantage
Merchants who regularly review analytics outperform those who don't:
- They know which channels truly convert vs. which just generate clicks
- They identify top-selling products and underperformers early
- They understand customer behavior and can remove friction
- They forecast inventory and cash flow more accurately

### What You Should Track
At a minimum, monitor these metrics weekly:
- **Revenue** and **conversion rate**
- **Traffic sources** and **cost per acquisition**
- **Average order value** (AOV) and **revenue per visitor** (RPV)
- **Customer lifetime value** (LTV) and **repeat purchase rate**
- **Product-level** performance (views, add-to-cart, sold)

## 2. Core Analytics Platforms

### Shopify Native Analytics
Every Shopify store includes built-in reports in **Analytics > Reports**.
**Pros**: Zero setup, real-time data, integrates with orders/customers
**Cons**: Limited customization, basic attribution, no funnel visualization
**Best for**: Daily monitoring, quick sales snapshots, inventory reports

### Google Analytics 4 (GA4)
The industry standard for web analytics. GA4 provides:
- Event-based tracking (flexible and powerful)
- Advanced audience segmentation
- Custom conversions and funnels
- Attribution modeling (data-driven, time decay, position-based)
- Integration with Google Ads, Search Console, Looker Studio

**Setup**:
1. Create a GA4 property (https://analytics.google.com)
2. In Shopify admin, go to **Online Store > Preferences > Google Analytics**
3. Paste your Measurement ID (G-XXXXXXXXXX)
4. Ensure "Enhanced Conversions" is enabled
5. Test with GA4 DebugView or Tag Assistant

**Key configurations**:
- Enable **Enhanced Measurement** (scrolls, outbound clicks, site search)
- Set up **e-commerce events**: `view_item`, `add_to_cart`, `begin_checkout`, `purchase` (Shopify auto-sends some)
- Define **custom dimensions** for product type, customer tier, discount used
- Mark important events as **conversions** (e.g., purchase, email signup)

### Third-Party Analytics Tools
- **Lucky Orange** – Heatmaps, session replays, form analytics; great for UX optimization
- **Hotjar** – Heatmaps, surveys, feedback polls
- **Kissmetrics** – Cohort analysis, funnel visualization, customer journey
- **Glew.io** – Shopify-focused; product affinities, churn prediction, advanced segmentation
- **Prysm** – AI-powered anomaly detection and forecasting

## 3. Essential Metrics & Reports

### Acquisition Metrics
- **Sessions by channel** (Organic, Paid, Direct, Referral, Social, Email)
- **New vs. returning visitors** ratio
- **Cost per acquisition (CPA)** by channel (need ad spend data)
- **Conversion rate** by channel

### Behavior Metrics
- **Bounce rate** – % who leave after one page; aim < 40%
- **Pages per session** – aim > 2
- **Average session duration** – varies by site type
- **Top landing pages** – where do people arrive?
- **Exit pages** – where do they leave? (especially checkout steps)

### Conversion Metrics
- **Overall conversion rate** – sessions that result in purchase; e-commerce average 1-3%
- **Add-to-cart rate** – product page views that add to cart
- **Checkout abandonment rate** – % who start checkout but don't complete
- **Average order value (AOV)** – revenue / number of orders
- **Revenue per visitor (RPV)** – total revenue / sessions

### Customer Metrics
- **Customer lifetime value (LTV)** – total revenue from a customer over lifetime
- **Repeat customer rate** – % of customers who buy again
- **Time between purchases** – average days from first to second order
- **Purchase frequency** – orders per customer per year

### Product Metrics
- **Best-selling products** by units and revenue
- **Product view-to-add-to-cart rate** – indicates product page effectiveness
- **Out-of-stock frequency** – lost sales due to inventory
- **Sell-through rate** – units sold / inventory on hand

## 4. Setting Up GA4 for Shopify

### Step-by-Step
1. **Create GA4 property** (if using existing Universal Analytics, upgrade)
2. Add **measurement ID** in Shopify admin (Online Store > Preferences > Google Analytics)
3. In GA4, go to **Admin > Data Streams > Web**, select your stream
4. Enable **Enhanced Measurement** (scrolls, outbound clicks, site search)
5. Under **Events**, verify Shopify is sending `view_item`, `add_to_cart`, `begin_checkout`, `purchase`
6. Mark `purchase` and any other key actions as **Conversions**

### Custom Dimensions (Optional but Powerful)
Create custom dimensions to segment data:
- `product_type` (from Shopify product type metafield)
- `customer_tier` (e.g., VIP, first-time)
- `discount_used` (yes/no or code)
To set up: Admin > Custom Definitions > Create custom dimension; scope: event; parameter: match your data

### Linking Google Ads & Search Console
- Link Google Ads for auto-tagging and conversion import
- Link Search Console to see organic search queries performance

## 5. Attribution Models

### The Attribution Problem
Which channel gets credit for a sale? Last click says "the last one before purchase." But what about the first touch that introduced the customer? Or the mid-funnel awareness builds?

### Common Models
- **Last click** – 100% to final touch; default in GA4 but often misleading
- **First click** – 100% to first touch; good for top-of-funnel valuation
- **Linear** – equal credit to all touches
- **Time decay** – more credit to touches closer to conversion
- **Position-based** (U-shaped) – 40% to first, 40% to last, 20% distributed to middle
- **Data-driven** – ML algorithm assigns credit based on actual contribution; requires ~15k conversions/month

**Recommendation**: Use data-driven if you have enough data; otherwise position-based is a reasonable compromise.

## 6. Shopify Reports to Master

### Daily/Weekly Check (Shopify Admin)
- **Dashboard** – Today's sales, visitors, top products
- **Sales** – Net sales, returns, taxes
- **Customers** – New customers, returning, locations
- **Product** – Low stock alerts, top products
- **Behavior** – Top online store pages, popular search terms

### Monthly Deep Dive
- **Customer reports** – Cohort analysis (retention by acquisition month)
- **Finance reports** – Payments, fees, refunds
- **Marketing reports** – Conversion by landing page, traffic source
- **Inventory reports** – Sell-through, aging inventory

## 7. Custom Dashboards with Looker Studio

Looker Studio (free) lets you build beautiful, shareable dashboards combining GA4, Shopify, and other data sources.

**Steps**:
1. Go to https://lookerstudio.google.com
2. Create new report, add data sources:
   - Google Analytics 4 (your property)
   - Shopify (via Shopify connector or BigQuery export)
3. Build charts: revenue trend, channel breakdown, product performance
4. Add date range controls and filters (by product, channel)
5. Share with team or schedule email delivery

**Sample Dashboard Layout**:
- Top: Revenue and conversion rate cards (weekly, monthly, YoY)
- Middle: Traffic source breakdown (pie chart, trend)
- Bottom: Top products table with revenue and units
- Side: Customer cohort retention heatmap

## 8. Advanced Analysis Techniques

### Cohort Analysis
Group customers by acquisition month and track their behavior over time:
- What % of Jan cohort purchases again in Feb, Mar, Apr?
- Which acquisition channel brings the highest retention?
- How does lifetime value vary by cohort?

In GA4: Explore > Cohort analysis. In Shopify: Customers > Cohort analysis (if available).

### Funnel Analysis
Map the customer journey and identify drop-off points:
- Home → Collection → Product → Add to cart → Checkout → Purchase
- Where do people leave? Optimize those pages.

In GA4: Explore > Funnel exploration. Define steps and analyze.

### Segment Comparison
Compare behavior of different customer groups:
- New vs. returning
- Mobile vs. desktop
- Geographic regions
- Traffic source

## 9. Action Framework: From Data to Decisions

### Weekly Routine (15 min)
1. Check today's sales vs. target
2. Scan any unusual anomalies (spikes or drops)
3. Review top 5 products; any out of stock or suddenly hot?
4. Check abandonment rate; if high, investigate checkout

### Monthly Deep Dive (1 hour)
1. Calculate LTV by acquisition channel; pause underperformers
2. Identify top 20% of products driving 80% revenue; focus marketing there
3. Review customer retention by cohort; implement winback if needed
4. Update GA4 goals and custom dimensions as business evolves

### Quarterly Strategy (2-3 hours)
1. Full audit of analytics setup; ensure tracking is accurate
2. Build new dashboards or reports for emerging needs
3. Train team on self-service reporting
4. Experiment with new tools (e.g., heatmaps, session replays)

## 10. Common Pitfalls to Avoid

- **No goals set** – If you don't define what "conversion" means, you can't optimize
- **Ignoring assist conversions** – Last click undervalues top-of-funnel; look at assisted conversions report
- **Not segmenting** – Averages hide problems; segment by channel, device, customer type
- **Overlooking time zones** – Shopify uses UTC; GA4 uses property time zone; align them
- **Set and forget** – Analytics configuration drifts as business changes; review quarterly

## 11. Quick Reference: Essential Dashboards

| Dashboard | Purpose | Key Widgets |
|-----------|---------|-------------|
| Daily Ops | Daily monitoring | Sales, orders, visitors, top products |
| Marketing ROI | Channel effectiveness | Sessions, conversions, CPA, RPV by channel |
| Customer Health | Retention & LTV | Repeat rate, cohort chart, LTV trend |
| Product Performance | Inventory & merchandising | Views, ATC, sold, sell-through |
| Checkout Funnel | Conversion optimization | Drop-off rates at each step |

---

**Navigation**

- [Table of Contents](TOC.md)
- Previous: [Shopify AI & Automation](ai-automation.md)
- Next: [Multichannel & Marketplace Selling](multichannel-marketplace.md)

*End of Analytics & Reporting Deep Dive chapter*
