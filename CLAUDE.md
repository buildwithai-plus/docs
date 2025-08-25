# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Mintlify documentation repository** for the BuildWithAI React Native/Expo boilerplate. The docs provide comprehensive setup and configuration guides for a production-ready mobile app boilerplate with AI features, authentication, in-app purchases, and monetization capabilities.

## Development Commands

### Documentation Development
```bash
# Install Mintlify CLI globally
npm i -g mint

# Start local development server
mint dev

# Update CLI to latest version
mint update
```

### Key Requirements
- Run `mint dev` in the folder containing `docs.json` (the docs/ directory)
- Documentation auto-deploys to production when pushed to main branch
- Use Mintlify web editor or local editing with CLI preview

## Architecture & Structure

### Documentation Structure
- **docs.json** - Main Mintlify configuration file defining navigation, theme, and structure
- **index.mdx** - Homepage with overview and quick action cards
- **quickstart/** - Step-by-step setup guides (Node.js, Git, Windsurf, Expo account, project setup)
- **features/** - Feature-specific documentation organized by category:
  - Authentication (social, Google, Apple)
  - In-app purchases (Android/iOS setup, RevenueCat, Superwall)
  - Styling and theming
  - Analytics (PostHog)
  - Internationalization
  - AdMob monetization
  - MCP server integration

### Navigation Groups
1. **Setting Up Your App** - Initial setup and MCP configuration
2. **Customising Your App** - Styling, auth, analytics, i18n
3. **Optional Features** - Authentication, analytics, error tracking, push notifications
4. **Monetizating Your App** - In-app purchases and advertising

### Key Features
- **MCP Integration** - Model Context Protocol server for accessing docs through Cursor/Windsurf
- **Multi-platform Setup** - Comprehensive Android and iOS configuration guides
- **Monetization Focus** - Detailed guides for RevenueCat, Superwall, and AdMob integration
- **Developer Experience** - IDE-specific setup guides (Windsurf recommended)

## Content Guidelines

### File Naming
- Use kebab-case for MDX files
- Organize features in logical subdirectories
- Place images in `/images/` directory

### Documentation Style
- Use Mintlify components: `<Card>`, `<Steps>`, `<Tabs>`, `<Warning>`, `<Info>`, `<Tip>`
- Include frontmatter with title, description, and icon
- Provide step-by-step guides with clear prerequisites
- Include screenshots and visual aids where helpful

### Boilerplate Context
- Primary target: React Native/Expo mobile applications
- Tech stack: TypeScript, Supabase, TailwindCSS/NativeWind
- Monetization: RevenueCat + Superwall for subscriptions, AdMob for ads
- Authentication: Social login (Google, Apple), email/password
- Development environment: Windsurf IDE recommended

## Important Notes

- **No build process required** - Mintlify handles compilation
- **Live reload** - Changes appear immediately with `mint dev`
- **Production deployment** - Automatic via GitHub integration to main branch
- **MCP server integration** - Allows docs access directly from supported IDEs
- **TASKS.md** contains pending documentation updates
- **Contextual actions** - docs.json configured with copy, ChatGPT, Claude, Perplexity, MCP, and Cursor options

## Troubleshooting

- If dev environment isn't running: Run `mint update` to get latest CLI version
- Page loads as 404: Ensure running in folder with `docs.json`
- Missing navigation: Check `docs.json` navigation structure matches file organization