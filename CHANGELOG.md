# Changelog

### Page Manager addon **[WHMCS](https://puqcloud.com/link.php?id=77)**
#####  [Order now](https://puqcloud.com/store/whmcs-addon-modules) | [Download](https://download.puqcloud.com/WHMCS/addons/PUQ_WHMCS-Page-Manager/) | [FAQ](https://community.puqcloud.com/)

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
