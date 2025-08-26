# Professional Services Website

A modern, high-performance company website built with Astro and powered by Cosmic CMS. This website showcases professional services, team expertise, client case studies, and testimonials with a clean, business-focused design.

![App Preview](https://imgix.cosmicjs.com/0bb0aeb0-8248-11f0-8dcc-651091f6a7c0-photo-1460925895917-afdab827c52f?w=1200&h=300&fit=crop&auto=format,compress)

## Features

- **⚡ Lightning Fast** - Built with Astro for optimal performance and SEO
- **📱 Responsive Design** - Looks great on desktop, tablet, and mobile
- **🛠️ Dynamic Services** - Showcase your services with detailed descriptions and pricing
- **👥 Team Profiles** - Professional team member directory with photos and bios
- **📊 Case Studies** - Detailed project showcases with results and metrics
- **💬 Client Testimonials** - Social proof with star ratings and client photos
- **🔍 SEO Optimized** - Built-in meta tags and structured data
- **🎨 Modern UI** - Clean, professional design with Tailwind CSS

<!-- CLONE_PROJECT_BUTTON -->

## Prompts

This application was built using the following prompts to generate the content structure and code:

### Content Model Prompt

> Create a content model for a company website with services, team members, testimonials, and case studies

### Code Generation Prompt

> Set up an Astro website powered by my existing content

The app has been tailored to work with your existing Cosmic content structure and includes all the features requested above.

## Technologies Used

- **Astro** - Static site generator with modern web standards
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first CSS framework
- **Cosmic CMS** - Headless content management
- **Inter Font** - Modern, readable typography

## Getting Started

### Prerequisites

- Node.js 18+ or Bun
- A Cosmic account with your content bucket

### Installation

1. Clone this repository
2. Install dependencies:
   ```bash
   bun install
   ```

3. Create a `.env` file in the root directory:
   ```env
   COSMIC_BUCKET_SLUG=your-bucket-slug
   COSMIC_READ_KEY=your-read-key
   COSMIC_WRITE_KEY=your-write-key
   ```

4. Start the development server:
   ```bash
   bun run dev
   ```

5. Open [http://localhost:4321](http://localhost:4321) to view the website

## Cosmic SDK Examples

### Fetching Services
```typescript
import { cosmic } from '../lib/cosmic'

const services = await cosmic.objects
  .find({ type: 'services' })
  .props(['id', 'title', 'slug', 'metadata'])
  .depth(1)
```

### Getting Team Members
```typescript
const teamMembers = await cosmic.objects
  .find({ type: 'team-members' })
  .props(['id', 'title', 'slug', 'metadata'])
  .depth(1)
```

## Cosmic CMS Integration

This website connects to your Cosmic bucket and displays:

- **Services**: Professional service offerings with descriptions and pricing
- **Team Members**: Staff profiles with photos, bios, and specialties
- **Case Studies**: Project showcases with challenges, solutions, and results
- **Testimonials**: Client feedback with ratings and photos

All content is managed through your Cosmic dashboard and updates automatically on the website.

## Deployment Options

### Deploy to Vercel
1. Connect your GitHub repository to Vercel
2. Add environment variables in Vercel dashboard
3. Deploy automatically on every push

### Deploy to Netlify
1. Connect your repository to Netlify
2. Set build command: `bun run build`
3. Set publish directory: `dist`
4. Add environment variables

The website will be optimized for production with static generation and fast loading times.