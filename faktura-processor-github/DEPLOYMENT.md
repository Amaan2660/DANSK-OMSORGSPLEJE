# 🚀 GitHub Pages Deployment Guide

## Quick Start (5 minutter)

### 1. Upload til GitHub

**Via GitHub Website:**

1. Gå til [github.com](https://github.com) og log ind
2. Klik på **"+"** i øverste højre hjørne → **"New repository"**
3. Navngiv dit repository (f.eks. `faktura-processor`)
4. Vælg **Public** (nødvendigt for gratis GitHub Pages)
5. Klik **"Create repository"**
6. Klik på **"uploading an existing file"**
7. Træk alle filer fra denne mappe ind (index.html, README.md, osv.)
8. Skriv en commit message (f.eks. "Initial commit")
9. Klik **"Commit changes"**

### 2. Aktivér GitHub Pages

1. I dit repository, gå til **Settings** (tandhjul ikon)
2. Scroll ned til **"Pages"** i venstre menu
3. Under **"Source"**, vælg **"main"** branch
4. Klik **"Save"**
5. Vent 1-2 minutter
6. Din side er nu live på: `https://[dit-brugernavn].github.io/faktura-processor/`

### 3. Test Din Side

1. Åben URL'en fra trin 2.6
2. Test med en Excel fil
3. Generer en PDF
4. Færdig! 🎉

---

## Alternativ: Via Git Command Line

```bash
# 1. Gå til mappen med filerne
cd /sti/til/faktura-processor

# 2. Initialiser Git
git init

# 3. Tilføj alle filer
git add .

# 4. Commit
git commit -m "Initial commit: Faktura Processor"

# 5. Tilføj remote (erstat med dit repo)
git remote add origin https://github.com/[dit-brugernavn]/faktura-processor.git

# 6. Push til GitHub
git branch -M main
git push -u origin main
```

Derefter følg trin 2 fra Quick Start guiden ovenfor.

---

## Custom Domain (Valgfrit)

Har du dit eget domæne?

1. Gå til **Settings** → **Pages**
2. Under **"Custom domain"**, indtast dit domæne (f.eks. `faktura.ditfirma.dk`)
3. Tilføj følgende DNS records hos din domæneudbyder:

```
Type: CNAME
Name: faktura (eller subdomain du vil bruge)
Value: [dit-brugernavn].github.io
```

4. Vent på DNS propagering (5-60 minutter)
5. Aktivér **"Enforce HTTPS"** i Settings → Pages

---

## Opdater Din Side

### Via GitHub Website:

1. Gå til dit repository
2. Klik på filen du vil redigere (f.eks. `index.html`)
3. Klik på blyant-ikonet (redigér)
4. Foretag ændringer
5. Scroll ned og klik **"Commit changes"**
6. Siden opdateres automatisk efter 1-2 minutter

### Via Git:

```bash
# 1. Foretag ændringer i dine lokale filer

# 2. Stage ændringer
git add .

# 3. Commit
git commit -m "Beskrivelse af ændringer"

# 4. Push
git push
```

---

## Fejlfinding

### Siden viser ikke
- ✅ Tjek at GitHub Pages er aktiveret (Settings → Pages)
- ✅ Tjek at "main" branch er valgt
- ✅ Vent 2-5 minutter efter aktivering
- ✅ Prøv at besøge siden i inkognito mode (clear cache)

### PDF genereres ikke
- ✅ Åben browser console (F12) for at se fejl
- ✅ Tjek at din Excel fil har korrekt format
- ✅ Prøv med en anden browser

### Excel fil læses ikke
- ✅ Tjek at filen er .xlsx eller .xls format
- ✅ Tjek at "Afdeling" kolonnen eksisterer
- ✅ Tjek at der er data i filen

---

## Performance Tips

- GitHub Pages er **gratis** og **ubegrænset** trafik
- Siden loader hurtigt (alt er client-side)
- Ingen server vedligeholdelse nødvendig
- Automatisk HTTPS aktiveret

---

## Support Links

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Git Tutorial](https://www.atlassian.com/git/tutorials)
- [GitHub Desktop App](https://desktop.github.com/) - GUI alternativ til command line

---

**Held og lykke med dit deployment! 🚀**
