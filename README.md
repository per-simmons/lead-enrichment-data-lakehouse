# LinkedIn Commenter Sales Enrichment Automation

## Overview
This n8n automation workflow streamlines the sales team's outbound process by extracting LinkedIn post engagement data and enriching leads through Clay's data platform.

## Workflow Components

### 1. LinkedIn Engagement Extraction
- Scrapes comments and reactions from LinkedIn posts
- Captures commenter profiles including name, title, company, and LinkedIn URL
- Processes engagement types (comments vs reactions)

### 2. Data Transformation
- Transforms raw LinkedIn data into structured format
- Maps fields for Clay enrichment pipeline
- Includes metadata for engagement scoring

### 3. Clay Integration
- Sends formatted data to Clay webhook endpoint
- Enables further enrichment and lead scoring
- Integrates with downstream sales tools

## Setup Instructions

1. **Prerequisites**
   - n8n instance (self-hosted or cloud)
   - Apify account with LinkedIn scraper access
   - Clay workspace with webhook configured

2. **Configuration**
   - Import the workflow JSON into n8n
   - Configure Apify credentials
   - Update Clay webhook URL
   - Set target LinkedIn post URLs

3. **Execution**
   - Trigger manually or schedule via cron
   - Monitor execution in n8n dashboard
   - Check Clay table for enriched leads

## Architecture
```
LinkedIn Post → Apify Scraper → n8n Transform → Clay Webhook → Sales Pipeline
```

## Use Cases
- Identify engaged prospects from thought leadership content
- Build targeted outreach lists from post interactions
- Score leads based on engagement type and frequency
- Automate top-of-funnel lead generation

## Technical Stack
- **Automation Platform**: n8n
- **Data Extraction**: Apify
- **Data Enrichment**: Clay
- **Integration**: HTTP webhooks

## Workflow Features
- Synchronous execution for real-time processing
- Error handling and retry logic
- Scalable to multiple posts
- Customizable field mapping