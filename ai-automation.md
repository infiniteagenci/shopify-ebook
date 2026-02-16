# Shopify AI & Automation

Shopify has been rapidly integrating artificial intelligence and workflow automation into its platform. Two major tools—**Shopify Sidekick** and **Shopify Flow**—empower merchants to work smarter, automate repetitive tasks, and leverage AI without leaving the admin. This chapter covers what these tools do, how to use them, and how to integrate them into your operations.

## 1. Shopify Sidekick: Your AI Assistant

### What Is Sidekick?
Sidekick is an AI-powered assistant built into the Shopify admin. It answers questions, generates content, analyzes data, and even performs actions on your behalf (with confirmation). Think of it as ChatGPT specialized for Shopify.

### How to Access
Sidekick is typically available in the sidebar of your Shopify admin (icon: a chat bubble or magic wand). Availability depends on your Shopify plan (often included with Plus or as an add-on).

### What You Can Do with Sidekick

#### Ask Questions
Sidekick can answer a wide range of questions about your store, Shopify features, and best practices:
- "How do I create a discount code for 20% off?"
- "What were my top-selling products last month?"
- "How do I set up Google Merchant Centre?"
- "Why is my checkout not working?"

It pulls from your store data (sales, products, customers) and Shopify's documentation to provide contextual answers.

#### Generate Content
Sidekick can draft marketing copy, product descriptions, email subjects, and more:
- "Write a product description for a handmade leather wallet, emphasizing durability and craft"
- "Suggest 5 email subject lines for a winter sale"
- "Create a Instagram caption for our new running shoe"

You can refine the output by providing tone, length, and keywords.

#### Analyze Data
Instead of building custom reports, ask Sidekick:
- "What's my customer retention rate this quarter?"
- "Which traffic channel has the highest conversion?"
- "Show me products with low inventory but high sales"

It will summarize data from your Shopify Analytics and present insights in plain language.

#### Take Actions (with Confirmation)
Sidekick can perform certain admin actions after you confirm:
- "Create a discount code 'SUMMER20' for 20% off"
- "Tag all customers from last week's email list as 'Newsletter-Q1'"
- "Increase price of product XYZ by $5"
- "Duplicate this product and change the color to blue"

This speeds up repetitive tasks while maintaining safety.

#### Troubleshoot
When something goes wrong, describe the issue to Sidekick:
- "Customers can't complete checkout"
- "My theme is broken after installing an app"
- "Images aren't loading on collection pages"

Sidekick will walk you through diagnostic steps or suggest fixes.

### Best Practices for Using Sidekick
- **Be specific**: Instead of "write a description", say "Write a 100-word product description for a yoga mat, highlighting eco-friendly materials and non-slip grip, tone: professional and trustworthy"
- **Review outputs**: AI can make mistakes or produce generic copy; always edit for brand voice and accuracy
- **Use store context**: Sidekick knows your products, orders, and customers—you can refer to them by name
- **Iterate**: If the first answer isn't quite right, ask for refinement or more detail
- **Teach your team**: Sidekick can onboard new staff quickly; they can ask "How do I process a return?" instead of reading manuals

### Limitations
- Not all Shopify plans include Sidekick; check your admin
- Actions that affect billing or critical settings may not be allowed
- Knowledge cutoff may mean it doesn't know about the very latest features
- It's an assistant, not a replacement for human judgment on strategic decisions

## 2. Shopify Flow: No-Code Automation

### What Is Flow?
Shopify Flow is a visual workflow builder that automates tasks across Shopify and connected apps. Unlike Sidekick's conversational interface, Flow uses triggers, conditions, and actions to create recurring automated processes.

### When to Use Flow vs. Sidekick
- **Sidekick**: One-off tasks, questions, content creation, ad-hoc analysis
- **Flow**: Repeatable automations that run in the background (e.g., "when an order is placed, do X, Y, Z")

You can even use Sidekick to help design Flow workflows by describing what you want to automate.

### Core Components
- **Trigger**: Event that starts the flow (e.g., "Order created", "Product tagged", "Customer signed up")
- **Condition**: Branch logic (if/then) based on data (e.g., "if order total > $100", "if customer has tag VIP")
- **Action**: What happens next (e.g., "Send email via Klaviyo", "Add tag to customer", "Create task in Trello", "Send Slack message")

### Getting Started
1. In Shopify admin, go to **Settings > Automations** (or **Flow**)
2. Click **Create workflow** (or use a template)
3. Choose a trigger from the list
4. Add conditions as needed (optional)
5. Add actions (one or multiple)
6. Test with sample data
7. Publish

### Essential Flows to Build

#### Abandoned Cart Recovery
- Trigger: Checkout started but not completed in 2 hours
- Condition: Cart total > $20
- Actions:
  - Add tag "abandoned-cart" to customer
  - Send email via Klaviyo (abandoned cart series)
  - Optional: create Slack notification for high-value carts

#### Order Confirmation & Updates
- Trigger: Order paid or fulfilled
- Actions:
  - Send confirmation email (Shopify native or Klaviyo)
  - Post to Slack/Discord channel
  - Add customer to segment (e.g., "Purchaser")

#### Review Request Automation
- Trigger: Order fulfilled (or delivered via carrier status)
- Condition: Wait 7 days
- Actions:
  - Send email requesting review (via Judge.me, Loox, or Klaviyo)
  - If review not left after 3 days, send reminder

#### High-Value Customer Alerts
- Trigger: Customer places 3rd order or lifetime spend > $500
- Actions:
  - Add tag "VIP"
  - Send thank you email with loyalty offer
  - Create task in CRM for account manager

#### Inventory & Supplier Management
- Trigger: Product inventory drops below threshold
- Actions:
  - Send email to purchasing manager
  - Create Trello card in "Restock" board
  - Update Google Sheet inventory log

#### Customer Support Routing
- Trigger: Support ticket created (via Gorgias/Zendesk)
- Condition: Contains keywords "urgent", "refund", "broken"
- Actions:
  - Escalate to senior agent
  - Set priority high
  - Slack notify support lead

### Integrating External Apps
Flow works with many popular apps via native connectors:
- **Klaviyo**: Trigger on email events, add/remove from lists
- **Gorgias**: Create/update tickets based on events
- **Trello/Asana**: Create tasks, update boards
- **Google Sheets/Drive**: Append rows, create files
- **Slack/Discord**: Send messages to channels
- **Webhooks**: Call any external API (for custom integrations)

### Testing & Monitoring
- Always test flows in **sandbox** or with a single test order before activating
- Check the **Flow activity log** to see runs, successes, and failures
- Set up error notifications (use Slack or email actions on flow failure)
- Review monthly to remove obsolete flows

## 3. Other AI-Powered Shopify Features

### AI Product Descriptions
Shopify's AI can write product descriptions from a few bullet points. In the product editor, look for "Generate description" or "AI tools". You can specify tone (playful, luxury, technical) and length. This is great for bulk updates.

### Predictive Analytics
Shopify Analytics uses ML to forecast sales, predict customer lifetime value, and identify at-risk customers. These insights appear in reports without any setup.

### Smart Reordering
AI suggests optimal reorder quantities based on sales trends, lead times, and seasonality. Available in the inventory section.

### AI-Powered Search
Shopify's search uses AI to understand natural language queries (e.g., "red shoes under $50") and personalize results.

## 4. Building Your AI & Automation Strategy

### Start with Pain Points
Identify repetitive manual tasks:
- How many hours per week do you spend on content writing?
- What tasks are error-prone when done manually?
- Which processes slow down order fulfillment?

### Implement in Phases
1. **Sidekick adoption**: Train team to use Sidekick for questions and content; track time saved
2. **Core flows**: Build 3-5 high-impact automations (abandoned cart, review requests, VIP tagging)
3. **Advanced integrations**: Connect Flow to external tools (CRM, project management)
4. **Iterate**: Review flows quarterly; prune unused ones; add new as needs evolve

### Measure Impact
- Time saved per week (track manually or estimate)
- Error rate reduction (fewer manual mistakes)
- Conversion improvements (from timely abandoned cart emails, etc.)
- Team satisfaction (less repetitive work)

### Cautions
- Don't automate everything; some decisions need human judgment
- Monitor AI-generated content for brand voice and accuracy
- Avoid over-tagging or spamming customers with automated messages
- Keep compliance in mind (GDPR, CAN-SPAM) even with automation

## 5. Resources

- Shopify Help Center: "Using Shopify Sidekick"
- Shopify Flow documentation and template gallery
- Partner apps that extend Flow (search "Shopify Flow" in App Store)
- Community forums for workflow ideas

---

**Navigation**

- [Table of Contents](TOC.md)
- Previous: [Must‑Have Shopify Apps](must-have-apps.md)
- Next: [Analytics & Reporting Deep Dive](analytics-reporting.md)

*End of Shopify AI & Automation chapter*
