# Frequently Asked Questions (FAQ)

## Role Control for Business Central

### General Questions

#### What is Role Control?

Role Control is a Business Central extension that allows you to create and customize Role Centers without writing code. You can configure tiles, filters, and layouts to match your business processes.

#### Which Business Central versions are supported?

Role Control requires Business Central version 26.0 or higher and works with Business Central Online (SaaS). Copilot features are available in all Online environments.

#### Where can I get Role Control?

Role Control is exclusively available on Microsoft AppSource. Search for "Role Control" by bydynamics in the AppSource marketplace within Business Central or visit [Microsoft AppSource](https://appsource.microsoft.com).

#### How much does it cost?

Pricing is available on our AppSource listing. Click on the app in AppSource to see current pricing, or contact sales@bydynamics.com for enterprise licensing options.

---

## Installation & Setup

#### How do I install Role Control?

1. Open Business Central
2. Search for **Extension Management** or **AppSource**
3. Search for "Role Control" by bydynamics
4. Click **Get it now** or **Install**
5. Accept the permissions and terms
6. Wait for installation to complete (usually 2-5 minutes)

#### Do I need special permissions to use Role Control?

Yes, you need:
- **Setup permissions** to create Role Centers and tiles (typically administrators)
- **User permissions** to view and use assigned Role Centers (all users)

The extension includes permission sets: `Rco - Premium Data` for full access.

#### Can I use Role Control in a sandbox environment?

Yes! We strongly recommend testing in a sandbox before deploying to production. The same AppSource installation works for both sandbox and production environments.

#### Can I try Role Control before purchasing?

Check the AppSource listing for trial availability. Many AppSource apps offer a free trial period. Contact sales@bydynamics.com for evaluation options.

---

## Role Centers

#### How many Role Centers can I create?

There's no limit. You can create as many custom Role Centers as needed for different user roles or departments.

#### Can I modify existing BC Role Centers?

No, you cannot modify Microsoft's standard Role Centers directly. However, you can create new Role Centers that replicate and extend standard ones.

#### How do I assign a Role Center to users?

1. Go to **Dynamic Role Center Access**
2. Create a new entry
3. Select **Type**: Profile or User
4. Enter the **Profile ID** or **User Name**
5. Select your **Role Center Code**

Users will see the assigned Role Center when they log in (if their profile matches).

#### Can a user have multiple Role Centers?

Users can only have one active Role Center at a time, but administrators can assign multiple Role Centers to different profiles, and users can switch between profiles.

---

## Tiles

#### What data sources can tiles use?

Tiles can connect to any Business Central table, including:
- Standard BC tables (Customer, Sales Order, Item, etc.)
- Tables from other extensions (if installed)
- Custom tables from your own extensions

#### What calculation types are supported?

- **Count**: Number of records
- **Sum**: Total of a numeric field
- **Min**: Minimum value of a field
- **Max**: Maximum value of a field
- **Average**: Average value of a field

#### Why is my tile showing zero?

Common reasons:
1. **Filters are too restrictive** - Check your filter configuration
2. **No data matches** - Verify data exists in the source table
3. **Permission issues** - Ensure users have read access to the table
4. **Field ID incorrect** - Verify the Result Field ID is valid

#### Can tiles refresh automatically?

Yes, tiles refresh when:
- The Role Center page is opened
- You manually refresh the page (F5)
- The user switches between Role Center groups

#### How do I improve tile performance on large tables?

Use **Optimization Keys**:
1. Edit the tile configuration
2. Click **Lookup Optimization Key**
3. Select an appropriate table key
4. Ensure your Result Field is part of the key

This dramatically improves Min/Max/Average calculations on large datasets.

---

## Filters

#### What types of filters are available?

1. **Fixed filters** - Static values (e.g., `Status = 'Open'`)
2. **My Filter References** - User-specific dynamic filters
3. **Calculated filters** - Computed from other table/field values

#### How do date filters work?

Use Business Central date formulas:
- `WORKDATE` - Today's date
- `WORKDATE-30D` - 30 days ago
- `WORKDATE..WORKDATE+7D` - Next 7 days
- `<WORKDATE` - Before today
- `>=WORKDATE-1M` - Last month onwards

#### Can users create their own filters?

Yes! Users can create **My Tile Filters** in the Role Center to personalize their view without affecting others.

#### What are Default Role Center Tile Filters?

These are predefined filter options that administrators set up. Users can copy these to their personal filters as starting points.

---

## Copilot Features

#### Is Copilot required to use Role Control?

No, Copilot is an optional feature. You can create Role Centers manually without using AI.

#### Why can't I see the Copilot feature?

Copilot requires:
- ✅ Business Central Online (which Role Control requires)
- ✅ BC version 26.0+
- ✅ Copilot features enabled in environment settings
- ✅ Active Azure OpenAI connection (configured by bydynamics)

Check **Copilot & AI Capabilities** in Business Central to ensure it's enabled.

#### Does Copilot access my business data?

**No.** Copilot only receives:
- Your natural language prompt
- BC table/field schema (structure, not data)
- Your BC version number

Your actual business records (customers, orders, amounts) are never sent to Azure OpenAI.

#### Can I use Copilot in multiple languages?

Copilot currently works best with English prompts. Other languages may produce suboptimal results.

#### How accurate is Copilot?

Copilot generates suggestions based on standard Business Central tables. Results are typically good for common business scenarios but may require manual adjustment for:
- Custom tables
- Complex filtering requirements
- Industry-specific terminology

Always review and test generated configurations before deploying to production users.

---

## Troubleshooting

#### Error: "You do not have permission to read the table"

**Solution:**
1. Check that you have the `Rco - Premium Data` permission set assigned
2. Verify you have read access to the source table
3. Contact your administrator to grant necessary permissions

#### Tiles are not calculating correctly

**Check:**
1. **Table ID** - Is it correct?
2. **Result Field ID** - Does the field exist and is it numeric (for Sum/Min/Max/Average)?
3. **Filters** - Are they preventing data from showing?
4. **Permissions** - Do you have read access?

#### Drill-down does nothing when clicking a tile

**Possible causes:**
1. **Drill-Down Action** set to "None"
2. **Object ID** is 0 or invalid
3. **Page permissions** - User lacks access to the drill-down page

**Solution:** Edit the tile and verify drill-down configuration.

#### Role Center is not showing for my users

**Check:**
1. **Dynamic Role Center Access** - Is the user/profile assigned?
2. **Profile settings** - Is the user using the correct profile?
3. **Role Center page ID** - Verify the Role Center is properly configured
4. **Permissions** - Does the user have access to the Role Center page?

#### Copilot generation failed

**Try:**
1. Simplify your prompt
2. Use Business Central terminology
3. Check internet connection
4. Wait a moment and try again
5. Use a template prompt as a starting point

#### Installation failed from AppSource

**Steps:**
1. Check you have permission to install extensions
2. Verify your BC environment is Online (not On-Premises)
3. Check BC version is 26.0 or higher
4. Try again after a few minutes
5. Contact Microsoft support if the issue persists

---

## Data & Privacy

#### What data does Role Control collect?

We collect anonymous telemetry:
- Performance metrics (calculation times)
- Feature usage statistics
- Error logs

We do NOT collect:
- Your business data
- Personal information
- User names or credentials

See our [Privacy Statement](../PRIVACY.md) for full details.

#### Is Role Control GDPR compliant?

Yes. Role Control complies with GDPR requirements:
- Transparent data collection
- No personal data in telemetry
- Copilot prompts not retained
- User rights respected

#### Can I disable telemetry?

Telemetry is currently integrated into the app. Contact us if you have specific concerns about data collection.

---

## Licensing & Support

#### How does AppSource licensing work?

Role Control is licensed through Microsoft AppSource subscriptions:
- Billed through your Microsoft/Azure account
- Monthly or annual subscription options
- Per-user or per-environment pricing (see AppSource listing)

#### What happens when my subscription expires?

When your subscription expires:
- Role Control stops functioning
- Users cannot access custom Role Centers
- Configuration data is preserved (not deleted)
- Renewing your subscription restores full functionality

#### Can I use Role Control in multiple environments?

Licensing depends on your subscription type. Check the AppSource listing for multi-environment options or contact us for enterprise licensing.

#### How do I cancel my subscription?

1. Go to **Extension Management** in Business Central
2. Find Role Control
3. Click **Uninstall** or manage through your Microsoft/Azure billing portal
4. Your subscription will cancel at the end of the current billing period

#### How do I get support?

- **GitHub Issues**: [Report bugs](https://github.com/bydynamics/AL-RoleControl-Support/issues)
- **Documentation**: [GitHub Repository](https://github.com/bydynamics/AL-RoleControl-Support)
- **AppSource**: Leave a review or question on our AppSource listing

---

## Updates & Versions

#### How do I update Role Control?

Updates are delivered automatically through AppSource:
1. Microsoft notifies you of available updates
2. Updates are applied during scheduled maintenance windows
3. You can also manually update through **Extension Management**

#### Will updates break my existing configurations?

No. We maintain backward compatibility. Your Role Centers, tiles, and filters are preserved during updates.

#### How often are updates released?

- **Bug fixes**: As needed
- **Minor updates**: Monthly
- **Major updates**: Quarterly

Check our [GitHub Releases](https://github.com/bydynamics/AL-RoleControl-AppSource/releases) for update history.

---

## Advanced Topics

#### Can I create tiles that execute custom code?

In a future release when using **Custom Functions**:
1. Set Drill-Down Action to "RunCustomFunction"
2. Configure your custom codeunit logic in `RcoCustomTileFunctions.Codeunit.al`
3. This requires AL development knowledge and access to extend the app

#### Can Role Control integrate with other extensions?

Yes! Role Control can:
- Read data from tables in other AppSource extensions (if installed)
- Be extended through events and extensibility points
- Coexist with other Role Center customizations

#### Can I export/import Role Center configurations?

Currently, there's no built-in export/import feature. Configuration is stored in BC tables and can be backed up through standard BC backup procedures.

Contact us if you need bulk migration assistance.

#### Is Role Control available for On-Premises?

No, Role Control is exclusively for Business Central Online (SaaS) and is only available through Microsoft AppSource.

---

## Still Have Questions?

**Contact us:**
- Email: support@bydynamics.com
- Website: www.bydynamics.com
- GitHub: [AL-RoleControl-AppSource](https://github.com/bydynamics/AL-RoleControl-Support)
- AppSource: [Leave a question on our listing](https://appsource.microsoft.com)

---

*Last updated: January 6, 2025*

© 2025 bydynamics B.V. All rights reserved.
