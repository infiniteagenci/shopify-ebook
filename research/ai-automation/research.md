# Research Notes: Shopify AI & Automation Features

## Shopify Sidekick (AI Assistant)

### What It Is
Shopify Sidekick is an AI-powered assistant embedded directly into the Shopify admin. It helps merchants with various tasks using natural language.

### Capabilities
- **Answer questions**: "How do I set up a discount code?" "What's my best-selling product last month?"
- **Generate content**: Draft product descriptions, email subject lines, social posts
- **Analyze data**: Summarize sales trends, customer behavior, inventory status
- **Make suggestions**: Recommend apps, theme optimizations, shipping settings
- **Perform actions** (with confirmation): Create discount codes, update product tags, adjust prices
- **Troubleshoot**: Walk through common issues (checkout errors, app conflicts)

### Access & Availability
- Included with certain Shopify plans ( typically Plus or via add-on)
- Available in Shopify admin sidebar as a chat interface
- Powered by large language models (likely GPT-4/Claude) with Shopify data integration

### Use Cases
- New store setup guidance
- Quick answers without leaving admin
- Content creation at scale (batch product descriptions)
- Data exploration ("what were top products in November?")
- Automation suggestions (create flows for abandoned carts)

### Limitations
- Not a fully autonomous agent; human oversight needed
- Actions require confirmation for safety
- Knowledge cutoff and scope limited to Shopify operations
- May not handle highly custom or complex requests

## Shopify Flow (Automation App)

### What It Is
Shopify Flow is a visual workflow builder that automates repetitive tasks by connecting triggers, conditions, and actions across Shopify and integrated apps.

### Core Concepts
- **Trigger**: Something that starts the flow (e.g., order created, product tagged, customer signed up)
- **Condition**: Branch logic (if/then) based on data
- **Action**: What happens next (e.g., send email, add tag, create task, call webhook)

### Popular Flows
1. **Abandoned cart recovery**: When cart abandoned >1 hour → tag customer → send email via Klaviyo
2. **High-value order alerts**: Order > $500 → Slack notify → priority fulfillment
3. **Customer segmentation**: When customer placed 3rd order → move to VIP segment → unlock loyalty benefits
4. **Inventory management**: Product out of stock → create Trello task → notify team
5. **Review request**: Order fulfilled → wait 7 days → email review request

### Integrations
- Native Shopify actions (orders, products, customers, tags)
- Popular apps: Klaviyo, Trello, Slack, Google Sheets, webhooks to external APIs
- Limited to installed apps that have Flow connectors

### Building Flows
- Use drag-and-drop interface in Shopify admin (no code)
- Templates available for common automations
- Test mode to simulate runs before going live
- Activity log to see executed flows and debug

## Other AI-Powered Features

### AI Product Descriptions
- Shopify now offers AI-generated product descriptions
- Input a few keywords or bullet points; AI writes full copy
- Available in product editor; can customize tone (luxury, casual, etc.)
- Saves time for large catalogs

### AI Image Generation (as already documented in product-photography.md)
- Generate product images from text prompts
- Useful for mockups or lifestyle shots

### Predictive Analytics
- Shopify Analytics uses ML to forecast sales, predict churn, recommend products
- Built into reports (e.g., "predicted next order" for customers)
- No setup required; automatically uses historical data

### Smart Reordering
- AI suggests reorder quantities based on sales velocity, seasonality, lead time
- Available in Shopify admin > inventory

## Comparing Sidekick vs Flow

| Feature | Sidekick | Flow |
|---------|----------|------|
| Interaction | Chat-based (conversational) | Visual builder (if-then) |
| Ideal for | One-off questions, content creation, data queries | Repeating automated workflows |
| Example | "Write a product description for a leather wallet" | "When order is created, tag as 'new' and send welcome email" |
| Execution | Manual or semi-automated (confirm actions) | Fully automated (runs in background) |
| Complexity | Simple to moderate | Simple to complex (multiple branches) |

## Implementation Roadmap

### Phase 1: Explore Sidekick
- Access Sidekick in admin (if plan includes)
- Try 5-10 common questions to gauge helpfulness
- Use for content generation on a few products
- Train team to use Sidekick for daily tasks

### Phase 2: Build Core Flows
- Identify top 3 manual processes (abandoned cart, order alerts, review requests)
- Implement using Flow templates or custom builds
- Test thoroughly; monitor logs
- Expand to other areas (inventory, customer tagging)

### Phase 3: Advanced Integrations
- Connect Flow to external systems (CRM, ERP) via webhooks
- Use Sidekick to design flows ("create a flow that...")
- Monitor AI-generated content for quality; add human review if needed

## Risks & Mitigations

- Over-reliance on AI: Human oversight essential for accuracy and brand voice
- Data privacy: Sidekick does not send data to third parties (Shopify-hosted AI)
- Flow misconfiguration: Can cause unwanted actions; use test mode and logs
- Cost: Both features may require pricier Shopify plan or add-on

## Conclusion
Shopify's AI and automation tools dramatically reduce manual work for merchants. Sidekick is your always-available assistant; Flow is your tireless automation engine. Together, they can streamline operations, improve marketing, and scale your business without adding headcount.
