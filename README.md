# Lead Enrichment Data Lakehouse

## Overview
This is a client project that automates lead enrichment by extracting LinkedIn engagement data and processing it through Clay's data enrichment platform.

## What It Does
- Extracts LinkedIn post engagement data (comments, reactions, profile info)
- Transforms and enriches lead data through Clay
- Automates data flow from LinkedIn → Apify → n8n → Clay → Sales Pipeline

## Workflows Included
- **LinkedIn to Clay Enrichment**: Main workflow for lead processing
- **PhantomBuster Integration**: Alternative LinkedIn scraping solutions
- **Clay to Instantly**: Downstream integration for sales outreach

## Architecture
```
LinkedIn → Data Extraction → n8n Processing → Clay Enrichment → Sales Tools
```