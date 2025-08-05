# 🤖 AI Services Dashboard

A comprehensive dashboard for monitoring and managing all your AI service accounts in one place. Track credit/token usage, renewal dates, pricing, and more across multiple AI providers.

## ✨ Features

### 📊 Comprehensive Monitoring
- **Multi-Provider Support**: Connect services from OpenAI, Anthropic, Google, Microsoft, Meta, Cohere, and Hugging Face
- **Real-time Usage Tracking**: Monitor token consumption, credit usage, and costs across all services
- **Visual Analytics**: Interactive charts showing usage trends and cost analysis over time
- **Smart Alerts**: Get notified when services need renewal or when usage limits are approaching

### 💳 Billing & Cost Management
- **Renewal Date Tracking**: Never miss a renewal with upcoming renewal alerts
- **Cost Breakdown**: Detailed monthly cost analysis by service and usage patterns
- **Pricing Comparison**: Compare pricing across different providers and models
- **Budget Monitoring**: Set limits and track spending across all AI services

### 🔧 Service Management
- **Easy Integration**: Simple setup process for adding new AI services
- **API Key Management**: Secure storage and management of API credentials
- **Service Toggling**: Enable/disable services as needed
- **Custom Configuration**: Flexible settings for each service including custom endpoints

### 📈 Analytics & Insights
- **Usage History**: Track token and credit usage over time with detailed historical data
- **Cost Optimization**: Identify cost-saving opportunities based on usage patterns
- **Provider Comparison**: Compare performance and costs across different AI providers
- **Usage Forecasting**: Predict future usage based on historical trends

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Set up the database
npm run db:push

# Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see your AI Services Dashboard.

## 🏗️ Project Structure

```
src/
├── app/                        # Next.js App Router pages
│   ├── api/                   # API routes
│   │   ├── ai-services/       # AI service management
│   │   ├── usage-records/     # Usage tracking
│   │   ├── analytics/         # Analytics data
│   │   └── users/             # User management
│   ├── page.tsx              # Main dashboard
│   └── layout.tsx             # Root layout
├── components/                # Reusable React components
│   ├── ui/                   # shadcn/ui components
│   ├── ai-service-card.tsx   # Individual service card
│   ├── usage-chart.tsx       # Usage analytics chart
│   └── add-service-dialog.tsx # Add new service dialog
├── hooks/                     # Custom React hooks
└── lib/                       # Utility functions and configurations
    ├── db.ts                 # Database client
    └── utils.ts              # Utility functions
```

## 🗄️ Database Schema

The application uses Prisma with SQLite for data persistence:

### Core Models
- **User**: User account information
- **AIService**: AI service configuration and settings
- **UsageRecord**: Individual usage tracking records

### Key Features
- **Credit/Token Tracking**: Monitor usage limits and remaining balances
- **Billing Information**: Track renewal dates, costs, and plan types
- **Usage Analytics**: Comprehensive usage history with metadata
- **Multi-Currency Support**: Handle different currencies for international users

## 🔌 API Endpoints

### AI Services Management
- `GET /api/ai-services` - Get all services for a user
- `POST /api/ai-services` - Add a new AI service
- `GET /api/ai-services/[id]` - Get specific service details
- `PUT /api/ai-services/[id]` - Update service configuration
- `DELETE /api/ai-services/[id]` - Remove a service

### Usage Tracking
- `GET /api/usage-records` - Get usage records with filtering
- `POST /api/usage-records` - Record new usage data

### Analytics
- `GET /api/analytics` - Get usage analytics and insights

### User Management
- `GET /api/users` - Get user information
- `POST /api/users` - Create or get user

## 🎨 Supported AI Providers

### Major Providers
- **OpenAI**: GPT-4, GPT-3.5, DALL-E 3, Whisper
- **Anthropic**: Claude 3 Opus, Claude 3 Sonnet, Claude 3 Haiku
- **Google**: Gemini Pro, Gemini Ultra, PaLM 2
- **Microsoft**: Azure OpenAI, Copilot, Bing AI

### Open Source & Specialized
- **Meta**: Llama 2, Code Llama
- **Cohere**: Command, Embed, Generate
- **Hugging Face**: Various open source models

## 📊 Dashboard Features

### Overview Section
- **Summary Cards**: Total credits, tokens, monthly costs, and active services
- **Smart Alerts**: Urgent and warning notifications for renewals
- **Quick Actions**: Add new services and access settings

### Services Tab
- **Service Cards**: Detailed view of each AI service with usage metrics
- **Progress Bars**: Visual representation of credit/token usage
- **Provider Badges**: Easy identification of service providers
- **Quick Actions**: Edit, toggle, and access service details

### Usage Analytics Tab
- **Token Usage Charts**: 30-day token consumption trends
- **Cost Analysis**: Daily cost breakdown across all services
- **Interactive Tooltips**: Detailed information on hover
- **Responsive Design**: Works seamlessly on all devices

### Billing Overview Tab
- **Upcoming Renewals**: Sorted list of services needing renewal
- **Billing Summary**: Monthly cost breakdown by service
- **Renewal Status**: Color-coded renewal warnings
- **Plan Information**: Current plan types and pricing details

## 🔧 Configuration

### Environment Variables
Create a `.env` file with the following variables:

```env
DATABASE_URL="file:./dev.db"
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="your-secret-key"
```

### Database Setup
```bash
# Generate Prisma client
npm run db:generate

# Push schema to database
npm run db:push

# View database (optional)
npm run db:studio
```

## 🚀 Production Deployment

### Build and Deploy
```bash
# Build the application
npm run build

# Start production server
npm start
```

### Environment Setup for Production
- Set up a production database (PostgreSQL recommended)
- Configure environment variables
- Set up proper authentication
- Configure monitoring and logging

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License.

## 🚀 Welcome to Z.ai Code Scaffold

A modern, production-ready web application scaffold powered by cutting-edge technologies, designed to accelerate your development with [Z.ai](https://chat.z.ai)'s AI-powered coding assistance.

## ✨ Technology Stack

This scaffold provides a robust foundation built with:

### 🎯 Core Framework
- **⚡ Next.js 15** - The React framework for production with App Router
- **📘 TypeScript 5** - Type-safe JavaScript for better developer experience
- **🎨 Tailwind CSS 4** - Utility-first CSS framework for rapid UI development

### 🧩 UI Components & Styling
- **🧩 shadcn/ui** - High-quality, accessible components built on Radix UI
- **🎯 Lucide React** - Beautiful & consistent icon library
- **🌈 Framer Motion** - Production-ready motion library for React
- **🎨 Next Themes** - Perfect dark mode in 2 lines of code

### 📋 Forms & Validation
- **🎣 React Hook Form** - Performant forms with easy validation
- **✅ Zod** - TypeScript-first schema validation

### 🔄 State Management & Data Fetching
- **🐻 Zustand** - Simple, scalable state management
- **🔄 TanStack Query** - Powerful data synchronization for React
- **🌐 Axios** - Promise-based HTTP client

### 🗄️ Database & Backend
- **🗄️ Prisma** - Next-generation Node.js and TypeScript ORM
- **🔐 NextAuth.js** - Complete open-source authentication solution

### 🎨 Advanced UI Features
- **📊 TanStack Table** - Headless UI for building tables and datagrids
- **🖱️ DND Kit** - Modern drag and drop toolkit for React
- **📊 Recharts** - Redefined chart library built with React and D3
- **🖼️ Sharp** - High performance image processing

### 🌍 Internationalization & Utilities
- **🌍 Next Intl** - Internationalization library for Next.js
- **📅 Date-fns** - Modern JavaScript date utility library
- **🪝 ReactUse** - Collection of essential React hooks for modern development

## 🎯 Why This Scaffold?

- **🏎️ Fast Development** - Pre-configured tooling and best practices
- **🎨 Beautiful UI** - Complete shadcn/ui component library with advanced interactions
- **🔒 Type Safety** - Full TypeScript configuration with Zod validation
- **📱 Responsive** - Mobile-first design principles with smooth animations
- **🗄️ Database Ready** - Prisma ORM configured for rapid backend development
- **🔐 Auth Included** - NextAuth.js for secure authentication flows
- **📊 Data Visualization** - Charts, tables, and drag-and-drop functionality
- **🌍 i18n Ready** - Multi-language support with Next Intl
- **🚀 Production Ready** - Optimized build and deployment settings
- **🤖 AI-Friendly** - Structured codebase perfect for AI assistance

## 🤖 Powered by Z.ai

This scaffold is optimized for use with [Z.ai](https://chat.z.ai) - your AI assistant for:

- **💻 Code Generation** - Generate components, pages, and features instantly
- **🎨 UI Development** - Create beautiful interfaces with AI assistance  
- **🔧 Bug Fixing** - Identify and resolve issues with intelligent suggestions
- **📝 Documentation** - Auto-generate comprehensive documentation
- **🚀 Optimization** - Performance improvements and best practices

Ready to build something amazing? Start chatting with Z.ai at [chat.z.ai](https://chat.z.ai) and experience the future of AI-powered development!

## 📁 Project Structure

```
src/
├── app/                 # Next.js App Router pages
├── components/          # Reusable React components
│   └── ui/             # shadcn/ui components
├── hooks/              # Custom React hooks
└── lib/                # Utility functions and configurations
```

## 🎨 Available Features & Components

This scaffold includes a comprehensive set of modern web development tools:

### 🧩 UI Components (shadcn/ui)
- **Layout**: Card, Separator, Aspect Ratio, Resizable Panels
- **Forms**: Input, Textarea, Select, Checkbox, Radio Group, Switch
- **Feedback**: Alert, Toast (Sonner), Progress, Skeleton
- **Navigation**: Breadcrumb, Menubar, Navigation Menu, Pagination
- **Overlay**: Dialog, Sheet, Popover, Tooltip, Hover Card
- **Data Display**: Badge, Avatar, Calendar

### 📊 Advanced Data Features
- **Tables**: Powerful data tables with sorting, filtering, pagination (TanStack Table)
- **Charts**: Beautiful visualizations with Recharts
- **Forms**: Type-safe forms with React Hook Form + Zod validation

### 🎨 Interactive Features
- **Animations**: Smooth micro-interactions with Framer Motion
- **Drag & Drop**: Modern drag-and-drop functionality with DND Kit
- **Theme Switching**: Built-in dark/light mode support

### 🔐 Backend Integration
- **Authentication**: Ready-to-use auth flows with NextAuth.js
- **Database**: Type-safe database operations with Prisma
- **API Client**: HTTP requests with Axios + TanStack Query
- **State Management**: Simple and scalable with Zustand

### 🌍 Production Features
- **Internationalization**: Multi-language support with Next Intl
- **Image Optimization**: Automatic image processing with Sharp
- **Type Safety**: End-to-end TypeScript with Zod validation
- **Essential Hooks**: 100+ useful React hooks with ReactUse for common patterns

## 🤝 Get Started with Z.ai

1. **Clone this scaffold** to jumpstart your project
2. **Visit [chat.z.ai](https://chat.z.ai)** to access your AI coding assistant
3. **Start building** with intelligent code generation and assistance
4. **Deploy with confidence** using the production-ready setup

---

Built with ❤️ for the developer community. Supercharged by [Z.ai](https://chat.z.ai) 🚀
