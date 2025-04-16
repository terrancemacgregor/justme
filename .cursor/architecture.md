# Home Website Architecture Rules

## Core Framework
- Next.js 14+ (App Router)
- Tailwind CSS for styling
- Radix UI for functionality
- shadcn/ui for components

## Required Dependencies
```json
{
  "dependencies": {
    "@aws-sdk/client-s3": "^3.x",
    "@prisma/client": "^5.x",
    "@radix-ui/react-icons": "^1.x",
    "@radix-ui/themes": "^2.x",
    "contentlayer": "^0.3.x",
    "gray-matter": "^4.x",
    "next": "14.x",
    "next-auth": "^4.x",
    "next-contentlayer": "^0.3.x",
    "nodemailer": "^6.x",
    "react": "18.x",
    "react-dom": "18.x",
    "react-email": "^1.x"
  },
  "devDependencies": {
    "@types/node": "^20.x",
    "@types/react": "^18.x",
    "autoprefixer": "^10.x",
    "postcss": "^8.x",
    "prisma": "^5.x",
    "tailwindcss": "^3.x",
    "typescript": "^5.x"
  }
}
```

## Project Structure
```
├── Dockerfile
├── docker-compose.yml
├── src/
│   ├── app/
│   │   ├── admin/
│   │   │   └── [...adminRoutes]
│   │   ├── blog/
│   │   └── api/
│   ├── components/
│   │   ├── ui/
│   │   └── admin/
│   ├── lib/
│   │   ├── auth/
│   │   ├── email/
│   │   └── backup/
│   ├── content/
│   │   └── posts/
│   └── styles/
├── prisma/
│   └── schema.prisma
└── public/
```

## Key Features
1. Content Management
   - MDX for blog posts
   - Contentlayer for type-safe content
   - Git-based version control

2. Backup System
   - Daily automated backups to S3
   - Database and content file backups
   - Version control for content recovery

3. Email Notifications
   - Post publication alerts
   - Backup confirmations
   - System alerts
   - React Email templates

4. Security Requirements
   - Environment variables for sensitive data
   - Rate limiting on API routes
   - CORS configuration
   - CSP headers
   - Regular security updates

## Docker Configuration
```dockerfile
FROM node:20-alpine AS base
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run build
EXPOSE 3000
CMD ["npm", "start"]
```

## AWS Configuration
- Credentials location: ~/.aws/
- Default PEM key: ~/.ssh/20121029_TerranceMacGregor.pem

## Content Update Guidelines
1. Admin Interface
   - shadcn/ui components
   - WYSIWYG editor (TipTap)
   - Image upload to S3
   - Preview functionality

2. Backup Process
   - Daily automated backups
   - Database dumps
   - Content files
   - Uploaded media
   - S3 versioning
   - Email notifications

## Development Environment
- OS: macOS Sequoia 15.2
- Architecture: Apple Silicon (M4)
- Shell: /bin/zsh 