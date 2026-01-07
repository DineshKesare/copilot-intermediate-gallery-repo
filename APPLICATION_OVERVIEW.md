# Application Overview

## About This Application

Photo Gallery & Portfolio is a professional photo management and showcase application built with Next.js 15, TypeScript, and Tailwind CSS. It serves as both a learning resource for GitHub Copilot features and a fully functional photo gallery application with portfolio management capabilities.

---

## Application Features

### 1. **Home Page - Professional Landing**
- **Hero Section**: Eye-catching introduction with title and description
- **Feature Cards**: Highlights three main capabilities:
  - Smart Photo Organization
  - Client Proofing
  - Automatic Optimization
- **Quick Upload**: Drag-and-drop file upload zone directly from homepage
- **Recent Uploads Preview**: Shows the 6 most recent photos with a "View All" link

### 2. **Gallery Page - Browse & Filter**
- **Advanced Search**: Real-time photo search functionality
- **Filter System**: 
  - Tag-based filtering with multi-select checkboxes
  - Visual tag counter showing active filters
  - Clear all filters option
  - Dropdown filter interface
- **View Options**: Toggle between grid and list views
- **Load More**: Pagination with "Load More" button for browsing additional photos
- **Responsive Grid**: Automatically adjusts photo grid based on screen size

### 3. **Upload Page - Photo Management**
- **Drag & Drop Upload**: Interactive upload zone with real-time file preview
- **Upload Settings**:
  - Gallery assignment (Wedding, Corporate, Nature, Street Photography)
  - Visibility controls (Public, Private, Client Review, Draft)
  - Tag management with comma-separated input
  - Copyright notice configuration
- **Upload Features Section**: Cards explaining:
  - Automatic Optimization
  - Client Sharing capabilities
  - Public Portfolio options
- **Action Buttons**: Upload & Process or Save as Draft

### 4. **Admin Dashboard - Management Hub**
- **Statistics Overview**: Visual stats grid showing:
  - Total Photos count
  - Active Galleries count
  - Total Views count
  - Client Accounts count
- **Quick Actions**:
  - Upload Photos shortcut
  - Manage Clients interface
  - Settings configuration
- **Galleries Management Table**: Comprehensive table view with:
  - Gallery name, type, and status
  - Photo count and view statistics
  - Last updated timestamps
  - Action buttons (View, Edit, Delete)

### 5. **UI Component System**
- **Reusable Components**: Consistent design across all pages
  - Hero sections for page headers
  - Section containers with background variants
  - Section titles with optional "View All" links
  - Feature cards for highlighting capabilities
  - Stats grid for displaying metrics
- **Responsive Design**: Mobile-first approach with breakpoints
- **Dark Mode Support**: Full dark/light theme support
- **Animations**: Framer Motion for smooth transitions

### 6. **Developer Features**
- **Mock Data System**: Development-ready with sample data
- **TypeScript Integration**: Type-safe component props and data structures
- **Component Library**: Pre-built UI components for rapid development
- **Copilot Demos**: Interactive tutorials for learning GitHub Copilot

---

## Important Folders & Their Purposes

### `/src` - Source Code Root
Main application source code directory containing all TypeScript/React components and utilities.

### `/src/app` - Next.js 15 App Router Pages
Contains all application pages using Next.js App Router architecture:
- **`page.tsx`** - Homepage with hero, features, and quick upload
- **`layout.tsx`** - Root layout with navigation header and metadata
- **`globals.css`** - Global styles and Tailwind configuration
- **`/gallery`** - Gallery page with search and filter functionality
- **`/upload`** - Photo upload page with settings
- **`/admin`** - Admin dashboard with management tools
- **`favicon.ico`** - Application favicon

**Purpose**: Defines the application's route structure and page-level components.

### `/src/components` - Reusable React Components
Organized component library following atomic design principles:

#### `/src/components/ui` - Core UI Components
Foundation-level components used across the entire application:
- **`/layout`** - Layout components (Hero, SectionContainer, SectionTitle)
- **`/cards`** - Card components (FeatureCard)
- **`/stats`** - Statistics display components (StatsGrid)
- **`index.ts`** - Central export file for easy imports

**Purpose**: Provides consistent, reusable UI building blocks.

#### `/src/components/gallery` - Gallery-Specific Components
- **`GalleryGrid.tsx`** - Photo grid with filtering, search, and pagination

**Purpose**: Handles photo display and gallery-specific functionality.

#### `/src/components/upload` - Upload-Specific Components
- **`UploadZone.tsx`** - Drag-and-drop file upload with preview

**Purpose**: Manages file upload interface and interactions.

### `/src/lib` - Utility Functions & Mock Data
Contains helper functions and development data:
- **`mock-photo-data.ts`** - Sample photo data with tags, likes, views
- **`mock-admin-data.ts`** - Dashboard statistics and gallery data
- **`mock-feature-card-data.ts`** - Feature card content
- **`mock-tag-data.ts`** - Available tags for filtering

**Purpose**: Provides mock data for development and testing, plus utility functions.

### `/demos` - GitHub Copilot Learning Materials
Comprehensive tutorial guides for GitHub Copilot features:
- **`README.md`** - Overview of all available demos
- **`features-demo.md`** - Core Copilot features walkthrough
- **`engineering-practices.md`** - Professional Copilot tools and workflows
- **`customize-copilot.md`** - Advanced customization techniques
- **`copilot-spaces.md`** - Collaborative Copilot Spaces guide
- **`coding-agent.md`** - GitHub Copilot coding agent demo

**Purpose**: Educational resources for learning GitHub Copilot capabilities in a real-world project.

### `/public` - Static Assets
Public files served directly by Next.js:
- SVG icons and images
- Static resources accessible at root URL path

**Purpose**: Hosts static files like icons, images, and other assets.

### `/.devcontainer` - Development Container Configuration
Settings for GitHub Codespaces and VS Code Dev Containers:
- Container configuration
- Automatic dependency installation
- Pre-configured extensions

**Purpose**: Enables consistent development environment setup.

### `/.github` - GitHub Configuration
GitHub-specific configurations:
- **`/agents`** - Custom agent configurations
- Workflow files and repository settings

**Purpose**: Manages CI/CD, automation, and GitHub-specific features.

### Configuration Files (Root Level)
- **`package.json`** - Project dependencies and scripts
- **`tsconfig.json`** - TypeScript compiler configuration
- **`next.config.ts`** - Next.js framework settings
- **`tailwind.config.js`** - Tailwind CSS customization
- **`postcss.config.mjs`** - PostCSS processing configuration
- **`eslint.config.mjs`** - Code linting rules
- **`.gitignore`** - Git ignore patterns
- **`README.md`** - Quick start guide and project setup
- **`COMPONENT_USAGE_GUIDE.md`** - Component usage examples
- **`LICENSE`** - Project license information

**Purpose**: Configure build tools, linters, and framework settings.

---

## Technology Stack

- **Framework**: Next.js 15 (React 19)
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 4
- **UI Components**: Radix UI primitives
- **Icons**: Lucide React
- **Animations**: Framer Motion
- **File Upload**: React Dropzone
- **Image Processing**: Sharp

---

## Project Architecture

### Component-Driven Design
The application follows a modular, component-driven architecture where:
1. **UI components** are small, focused, and reusable
2. **Page components** compose UI components into full pages
3. **Mock data** provides realistic development data
4. **TypeScript interfaces** ensure type safety

### Data Flow
1. Mock data stored in `/src/lib`
2. Components import and use mock data
3. State management via React hooks
4. Props passed down component tree

### Styling Approach
1. Tailwind utility classes for styling
2. Global styles in `globals.css`
3. Dark mode support via Tailwind dark: prefix
4. Responsive design with mobile-first breakpoints

---

## Getting Started

### Prerequisites
- Node.js v18 or newer
- npm, yarn, pnpm, or bun

### Quick Start
```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Run production server
npm start

# Lint code
npm run lint
```

### Using GitHub Codespaces
1. Click "Code" button on GitHub
2. Select "Codespaces" tab
3. Click "Create codespace on main"
4. Environment automatically configured

---

## Development Workflow

1. **Explore**: Review existing components and pages
2. **Learn**: Follow demo guides in `/demos` folder
3. **Build**: Create new features using component library
4. **Test**: Use mock data for development
5. **Style**: Apply Tailwind classes consistently
6. **Document**: Update guides for new features

---

## Key Features for Developers

### Reusable Component Library
Import and use pre-built components:
```tsx
import { Hero, SectionContainer, SectionTitle, FeatureCard } from "@/components/ui";
```

### Type Safety
All components have TypeScript interfaces:
```tsx
interface Photo {
  id: string;
  url: string;
  title: string;
  tags: string[];
  likes: number;
  downloads: number;
  views: number;
}
```

### Mock Data Pattern
Easy development with realistic data:
```tsx
import { mockPhotos } from "@/lib/mock-photo-data";
```

### Consistent Styling
Use predefined CSS classes:
- `page-gradient` - Page background
- `card-base` - Card styling
- `btn-primary` - Primary button
- `nav-link` - Navigation links

---

## Learning Resources

This repository is designed for learning GitHub Copilot:
- Start with `/demos/features-demo.md`
- Progress through demos in order
- Practice with real components
- Build new features with Copilot assistance

---

## Contributing

When adding new features:
1. Follow existing component patterns
2. Use TypeScript interfaces
3. Maintain responsive design
4. Support dark mode
5. Update documentation
6. Add mock data if needed

---

## License

See LICENSE file for details.
