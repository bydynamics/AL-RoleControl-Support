# Role Control for Business Central

**Take control of your Business Central Role Centers with dynamic configuration and AI-powered assistance.**

[![Version](https://img.shields.io/badge/version-26.0.0.0-blue.svg)](https://github.com/bydynamics/AL-RoleControl-AppSource)
[![Business Central](https://img.shields.io/badge/Business%20Central-26.0-green.svg)](https://docs.microsoft.com/en-us/dynamics365/business-central/)
[![License](https://img.shields.io/badge/license-MIT-orange.svg)](LICENSE)

## Overview

Role Control is a powerful Business Central extension that enables you to create and customize Role Centers without writing code. Configure tiles, filters, and layouts to match your business processes and user needs.

## Key Features

### 🎯 Dynamic Role Centers
- Create unlimited custom Role Centers
- Configure tiles with real-time data
- Organize tiles in multiple groups (up to 3 groups per Role Center)
- Assign Role Centers to specific profiles or users

### 📊 Flexible Tile Configuration
- **Data Sources**: Connect tiles to any Business Central table
- **Calculation Types**: Count, Sum, Min, Max, Average
- **Drill-Down Actions**: Open pages, run reports, execute codeunits, or open URLs
- **Visual Styles**: Configure color-coded thresholds (Favorable, Ambiguous, Unfavorable)
- **Filters**: Fixed filters, user-specific filters, or filterset references
- **Performance Optimization**: Define optimization keys for faster calculations on large datasets

### 🔍 Advanced Filtering
- Create personal tile filters per user
- Define default Role Center filters
- Use filter references for dynamic data
- Support for date formulas (WORKDATE, relative dates)
- Location filters, customer filters, and custom filter references

### 🤖 AI-Powered Role Center Generation (Copilot)
Generate complete Role Centers with AI assistance. [Learn more about Copilot features](COPILOT.md)

### 🌍 Multilingual Support
Available in:
- English (EN)
- Dutch (NL)
- German (DE)
- Spanish (ES)
- French (FR)

## Installation

1. Install from **Microsoft AppSource**
2. Open Business Central
3. Search for "Role Control" in the extension marketplace
4. Click **Install**

## Quick Start

### Creating Your First Role Center

1. Search for **"Dynamic Role Centers"** in Business Central
2. Click **New** to create a Role Center
3. Fill in:
   - **Code**: Unique identifier (e.g., "SALES-MGR")
   - **Description**: Display name
   - **Group Descriptions**: Names for your tile groups
4. Click **Configure Tiles** to add tiles

### Adding Tiles

1. From the Role Center card, click **Tiles**
2. Click **New** and configure:
   - **Tile Code**: Select from predefined tiles or create new
   - **Description**: Tile caption
   - **Activity Cue Group**: Which group to display in (Group 1, 2, or 3)
   - **Sequence**: Display order
3. Configure drill-down action (what happens when clicking the tile)
4. Set visual thresholds for color indicators

### Assigning Role Centers

1. Open **Dynamic Role Center Access**
2. Click **New**
3. Select:
   - **Type**: User or Profile
   - **Code**: Specific user or profile ID
   - **Role Center Code**: Your custom Role Center

## Use Cases

### Credit Control Dashboard
Monitor overdue customer invoices with date-based tile groups:
- Group 1: Overview (all open entries with user filters)
- Group 2: Aging buckets (1-30, 31-60, 61-90, 90+ days)
- Personal filters: Filter by specific customers

### Sales Manager Role Center
Track sales performance:
- Open sales orders
- Sales invoices to ship
- Customer count by region
- Top customers by revenue

### Inventory Management
Monitor stock levels:
- Items below reorder point
- Inventory by location
- Pending purchase orders
- Recent stock adjustments

## Features in Detail

### Optimization Keys
For large datasets, define optimization keys to improve performance:
- Used for Min/Max calculations
- Leverages table indexes for faster queries
- Automatically validates if result field is included in key

### Tile Filter Types
- **Fixed**: Static filter value
- **MyFilterReference**: User-specific dynamic filters
- **Calculated**: Compute filter from other table/field

### Drill-Down Actions
- **RunObject**: Open page or report
- **RunCustomFunction**: Execute custom codeunit logic
- **OpenURL**: Open external websites

### Telemetry
Built-in Application Insights integration for monitoring:
- Tile calculation performance
- Drill-down usage
- Configuration events
- Error tracking

## Documentation

- [Copilot Features](COPILOT.md)
- [Privacy Statement](PRIVACY.md)
- [End User License Agreement](EULA.md)

## Support

- **Issues**: [GitHub Issues](https://github.com/bydynamics/AL-RoleControl-Support/issues)
- **Website**: [www.bydynamics.com](https://www.bydynamics.com)

## About bydynamics

bydynamics is a Microsoft partner specializing in Business Central extensions and solutions. We help businesses optimize their ERP processes through innovative extensions and custom development.

**Visit us**: [www.bydynamics.com](https://www.bydynamics.com)

---

© 2025 bydynamics B.V. All rights reserved.
