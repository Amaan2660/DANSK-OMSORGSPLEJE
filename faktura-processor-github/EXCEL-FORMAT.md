# Excel Format Dokumentation

## Påkrævede Kolonner

Din Excel fil skal indeholde følgende kolonner (rækkefølge er ligegyldig):

| Kolonne Navn | Type | Beskrivelse | Eksempel |
|--------------|------|-------------|----------|
| **Dato** | Dato | Vagtdato | 26.01.2026 |
| **Medarbejder** | Tekst | Medarbejdernavn | Berivan S |
| **Starttid** | Tid | Vagtstartidspunkt | 07:00:00 |
| **Sluttid** | Tid | Vagtsluttidspunkt | 13:00:00 |
| **Timer** | Nummer | Antal timer | 6 |
| **Afdeling** | Tekst | **VIGTIG**: Bruges til filtrering | Dansk Omsorgspleje |
| **Personalegruppe** | Tekst | Personaletyppe | ufaglært 2 |
| **Jobfunktion** | Tekst | Job beskrivelse/lokation | Helsinge Dag Ufaglært 2 |

## Filtrerings Logik

Applikationen **beholder** rækker hvor `Afdeling` kolonnen indeholder:
- "Dansk Omsorgspleje" (case-insensitive)

Applikationen **fjerner** rækker hvor `Afdeling` kolonnen indeholder:
- "Akut vikar"
- "Akutvikar"
- Alt andet

## Personaletype Takster

Systemet beregner automatisk takster baseret på `Personalegruppe`:

### Basis Takster:
- **ufaglært** / **ufaglært 2**: 175 kr/time
- **assistent**: 220 kr/time
- **hjælper**: 200 kr/time

### Tillæg:
- **Aften/Nat** (+35 kr): Vagter der starter kl. 15:00 eller senere, eller før kl. 07:00
- **Weekend** (+40 kr): Lørdage og søndage

### Eksempler:

```
Ufaglært, mandag kl. 07:00-15:00
= 175 kr/time (ingen tillæg)

Assistent, mandag kl. 16:00-23:00  
= 220 + 35 = 255 kr/time (aften tillæg)

Hjælper, lørdag kl. 07:00-15:00
= 200 + 40 = 240 kr/time (weekend tillæg)

Ufaglært, søndag kl. 15:00-23:00
= 175 + 35 + 40 = 250 kr/time (aften + weekend)
```

## Excel Format Tips

### ✅ DO:
- Brug standard Excel dato format (dd.mm.yyyy)
- Brug standard tid format (HH:MM:SS)
- Sørg for at alle påkrævede kolonner er udfyldt
- Brug konsistent stavning i "Afdeling" kolonnen

### ❌ DON'T:
- Lad celler være tomme i påkrævede kolonner
- Brug forskellige datoformater i samme kolonne
- Ændr kolonnenavne fra standardformatet
- Sammenlæg celler

## Eksempel Rækker

```csv
Dato,Medarbejder,Starttid,Sluttid,Timer,Afdeling,Personalegruppe,Jobfunktion
26.01.2026,Berivan S,07:00:00,13:00:00,6,Dansk Omsorgspleje,ufaglært 2,Helsinge Dag Ufaglært 2
27.01.2026,Berivan S,07:00:00,13:00:00,6,Dansk Omsorgspleje,ufaglært 2,Helsinge Dag Ufaglært 2
30.01.2026,Alper K,15:00:00,23:00:00,8,Akut vikar,Ufaglært,Kirsten Aften - Køge Kommune
```

I dette eksempel vil de første 2 rækker blive **bevaret** og den tredje række bliver **fjernet**.

## Understøttede Filformater

- ✅ `.xlsx` (Excel 2007+)
- ✅ `.xls` (Excel 97-2003)
- ❌ `.csv` (ikke understøttet direkte - konverter til .xlsx først)
- ❌ `.ods` (LibreOffice - gem som .xlsx)

## Maksimale Grænser

- **Rækker**: Ubegrænset (anbefalet < 10,000 for bedste performance)
- **Filstørrelse**: < 10 MB anbefalet
- **Kolonner**: Minimum de 8 påkrævede, maksimum ubegrænset (ekstra kolonner ignoreres)

## Fejlhåndtering

Hvis applikationen ikke kan læse din fil:

1. **Tjek kolonnenavne** - De skal matche præcist (case-insensitive)
2. **Tjek datatyper** - Datoer skal være Excel datoer, ikke tekst
3. **Fjern tomme rækker** - Særligt i bunden af filen
4. **Gem filen igen** - Nogle gange hjælper det bare at åbne og gemme
5. **Prøv en simpel version** - Fjern alle kolonner undtagen de påkrævede

---

**Har du stadig problemer?** Åben et issue på GitHub med din Excel fil vedlagt (fjern evt. personlige data først).
