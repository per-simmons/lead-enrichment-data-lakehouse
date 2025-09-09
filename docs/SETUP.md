# Setup Guide

## Prerequisites

1. **n8n Installation**
   - Cloud: Sign up at [n8n.io](https://n8n.io)
   - Self-hosted: Follow [installation guide](https://docs.n8n.io/hosting/)

2. **Apify Account**
   - Create account at [apify.com](https://apify.com)
   - Subscribe to LinkedIn Post Comments scraper
   - Generate API token

3. **Clay Account**
   - Set up workspace
   - Create webhook table
   - Configure column mappings

## Configuration Steps

### 1. Import Workflow
```bash
# In n8n UI:
1. Go to Workflows
2. Click "Import from File"
3. Select linkedin-enrichment-workflow.json
```

### 2. Configure Credentials

#### Apify Credentials:
1. In n8n, go to Credentials
2. Create new "Apify OAuth2 API" credential
3. Add your API token

#### Clay Webhook:
1. In Clay, create new table
2. Add webhook source
3. Copy webhook URL
4. Update in n8n workflow

### 3. Set Target Posts
Update the LinkedIn post URLs in the Apify actor configuration:
```json
{
  "posts": [
    "your-linkedin-post-url-here"
  ],
  "maxItems": 100
}
```

### 4. Test Execution
1. Click "Execute Workflow"
2. Check execution logs
3. Verify data in Clay table

## Field Mappings

| Apify Field | Clay Column | Description |
|-------------|-------------|-------------|
| actor.name | fullName | Commenter's full name |
| actor.position | title | Job title |
| actor.linkedinUrl | linkedinUrl | Profile URL |
| commentary | commentText | Comment content |
| createdAt | commentCreatedAt | Timestamp |

## Troubleshooting

### Common Issues

1. **Authentication Error**
   - Verify API credentials
   - Check token expiration

2. **No Data Returned**
   - Confirm post URL is public
   - Check Apify actor limits

3. **Clay Webhook Failed**
   - Verify webhook URL
   - Check Clay table configuration

### Support Resources
- n8n Documentation: https://docs.n8n.io
- Apify Documentation: https://docs.apify.com
- Clay Help Center: https://clay.com/help