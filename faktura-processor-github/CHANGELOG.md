# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-02-04

### Added
- Initial release of Faktura Processor
- Drag & drop Excel file upload functionality
- Automatic filtering of "Dansk Omsorgspleje" rows
- PDF invoice generation with jsPDF
- Automatic rate calculation based on personnel type
- Evening/night shift bonus (+35 kr)
- Weekend shift bonus (+40 kr)
- Real-time statistics display (total rows, filtered rows, hours)
- Responsive design for mobile and desktop
- Danish localization
- Professional invoice layout matching MR Rekruttering format
- Bank details: Finseta | IBAN: GB79TCCL04140404627601

### Features
- **Personnel Types Supported:**
  - Ufaglært: 175 kr/hour base rate
  - Assistent: 220 kr/hour base rate
  - Hjælper: 200 kr/hour base rate

- **Invoice Details:**
  - From: MR Rekruttering (CVR 45090965)
  - To: DANSK OMSORGSPLEJE APS (CVR 42092630)
  - Automatic calculation of subtotal, VAT (25%), and total
  - Comprehensive shift details table

### Technical
- 100% client-side processing (no server required)
- Vanilla JavaScript (no frameworks)
- CDN-hosted libraries (SheetJS, jsPDF)
- IBM Plex Sans & JetBrains Mono fonts
- GitHub Pages ready

---

## [Unreleased]

### Planned Features
- Multiple invoice templates
- CSV export option
- Save/load invoice numbers
- Custom rate configuration
- Multi-language support (English)
- Print preview before PDF generation
- Batch processing of multiple Excel files

---

**Legend:**
- `Added` for new features
- `Changed` for changes in existing functionality
- `Deprecated` for soon-to-be removed features
- `Removed` for now removed features
- `Fixed` for any bug fixes
- `Security` for vulnerability fixes
