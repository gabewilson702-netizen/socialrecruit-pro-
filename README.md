# SocialRecruit - AI-Generated Social Recruiting Content

A Next.js 15 application that generates AI-powered social media recruiting content for LinkedIn, Instagram, Facebook, and TikTok.

## Features

✅ **Landing Page** - Modern, conversion-optimized landing page with pricing and testimonials
✅ **AI Generator Form** - 5-question form to collect company information
✅ **Content Dashboard** - View and manage generated content
✅ **Multi-Platform Posting** - Platform-specific content management for LinkedIn, Instagram, Facebook, and TikTok
✅ **Responsive Design** - Mobile-first design with Tailwind CSS v4

## Tech Stack

- **Framework**: Next.js 15 with TypeScript
- **Styling**: Tailwind CSS v4
- **UI Components**: shadcn/ui
- **Icons**: Lucide React
- **Database**: Supabase (ready for integration)

## Getting Started

### Prerequisites

- Node.js 18+ 
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone <your-repo-url>
cd talentsocial-pro
```

2. Install dependencies
```bash
npm install
```

3. Set up environment variables
Create a `.env.local` file in the root directory:
```env
# Supabase Configuration
NEXT_PUBLIC_SUPABASE_URL=your_supabase_url_here
NEXT_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key_here

# OpenAI Configuration
OPENAI_API_KEY=your_openai_api_key_here

# App Configuration
NEXT_PUBLIC_APP_URL=http://localhost:3000
```

4. Run the development server
```bash
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser

## Project Structure

```
src/
├── app/
│   ├── generator/          # AI generator form page
│   ├── dashboard/          # Content dashboard
│   ├── globals.css         # Global styles
│   ├── layout.tsx          # Root layout
│   └── page.tsx            # Landing page
├── components/
│   ├── ui/                 # shadcn/ui components
│   ├── AIGeneratorForm.tsx # 5-question form
│   └── PlatformPosting.tsx # Multi-platform posting interface
└── lib/
    └── utils.ts            # Utility functions
```

## Features Overview

### 1. Landing Page (`/`)
- Hero section with clear value proposition
- How it works (3-step process)
- Content preview examples
- Pricing plans ($149/month and $299/month)
- Customer testimonials
- Call-to-action buttons

### 2. AI Generator (`/generator`)
- 5-question form collecting:
  - Company website
  - Careers page
  - Social media handles
  - Role being hired for
  - Top 3 requirements
- Progress indicator
- Form validation
- Success state with redirect to dashboard

### 3. Content Dashboard (`/dashboard`)
- **Overview Tab**: Content grid with platform filtering
- **Platform Posting Tab**: Multi-platform content management
- Statistics cards (total posts, scheduled, engagement, applications)
- Platform-specific content previews
- Copy, download, and schedule actions

### 4. Multi-Platform Posting
- Platform-specific tabs (LinkedIn, Instagram, TikTok, Facebook)
- Content preview with media placeholders
- Copy to clipboard functionality
- Download assets (placeholder)
- Schedule posts (placeholder)
- Platform-specific styling and icons

## Next Steps for Production

### 1. Database Integration
- Set up Supabase project
- Create tables for users, content, and analytics
- Implement user authentication
- Add data persistence for generated content

### 2. AI Integration
- Integrate OpenAI API for content generation
- Add image generation (DALL-E or similar)
- Implement video generation for TikTok
- Add content personalization based on company data

### 3. Social Media APIs
- Integrate LinkedIn API for posting
- Add Instagram Basic Display API
- Implement TikTok for Business API
- Add Facebook Graph API

### 4. Additional Features
- Email notifications
- Content scheduling
- Analytics and reporting
- User management
- Payment processing (Stripe)

## Deployment

### Vercel (Recommended)
1. Push code to GitHub
2. Connect repository to Vercel
3. Add environment variables in Vercel dashboard
4. Deploy automatically

### Manual Deployment
```bash
npm run build
npm start
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is proprietary software. All rights reserved.

## Support

For support or questions, please contact the development team.



