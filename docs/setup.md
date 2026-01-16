# Setup Guide

## Overview
This project has been initialized with Next.js 16 and Supabase using the official `with-supabase` example template from Vercel.

## What Was Installed

### Framework & Core
- **Next.js 16.1.2** - React framework with App Router
- **React 19.0.0** - UI library
- **TypeScript 5.x** - Type safety

### Supabase Integration
- **@supabase/supabase-js** - Supabase client library
- **@supabase/ssr** - Server-side rendering support for Supabase Auth

### UI Components
- **Tailwind CSS 3.4.x** - Utility-first CSS framework
- **shadcn/ui components** - Pre-built accessible components
- **Radix UI** - Headless UI primitives
- **next-themes** - Theme switching (dark/light mode)

### Features Included
1. ✅ Authentication pages (login, sign-up, password reset)
2. ✅ Protected routes
3. ✅ Theme switching (dark/light mode)
4. ✅ Responsive design with Tailwind CSS
5. ✅ TypeScript configuration
6. ✅ ESLint setup

## Directory Structure

```
/home/runner/work/Jubby/Jubby/
├── app/                      # Next.js App Router pages
│   ├── auth/                # Authentication pages
│   ├── protected/           # Protected pages
│   ├── layout.tsx           # Root layout
│   └── page.tsx             # Home page
├── components/              # React components
│   ├── ui/                  # shadcn/ui components
│   └── tutorial/            # Tutorial components
├── lib/                     # Library code
│   └── supabase/           # Supabase client setup
├── docs/                    # Documentation
├── .env.example             # Environment variables template
├── package.json             # Dependencies
└── README.md               # Project documentation
```

## Getting Started

### 1. Set Up Environment Variables

Copy the example environment file:
```bash
cp .env.example .env.local
```

Then update `.env.local` with your Supabase credentials:
```
NEXT_PUBLIC_SUPABASE_URL=your-project-url
NEXT_PUBLIC_SUPABASE_PUBLISHABLE_KEY=your-publishable-or-anon-key
```

You can find these values in your Supabase project settings:
https://app.supabase.com/project/_/settings/api

### 2. Install Dependencies

Dependencies are already installed, but you can reinstall them with:
```bash
npm install
```

### 3. Run Development Server

```bash
npm run dev
```

The app will be available at http://localhost:3000

### 4. Build for Production

```bash
npm run build
npm start
```

### 5. Lint Code

```bash
npm run lint
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## Supabase Setup

To use the authentication features, you need to:

1. Create a Supabase project at https://supabase.com
2. Set up authentication in your Supabase dashboard
3. Add your Supabase URL and anon key to `.env.local`
4. Configure authentication redirect URLs in Supabase settings

## Known Issues

- **Google Fonts**: The build may fail to fetch Google Fonts (Geist font) if running in a restricted network environment. This is used in `app/layout.tsx` and can be replaced with local fonts or alternative font providers if needed.

## Next Steps

1. Configure your Supabase project
2. Customize the authentication flow
3. Add your application-specific pages and features
4. Update the README with project-specific information
5. Deploy to Vercel or your preferred hosting platform

## Resources

- [Next.js Documentation](https://nextjs.org/docs)
- [Supabase Documentation](https://supabase.com/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [shadcn/ui Documentation](https://ui.shadcn.com)
