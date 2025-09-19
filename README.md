# Lead Enrichment Data Lakehouse

## Overview
This is an N8N automation (adapted from a client project working with a Data Lakehouse company) that automates lead enrichment by extracting LinkedIn engagement data and processing it through Clay's data enrichment platform.

## What It Does
- Extracts LinkedIn post engagement data (comments, reactions, profile info)
- Extracts those leads with contact information
- Transforms and enriches lead data through Clay
- Drafts a personalized outreach note with Instantly
- Automates data flow from LinkedIn → Apify → n8n → Clay → Sales Pipeline

## Workflows Included
- **LinkedIn to Clay Enrichment**: Main workflow for lead processing
- **PhantomBuster Integration**: Alternative LinkedIn scraping solutions
- **Clay to Instantly**: Downstream integration for sales outreach

## Architecture
```
LinkedIn → Data Extraction → n8n Processing → Clay Enrichment → Sales Tools
```
