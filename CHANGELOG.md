# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

## [0.4.1] - 2025-01-XX

### Changed
- **UI/UX**: Reduced main page description text size for better visibility of converter textboxes on page load
- **SEO**: Updated metadata descriptions to emphasize TOML to TOON & TONL conversion

## [0.4.0] - 2025-12-06

### Added
- **API System**: Full-featured REST API (`/api/v1/toon`) for converting data programmatically.
- **API Tester**: Interactive playground to test the API directly from the UI with code snippets for cURL, Python, and JS.
- **Documentation**: Integrated Swagger UI documentation at `/api-docs` and OpenAPI spec at `/api/doc`.
- **Privacy**: Dedicated Privacy Policy page and comprehensive privacy controls.
- **Analytics**: Integrated Ahrefs Analytics and Google Tag Manager for better insights.
- **Rate Limiting**: Robust rate limiting for the API with `X-RateLimit-Reset` headers.

### Changed
- **SEO**: Major SEO overhaul including canonical URLs, enhanced metadata, Open Graph, and Twitter Cards.
- **Performance**: Optimized API response times and added Cloudflare Worker observability.
- **Layout**: New global layout structure with improved header/footer navigation.

## [0.3.0] - 2025-12-04

### Added
- Blog section with articles about TOON format and data serialization
- Installation guides with language-specific instructions
- Open Graph, Twitter Card, and JSON-LD structured data for SEO
- Web worker for improved conversion performance

### Changed
- Offloaded conversion logic to a web worker for better UI responsiveness
- Dynamic imports for UI components to reduce initial bundle size

---

## [0.2.0] - 2025-12-02

### Added
- Character and line count display for both input and output
- Conversion time measurement
- Line length markers toggle for supported formats
- Bug report link in footer
- Changelog page
- Comprehensive documentation section with format guides

## [0.1.0] - 2025-11-30

### Added
- Convert between JSON, TOON, CSV, TOML, YAML, and XML formats
- Copy to clipboard with confetti animation
- Download converted files
- Sample data templates for quick testing
- Drag-and-drop file upload
- Dark/light theme support
- Token savings calculator
- Privacy-first design (all processing happens in your browser)
