# Changelog

### PUQ Page Manager module **[WHMCS](https://puqcloud.com/link.php?id=77)**
##### [Order now](https://puqcloud.com/whmcs-addon-puq-page-manager.php) | [Download](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Page-Manager/) | [Community](https://community.puqcloud.com/)

## v4.0.0 — 2026-09-15

### Major Architecture & Features Upgrade

- **Universal ionCube Loader v15 Support:** Fully re-encoded using the latest ionCube 15 compiler, guaranteeing seamless execution across PHP 7.4, 8.1, 8.2, 8.3, and 8.4 environments.
- **Unencoded Hooks Architecture (v4.0.0 Standard):** Refactored `hooks.php` into an open, unencoded entrypoint delegating to `lib/puqPageManagerHooks.php` for bulletproof dynamic hook registration and error isolation across all WHMCS environments.
- **Instant Demo Content Generation (Quick Start):** Added a 1-click **Create Demo Pages** button in the Pages management area. Automatically seeds a full suite of preconfigured showcase pages (Home, About Us, Widget Gallery) with styled widget blocks, vibrant color palettes, and English placeholders for instant testing and onboarding.
- **Analytics & Page View Reset Controls:** Added per-page view count reset controls in the page editor alongside a global **Reset All Views** action on the Analytics dashboard for effortless testing and statistics maintenance.
- **Dual Ukrainian Language Pack Support:** Added full simultaneous support for both `ukranian.php` (historical WHMCS slug) and `ukrainian.php` (standard grammatical slug) to ensure seamless native localization across all WHMCS distribution setups.
- **Comprehensive Multi-language i18n Audit:** Audited and synchronized translation keys across all 25+ language files, enforcing typographic apostrophe standards (`’`) to eliminate JavaScript syntax breakage in dynamic frontend notifications.
- **Clean Admin & Widget AJAX Interception:** Fixed an issue where admin AJAX endpoints (e.g. `getDashboard`, page lists, settings) could be wrapped in WHMCS admin HTML templates, causing infinite loading spinners. Added early hook interception and strict output buffer cleansing.
- **Enhanced WHMCS 8.x & WHMCS 9+ Compatibility:** Modernized request routing and custom rewrite pipelines to ensure smooth operation on latest WHMCS releases.
- **Improved Performance & Reliability:** Optimized page lookup caching and cleaner exception handling in frontend render loops.

---

## v1.2 — 2026-07-16

### Improvements & Standardization

- **Enhanced PHP 8.1+ Compatibility:** Improved internal AJAX routing and error handling by replacing deprecated legacy termination calls with modern exception throwing, ensuring smooth execution on strict WHMCS 8.x environments.
- **Optimized License Verification:** Eliminated log bloat by skipping redundant log entries during successful local (offline) license validations, keeping your WHMCS system logs clean and focused.
- **Admin Interface Upgrade:** Redesigned the module's administrative navigation bar to match the latest PUQ Bootstrap 3 standard. Added a quick-access "Help" menu with direct links to Documentation, Website, and the Community Forum.
- **Updated Marketing Assets:** Generated high-resolution, standard-compliant cover images and marketplace banners with updated PUQ Software branding while preserving custom module iconography.

---

## v1.1 — 2026-04-27

### New Features

- **New widget: Markdown.** A4-styled document renderer with a Markdown source editor on the admin side and a printable A4 paper layout on the frontend. Includes an optional **Download as PDF** button (uses html2pdf.js), a **Disable A4 paper layout** option for plain in-page rendering, configurable paper width, and a custom PDF file name.
- **Live preview toggle in the Markdown widget.** Single-button switch between the Markdown source and the rendered preview.
- **Translatable widget labels.** `puqWidgetHelpers` now exposes the current language to widget templates via `$lang`. Added `Download as PDF` and `Generating...` translation keys (English, Russian, Ukrainian).

### Improvements

- **Editor loading indicator.** The page editor now shows a progress bar with per-step status while loading widget scripts, EditorJS core, and TinyMCE — instead of a blank screen.
- **Asset cache busting.** Widget JS and the EditorJS core are now loaded with a `?v={version}` query string, so updates take effect on the next page load without manual cache clearing.

### Fixes

- Fixed editor toolbar ("+" / settings) sometimes appearing on the wrong side because EditorJS was being initialized inside a hidden container.
- Fixed text alignment inheritance in document-style widgets (markdown content was rendered centered because of the shared background wrapper).

---

## v1.0 — 2026-02-22

First release.

### New Features

- Block widget editor powered by EditorJS with drag-and-drop block management
- Built-in widgets: Announcements, Call To Action, Contact Form, Custom Code, Domain Search, Domain TLD, Feature Grid, Hero Section, Intelligent Domain Search, Map, Mini Menu, Page Background, Product Cards, Promo Slider, Question Answer, Separator, Slider Logos, Tabs / Accordion, Team Slide, Testimonials, Text Editor TinyMCE, Timeline, Video Embed
- Multiple style variants per widget (5–11 design templates)
- Full background control per widget: background image, color, shadow, border radius
- Multilingual page support with translation status tracking
- SEO fields: OG Title, OG Description, OG Image, Keywords, Canonical URL, Meta Robots, Schema JSON-LD
- Custom CSS and JavaScript per page
- Page analytics: views, unique views, top pages, views per day chart
- Revision history with content preview and one-click restore
- Password-protected pages with customizable appearance and quick presets
- Page visibility control: all visitors, guests only, clients only, client groups
- WHMCS page rewrites: replace home page, footer, domain register, or custom URL patterns
- Import and export pages as JSON (individual or bulk)
- Parent pages and custom sort order
- Page statuses: Draft, Published, Scheduled, Archived
- WHMCS product integration: Product Cards and Domain widgets pull live pricing
- Dashboard with statistics, recent changes, top viewed pages, system info
- One-click page creation from the pages list
- License verification system with online/offline modes
- English language interface
