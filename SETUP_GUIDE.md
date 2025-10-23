# SocialRecruit Setup Guide

## Environment Variables Required

Create a `.env.local` file in your project root with the following variables:

```env
# App Configuration
NEXT_PUBLIC_APP_URL=http://localhost:3000
NODE_ENV=development

# Supabase Configuration
NEXT_PUBLIC_SUPABASE_URL=your_supabase_project_url
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
SUPABASE_SERVICE_ROLE_KEY=your_supabase_service_role_key

# OpenAI Configuration
OPENAI_API_KEY=your_openai_api_key

# Firecrawl Configuration (Web Scraping)
FIRECRAWL_API_KEY=your_firecrawl_api_key

# SendGrid Configuration (Email)
SENDGRID_API_KEY=your_sendgrid_api_key

# Social Media APIs (Optional - for direct posting)
LINKEDIN_CLIENT_ID=your_linkedin_client_id
LINKEDIN_CLIENT_SECRET=your_linkedin_client_secret
INSTAGRAM_ACCESS_TOKEN=your_instagram_access_token
FACEBOOK_ACCESS_TOKEN=your_facebook_access_token
TIKTOK_ACCESS_TOKEN=your_tiktok_access_token

# AI Image/Video Generation
HEYGEN_API_KEY=your_heygen_api_key
MIDJOURNEY_API_KEY=your_midjourney_api_key

# Social Media Listening & Analytics
BRANDWATCH_API_KEY=your_brandwatch_api_key
RITETAG_API_KEY=your_ritetag_api_key
```

## Step-by-Step Setup

### 1. Supabase Setup
1. Go to [supabase.com](https://supabase.com) and create a new project
2. Go to Settings > API to get your URL and keys
3. Run the SQL schema from `supabase-schema.sql` in your Supabase SQL editor
4. Add the URL and keys to your `.env.local`

### 2. OpenAI Setup
1. Go to [platform.openai.com](https://platform.openai.com)
2. Create an API key
3. Add to your `.env.local`

### 3. Firecrawl Setup
1. Go to [firecrawl.dev](https://firecrawl.dev)
2. Sign up and get your API key
3. Add to your `.env.local`

### 4. SendGrid Setup
1. Go to [sendgrid.com](https://sendgrid.com)
2. Create an account and get your API key
3. Add to your `.env.local`

### 5. Optional Integrations

#### HeyGen (Video Generation)
1. Go to [heygen.com](https://heygen.com)
2. Get your API key
3. Add to your `.env.local`

#### Midjourney (Image Generation)
1. Go to [midjourney.com](https://midjourney.com)
2. Get your API key
3. Add to your `.env.local`

#### Brandwatch (Social Media Listening)
1. Go to [brandwatch.com](https://brandwatch.com)
2. Sign up for their social listening platform
3. Get your API key
4. Add to your `.env.local`

#### Ritetag (Hashtag Analytics)
1. Go to [ritetag.com](https://ritetag.com)
2. Sign up for their hashtag analytics service
3. Get your API key
4. Add to your `.env.local`

#### Social Media APIs
- **LinkedIn**: Create a LinkedIn app at [linkedin.com/developers](https://linkedin.com/developers)
- **Instagram**: Use Instagram Basic Display API
- **Facebook**: Create a Facebook app at [developers.facebook.com](https://developers.facebook.com)
- **TikTok**: Use TikTok for Business API

## Testing the Setup

1. Start the development server:
```bash
npm run dev
```

2. Test the AI generation:
```bash
curl -X POST http://localhost:3000/api/generate-content \
  -H "Content-Type: application/json" \
  -d '{
    "companyWebsite": "https://example.com",
    "socialMedia": "@example",
    "roleTitle": "Marketing Manager",
    "requirements": "3+ years experience, Bachelor degree"
  }'
```

3. Check the logs for any errors

## Production Deployment

### Vercel Deployment
1. Push your code to GitHub
2. Connect your repository to Vercel
3. Add all environment variables in Vercel dashboard
4. Deploy!

### Environment Variables in Production
Make sure to add all the same environment variables to your production environment (Vercel, Netlify, etc.)

## Troubleshooting

### Common Issues

1. **OpenAI API errors**: Check your API key and billing
2. **Supabase connection issues**: Verify your URL and keys
3. **SendGrid not sending**: Check your API key and sender verification
4. **Firecrawl errors**: Verify your API key and quota

### Debug Mode
Set `NODE_ENV=development` to see detailed error messages in the console.

## Cost Estimates

### Monthly Costs (Approximate)
- OpenAI API: $50-200 (depending on usage)
- Firecrawl: $99/month
- SendGrid: $20/month
- Supabase: Free tier available
- **Total**: ~$170-320/month

### Revenue Break-even
- Basic Plan: $149/month
- Growth Plan: $299/month
- **Break-even**: 1-2 customers

## Support

If you encounter issues:
1. Check the console logs
2. Verify all environment variables are set
3. Test each API individually
4. Contact support if needed
