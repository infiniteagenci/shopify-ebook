# Research Notes: Analytics & Reporting for Shopify

## Why Analytics Matter
- Data-driven decisions outperform gut feelings
- Identify what's working and what's wasting money
- Track customer behavior, product performance, marketing ROI
- Forecast sales and inventory needs

## Core Analytics Platforms

### Shopify Native Analytics
- Built into Shopify admin (no setup required)
- Reports: Sales, Customers, Behavior, Finance
- Limited customization; good for basic monitoring
- Real-time dashboard

### Google Analytics 4 (GA4)
- Industry standard; deeper insights
- Tracks events, conversions, user journey
- Integration: Use Shopify's native GA4 integration or Google Tag Manager
- Set up custom dimensions (product type, customer tier)
- Goals: track checkout steps, email signups, etc.

### Third-Party Analytics
- **Lucky Orange** – Heatmaps, session recordings, form analytics
- **Hotjar** – Heatmaps, surveys, feedback
- **Kissmetrics** – Cohort analysis, funnel visualization
- **Glew.io** – Advanced Shopify-specific analytics (product affinities, churn prediction)

## Key Metrics to Track

### Acquisition
- Sessions by channel (organic, paid, direct, referral, social)
- New vs returning visitors
- Cost per acquisition (CPA) by channel
- Conversion rate by channel

### Behavior
- Bounce rate (goal < 40%)
- Pages per session (goal > 2)
- Average session duration
- Top landing pages
- Exit pages (where people drop off)

### Conversion
- Overall conversion rate (e-commerce) – industry average 1-3%
- Add-to-cart rate
- Checkout abandonment rate (and steps)
- Average order value (AOV)
- Revenue per visitor (RPV)

### Customer
- Customer lifetime value (LTV)
- Repeat customer rate
- Time between first and second purchase
- Purchase frequency

### Product
- Best-selling products (by units, revenue)
- Product view-to-add-to-cart rate
- Out-of-stock frequency

## Setting Up GA4 Correctly

### Data Stream Setup
- Create GA4 property (or use existing)
- Add measurement ID to Shopify admin (Online Store > Preferences > Google Analytics)
- Enable enhanced measurements (scroll, outbound clicks, site search)

### Events to Configure
- `purchase` (Shopify auto-sends with revenue)
- `begin_checkout`, `add_to_cart`, `view_item`
- `email_signup` (if using Klaviyo or custom)
- Custom events for key actions (e.g., "video_played", "360_view")

### E-commerce Settings
- Turn on "Enhanced Measurement" for site content
- Set up "User-ID" if you have logged-in customers (advanced)
- Link Google Ads and Search Console for full attribution

## Attribution Models

### Last Click (Default)
- Gives 100% credit to last touchpoint before conversion
- Penalizes top-of-funnel; easy to understand but misleading

### Data-Driven (GA4)
- Uses machine learning to assign credit across touchpoints
- Requires sufficient data (conversions > 15k/month typically)
- More accurate but complex

### Time Decay
- Credit distributed with more weight to recent touches
- Good for short sales cycles

### Position-Based (U-Shaped)
- 40% to first touch, 40% to last touch, 20% distributed to middle
- Balanced view

## Shopify Reports to Monitor Weekly

- **Dashboard** – Quick overview (sales, visitors, top products)
- **Sales** – Net sales, returns, gift cards
- **Customers** – New vs returning, location, lifetime spend
- **Product** – Inventory levels, sell-through rate
- **Behavior** – Top online store pages, landing pages
- **Finance** – Payments, taxes, refunds

## Custom Dashboards

- Use **Looker Studio** (free) to combine GA4, Shopify, and other sources
- Build a single view with:
  - Revenue trend
  - Channel performance
  - Product performance
  - Customer cohort retention
- Share with team; schedule email reports

## Cohort Analysis

- Group customers by acquisition month/cohort
- Track retention over time (month 1, month 2, month 3 repeat rates)
- Identify which channels bring best long-term value
- Compare product variations (e.g., customers who bought product A vs B)

## Advanced: Predictive Analytics

- Shopify's built-in "predicted next order" value
- Churn prediction (custom via ML models)
- Discount elasticity modeling (how much lift from X% off?)

## Common Pitfalls

- Not setting up goals/conversions; flying blind
- Relying on last-click attribution only
- Ignoring mobile vs desktop breakdowns
- Not segmenting data (by customer type, product category)
- Overlooking time zones (data resets at midnight UTC)

## Action Framework

1. **Week 1**: Install GA4, verify data, set up basic conversions
2. **Week 2**: Create custom dashboards; identify top 5 metrics to track daily
3. **Week 3**: Build cohort analysis; calculate baseline LTV
4. **Ongoing**: Weekly review of key metrics; monthly deep dive

---

**Navigation**

- [Table of Contents](TOC.md)
- Previous: [Shopify AI & Automation](ai-automation.md)
- Next: [Multichannel & Marketplace Selling](multichannel-marketplace.md)

*End of Analytics & Reporting chapter*
