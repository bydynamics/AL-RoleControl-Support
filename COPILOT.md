# Role Control - Copilot Features

Role Control includes AI-powered capabilities using Microsoft Copilot to help you generate Role Centers and tiles automatically.

## Overview

The Copilot feature uses Azure OpenAI to understand your business requirements and generate complete Role Center configurations, including tiles, filters, and layouts.

## Prerequisites

- Business Central Online (SaaS)
- Copilot features must be enabled in your environment
- Business Central version 26.0 or higher

## Features

### 🤖 AI-Powered Role Center Generation

Generate complete Role Centers by describing your needs in natural language.

**Example prompts:**
- *"Create a sales manager role center with customer insights, open orders, sales KPIs, and pending approvals"*
- *"Generate a warehouse role center focused on inventory levels and pending shipments"*
- *"Build a finance role center with payment reminders and cash flow analysis"*

### 🎯 Intelligent Tile Suggestions

Copilot analyzes your prompt and suggests:
- Relevant Business Central tables to monitor
- Appropriate calculation types (Count, Sum, Average, etc.)
- Meaningful tile descriptions
- Suitable filter configurations
- Optimal tile grouping and layout

### 📊 Smart Configuration

The AI automatically:
- Validates that suggested tables exist in Business Central
- Ensures field compatibility with calculation types
- Groups related tiles logically
- Suggests appropriate drill-down pages
- Recommends useful filters

## How to Use

### Generating a New Role Center

1. Open **Role Control** from the search
2. Navigate to **Dynamic Role Centers**
3. Click **Generate with Copilot** (sparkle icon ✨)
4. In the Copilot prompt window:
   - Describe your desired Role Center
   - Be specific about the data you want to track
   - Mention user roles or departments if relevant
5. Click **Generate**
6. Review the suggested Role Center and tiles
7. Click **Apply** to create the configuration

### Using Prompt Templates

The Copilot page includes quick-start templates:

- **Sales Manager Role Center**
  - Customer insights
  - Open orders tracking
  - Sales KPIs
  - Pending approvals

- **Purchase Manager Role Center**
  - Vendor management
  - Purchase orders
  - Pending receipts
  - Budget tracking

- **Warehouse Manager Role Center**
  - Inventory levels
  - Pending shipments
  - Stock transfers
  - Location overview

### Refining Results

After generation, you can:
- **Edit tiles**: Modify descriptions, calculations, or filters
- **Add more tiles**: Use Copilot again or add manually
- **Adjust layout**: Change tile groups and sequences
- **Configure filters**: Add personal filters or default filters

## Best Practices

### Writing Effective Prompts

✅ **Good prompts:**
- *"Create a role center for credit controllers showing overdue invoices in aging buckets (30, 60, 90 days) and customer payment history"*
- *"Build a production manager dashboard with work orders by status, machine capacity, and material shortages"*

❌ **Less effective prompts:**
- *"Make a sales thing"* (too vague)
- *"I need everything about customers"* (too broad)

### Tips for Better Results

1. **Be Specific**: Mention specific data points you want to track
2. **Include Context**: Describe the user role or department
3. **Mention Grouping**: Suggest how tiles should be organized
4. **Specify Metrics**: State if you need counts, sums, or averages
5. **Reference BC Concepts**: Use Business Central terminology (e.g., "Sales Orders", "Customer Ledger Entries")

## Data Processing & Privacy

### How Copilot Works

1. Your prompt is sent to Azure OpenAI Service
2. AI analyzes your request and Business Central structure
3. Suggestions are generated based on standard BC tables
4. Results are returned to your session
5. No configuration is saved until you click **Apply**

### Data Usage

**What is sent to Azure OpenAI:**
- Your natural language prompt
- Business Central table/field metadata (public schema information)
- Your selected Business Central version

**What is NOT sent:**
- Your actual business data
- Customer records
- Transaction data
- Personal information
- Company-specific configurations

### Privacy & Compliance

- All data transmission uses encrypted connections (HTTPS)
- Azure OpenAI complies with GDPR and Microsoft privacy standards
- Prompts are not used to train AI models
- No data is retained after your session
- Full compliance with Microsoft's Responsible AI principles

### Opting Out

Copilot features can be disabled:
1. Go to **Copilot & AI Capabilities** in Business Central
2. Find **Role Center Generation (bydynamics)**
3. Set to **Disabled**

## Limitations

### Current Limitations

- ⚠️ Only available in Business Central Online (SaaS)
- ⚠️ Requires active Azure OpenAI connection
- ⚠️ Advanced custom functions must be configured manually
- ⚠️ Complex filter logic may need manual adjustment

### Known Issues

- Very complex prompts with multiple unrelated requirements may produce suboptimal grouping
- Custom table suggestions may require manual table ID entry
- Some industry-specific terminology may not be recognized

## Troubleshooting

### "Copilot is not available"

**Possible causes:**
- Environment is On-Premises (not supported)
- Copilot features disabled in environment settings
- Azure OpenAI service configuration issue

**Solution:**
- Verify you're using Business Central Online
- Check **Copilot & AI Capabilities** settings
- Contact support if issues persist

### "Failed to generate suggestions"

**Possible causes:**
- Network connectivity issues
- Azure OpenAI service temporarily unavailable
- Invalid prompt format

**Solution:**
- Check internet connection
- Try again in a few moments
- Simplify your prompt
- Use a template prompt as starting point

### "No tiles generated"

**Possible causes:**
- Prompt too vague or ambiguous
- No matching BC tables found
- Request outside BC scope

**Solution:**
- Be more specific about data you want to track
- Use Business Central terminology
- Reference specific BC modules (Sales, Purchase, Inventory, etc.)

## Examples

### Example 1: Sales Dashboard

**Prompt:**
```
Create a sales manager role center with three groups:
1. Customer insights: active customers, top 10 customers by revenue
2. Orders: open sales orders, orders ready to ship, backorders
3. Performance: monthly sales total, average order value
```

**Generated Result:**
- Group 1: 2 tiles (Customer count, Top customers)
- Group 2: 3 tiles (Open orders, Ready to ship, Backorders)
- Group 3: 2 tiles (Sales amount, Average value)

### Example 2: Warehouse Operations

**Prompt:**
```
Build a warehouse role center focused on inventory management with stock levels by location, items below reorder point, and pending put-aways
```

**Generated Result:**
- Group 1: Inventory overview tiles
- Group 2: Reorder warnings and stock alerts
- Group 3: Pending warehouse activities

## Support

For Copilot-related questions:
- Check [FAQ](FAQ.md)
- Report issues on [GitHub](https://github.com/bydynamics/AL-RoleControl-Support/issues)

## Learn More

- [Microsoft Copilot in Business Central](https://docs.microsoft.com/dynamics365/business-central/copilot-overview)
- [Azure OpenAI Service](https://azure.microsoft.com/products/ai-services/openai-service)
- [Responsible AI at Microsoft](https://www.microsoft.com/ai/responsible-ai)

---

**Note**: Copilot features are powered by Azure OpenAI and are subject to Microsoft's AI services terms and conditions.

© 2025 bydynamics B.V. All rights reserved.
