# System Patterns and Architecture

## System Architecture
- **Single-Page Application (SPA)**: Entire website contained in one HTML file
- **Static Site Generation**: No server-side processing or dynamic content generation
- **Client-Side Rendering**: All functionality handled by browser JavaScript
- **Asset Management**: Mix of local images and external CDN resources

## Key Technical Decisions
- **Inline Styles and Scripts**: CSS and JavaScript embedded in HTML for single-file deployment
- **CSS Custom Properties**: Centralized theming system using CSS variables
- **Mobile-First Responsive Design**: Base styles for mobile, enhanced for larger screens
- **Progressive Enhancement**: Core functionality works without JavaScript, enhanced with it
- **Semantic HTML**: Proper use of header, nav, section, footer elements for accessibility

## Design Patterns
- **Component-Based CSS**: Modular class naming convention (.hero, .menu-item, .contact-item)
- **CSS Grid and Flexbox**: Modern layout techniques for responsive designs
- **Hamburger Menu**: Mobile navigation pattern with overlay menu
- **Card Layout**: Consistent design pattern for menu items and contact information
- **Hero Section**: Large background image with centered content overlay

## Component Relationships
```
index.html
├── Header (Fixed Navigation)
│   ├── Logo
│   ├── Navigation Menu
│   └── Mobile Hamburger
├── Hero Section
│   ├── Background Image
│   ├── Headline & Tagline
│   └── Call-to-Action Button
├── About Section
│   ├── Text Content
│   └── Featured Image
├── Menu Section
│   ├── Section Title
│   └── Menu Items Grid
│       ├── Menu Item Card
│       │   ├── Image
│       │   ├── Title
│       │   ├── Description
│       │   └── Price
├── Contact Section
│   ├── Contact Information
│   │   ├── Address
│   │   ├── Hours
│   │   ├── Phone
│   │   └── Email
│   └── Embedded Map
└── Footer
    ├── Logo
    ├── Tagline
    ├── Social Links
    └── Copyright
```

## Critical Implementation Paths
- **Navigation Flow**: Header links trigger smooth scrolling to anchored sections
- **Mobile Menu**: Hamburger button toggles overlay navigation with JavaScript
- **Responsive Images**: CSS handles image scaling and positioning
- **Form Handling**: Currently informational only, no form submission implemented
- **External Dependencies**: Font Awesome icons and Google Maps embed

## Code Organization Patterns
- **CSS Structure**: Variables → Base styles → Component styles → Responsive overrides
- **JavaScript Structure**: DOM manipulation → Event handlers → Utility functions
- **Naming Convention**: BEM-like approach with descriptive class names
- **Commenting**: Section headers and functional comments for maintainability

## Performance Patterns
- **Lazy Loading**: Images load as needed (no explicit lazy loading implemented)
- **Minification**: Code could be minified for production deployment
- **Caching Strategy**: Static assets suitable for aggressive caching
- **Bundle Size**: Single file approach minimizes HTTP requests

## Maintenance Patterns
- **Content Updates**: Menu prices and business information easily editable in HTML
- **Style Modifications**: CSS variables allow theme changes without code edits
- **Feature Additions**: Modular component structure supports easy extensions
- **Testing Approach**: Manual testing across devices and browsers
