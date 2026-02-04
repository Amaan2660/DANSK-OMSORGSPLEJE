# 📄 Faktura Processor - Dansk Omsorgspleje

En streamlined webapplikation til at filtrere Excel-data og generere PDF-fakturaer for Dansk Omsorgspleje ApS.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 🎯 Funktioner

- **Drag & Drop** Excel fil upload (.xlsx, .xls)
- **Automatisk filtrering** - Fjerner "Akut vikar" rækker, beholder kun "Dansk Omsorgspleje"
- **PDF generering** - Professionelle fakturaer i standardformat
- **Automatisk takstberegning**:
  - Ufaglært: 175 kr/time
  - Assistent: 220 kr/time
  - Hjælper: 200 kr/time
  - +35 kr tillæg for aften/nat vagter (15:00-07:00)
  - +40 kr tillæg for weekend
- **Live statistik** - Se total rækker, filtrerede rækker og timer
- **Responsiv design** - Virker på desktop, tablet og mobil

## 🚀 Kom i gang

### Lokal brug

1. Download `index.html` filen
2. Åben filen i din browser (Chrome, Firefox, Edge, Safari)
3. Færdig! Ingen installation nødvendig.

### GitHub Pages Deployment

1. Fork eller clone dette repository
2. Gå til **Settings** → **Pages**
3. Under "Source", vælg **main** branch
4. Klik **Save**
5. Din side vil være tilgængelig på: `https://[dit-brugernavn].github.io/[repo-navn]/`

## 📖 Brugervejledning

### Trin 1: Indtast Fakturanummer
Indtast det ønskede fakturanummer (f.eks. "164")

### Trin 2: Upload Excel Fil
- Træk din Excel fil ind i upload-området, ELLER
- Klik på området for at vælge en fil fra din computer

### Trin 3: Generer PDF
- Systemet filtrerer automatisk dataen
- Klik på "Generer PDF Faktura"
- PDF'en downloades til din computer

## 📊 Excel Format

Applikationen forventer følgende kolonner i Excel-filen:

| Kolonne | Beskrivelse |
|---------|-------------|
| Dato | Vagtdato |
| Medarbejder | Medarbejdernavn |
| Starttid | Vagtstartidspunkt |
| Sluttid | Vagtsluttidspunkt |
| Timer | Antal timer |
| Afdeling | **Vigtig**: "Dansk Omsorgspleje" eller "Akut vikar" |
| Personalegruppe | ufaglært/assistent/hjælper |
| Jobfunktion | Beskrivelse af job/lokation |

## 📄 PDF Output

Genererede fakturaer indeholder:

**Fra:**
- MR Rekruttering
- Valbygårdsvej 1, 4. th, 2500 Valby
- CVR.nr. 45090965

**Til:**
- DANSK OMSORGSPLEJE APS
- CVR: 42092630
- Frederiksborgvej 14, st, 3200 Helsinge

**Detaljer:**
- Komplet vagtliste med dato, medarbejder, tidsperiode, timer
- Automatisk beregnet takst og total pr. linje
- Subtotal, moms (25%) og total inkl. moms
- Bankoplysninger: Finseta | IBAN: GB79TCCL04140404627601

## 🛠️ Teknologi Stack

- **Frontend**: Vanilla HTML5, CSS3, JavaScript (ES6+)
- **Excel Processing**: SheetJS (xlsx.js)
- **PDF Generation**: jsPDF + jsPDF-AutoTable
- **Styling**: Custom CSS med IBM Plex Sans & JetBrains Mono fonts
- **Deployment**: GitHub Pages ready

## 🎨 Design Features

- Moderne, professionelt design
- Glatte animationer og overgange
- Responsive layout (desktop → mobil)
- Drag & drop funktionalitet
- Real-time feedback og statusmeldinger
- Tilgængelighedsvenlig

## 📝 Eksempel Flow

```
1. Bruger uploader Schedule_stats.xlsx
2. Systemet læser 117 rækker
3. Filtrerer til 45 rækker (kun "Dansk Omsorgspleje")
4. Beregner takster baseret på personaletype og tid
5. Genererer PDF med alle detaljer
6. PDF downloades som "Faktura_164_Dansk_Omsorgspleje.pdf"
```

## 🔒 Privatliv & Sikkerhed

- **100% client-side** - Ingen data sendes til servere
- Alle filer behandles lokalt i din browser
- Ingen cookies eller tracking
- Open source - inspicér koden selv

## 🤝 Bidrag

Bidrag er velkomne! 

1. Fork projektet
2. Opret en feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit dine ændringer (`git commit -m 'Add some AmazingFeature'`)
4. Push til branch (`git push origin feature/AmazingFeature`)
5. Åben en Pull Request

## 📜 Licens

Dette projekt er licenseret under MIT License - se [LICENSE](LICENSE) filen for detaljer.

## 💡 Support

Har du spørgsmål eller problemer?

- 🐛 [Rapportér en bug](../../issues)
- 💬 [Stil et spørgsmål](../../discussions)
- 📧 Kontakt via GitHub

## 🙏 Anerkendelser

- [SheetJS](https://sheetjs.com/) - Excel fil behandling
- [jsPDF](https://github.com/parallax/jsPDF) - PDF generering
- [IBM Plex](https://github.com/IBM/plex) - Typography
- [JetBrains Mono](https://www.jetbrains.com/lp/mono/) - Monospace font

---

**Lavet med ❤️ for Dansk Omsorgspleje ApS**
