# Poplatkový agent – sop2.cendai.cz

AI agent pro výpočet soudních poplatků u Městského soudu v Praze.

## Co aplikace dělá

1. Uživatel nahraje žalobu ve formátu PDF
2. Agent (Claude AI) vytěží účastníky řízení a spisovou značku
3. Vypočte soudní poplatek dle zákonného sazebníku
4. Při zjištěném nedoplatku automaticky vygeneruje výzvu k doplacení (.docx)

## Technický stack

- **Backend:** Node.js (vanilla, bez závislostí)
- **Frontend:** Single-page HTML s JSZip (CDN)
- **AI:** Anthropic Claude API

## Nasazení (Railway)

Aplikace je připravena pro nasazení na [Railway](https://railway.app).

### Požadované proměnné prostředí

| Proměnná | Popis |
|---|---|
| `ANTHROPIC_API_KEY` | API klíč pro Anthropic Claude |
| `PORT` | Port serveru (Railway nastavuje automaticky) |

### Postup

1. Vytvořte nový projekt na Railway
2. Napojte tento repozitář
3. Nastavte proměnnou `ANTHROPIC_API_KEY`
4. Nasměrujte custom doménu `sop2.cendai.cz` na Railway service

## Lokální spuštění

```bash
ANTHROPIC_API_KEY=your_key node server.js
```

Aplikace poté běží na http://localhost:3000
