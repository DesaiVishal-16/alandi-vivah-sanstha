# Technical Documentation: Alandi Vivah Sanstha

## 1. Project Overview
**Alandi Vivah Sanstha** is a matrimonial website designed to facilitate wedding planning and matchmaking. This codebase represents a **static export** of a WordPress website. The site is built to be fast, secure, and easy to host on any static hosting provider (e.g., GitHub Pages, Netlify, Vercel, or standard Apache/Nginx servers).

**Production URL**: [courtmarriagealandi.com](https://courtmarriagealandi.com)

## 2. Technology Stack
The project utilizes the following technologies:

*   **Core**: HTML5, CSS3, JavaScript
*   **Origin CMS**: WordPress (v6.8.3)
*   **Theme**: [Astra](https://wpastra.com/) (v4.11.13)
*   **Page Builder**: [Elementor](https://elementor.com/) (v3.32.4)
*   **Static Site Generator**: Likely generated using a plugin like *Simply Static*, *Make Me Static*, or *Staatic* (all present in plugins directory).

## 3. File Structure
The codebase follows a standard static site structure that mirrors a WordPress installation:

```
/
├── index.html          # Homepage
├── blogs/              # Blog section
│   ├── index.html      # Blog listing page
│   └── post1/          # Individual blog post
├── wp-content/         # Static assets from WordPress
│   ├── plugins/        # Plugin assets (CSS/JS)
│   ├── themes/         # Theme assets (CSS/JS/Fonts)
│   └── uploads/        # Media files (Images, Videos)
└── wp-includes/        # Core WordPress assets (jQuery, Emojis, etc.)
```

## 4. Key Components

### 4.1. Plugins
The site relies on several key WordPress plugins, whose static assets are included:
*   **Elementor**: Used for page layout and design.
*   **Astra Sites**: Starter templates for the Astra theme.
*   **Rank Math SEO**: Handles SEO metadata (Open Graph, Twitter Cards, Schema.org).
*   **WPForms Lite**: Contact forms (Note: Static forms may require external handling like Formspree if not configured for static submission).
*   **WP WhatsApp**: WhatsApp chat integration.
*   **Really Simple SSL**: SSL configuration (assets).
*   **Image Optimization**: Tools for optimizing images.

### 4.2. Metadata & SEO
The `index.html` file is heavily optimized for SEO using Rank Math:
*   **Open Graph (OG)** tags for social media sharing (Facebook, LinkedIn).
*   **Twitter Card** tags for Twitter previews.
*   **Schema.org** JSON-LD markup for structured data (Organization, WebSite, WebPage).
*   **Canonical URLs** to prevent duplicate content issues.

### 4.3. Styling
Styling is handled through a combination of:
*   **Global Styles**: `global-styles-inline-css` defines CSS variables for colors, fonts, and spacing.
*   **Theme Styles**: `astra-theme-css` provides the base styling from the Astra theme.
*   **Elementor Styles**: `elementor-frontend-css` and inline styles manage the layout and design of specific page elements.
*   **Fonts**: Google Fonts (Kirang Haerang, Brygada 1918, Roboto) are loaded via `astra-google-fonts-css`.

## 5. Maintenance & Deployment

### 5.1. Updates
Since this is a static export, you **cannot** edit the content (text, images, layout) directly in these HTML files efficiently.
*   **To make changes**: You must edit the original WordPress site.
*   **To publish changes**: Re-export the site using your static site generator plugin and replace the files in this repository.

### 5.2. Deployment
This site can be deployed to any static hosting service.
*   **Entry Point**: `index.html`
*   **Requirements**: None (no database or PHP required).
