# Kodhuset AB – Umbraco-webbplats

## Stilmallen (Sass)

Stilmallen skrivs i Sass i mappen `Styles/` och kompileras till CSS.

| Vad | Kommando / fil |
| --- | --- |
| Installera verktygen | `npm install` |
| Kompilera (komprimerad, för publicering) | `npm run bygg` |
| Kompilera automatiskt när du sparar | `npm run sass` (avsluta med Ctrl+C) |
| Filen som sidan läser | `wwwroot/css/site.css` |

Använd Node-version: **v24.15.0** (npm 11.12.1). Sass-version: **Dart Sass 1.105.1**.

> Ändra aldrig `wwwroot/css/site.css` för hand – den skrivs över varje gång du kompilerar. Ändra i `Styles/` i stället.

### Filer i `Styles/`

- `_variabler.scss` – alla färger, typsnitt och mått. Byt färg här.
- `_mixins.scss` – återanvändbara delar: `mobil`, `liten`, `versaler`, `knapp` och `linje`.
- `_bas.scss` – grundstil, sidhuvud, meny, brödsmulor, sidfot och fokusmarkering.
- `_komponenter.scss` – hero, knappar, kort, taggar, projektsida och sektionsromber.
- `main.scss` – sätter ihop allt.

### Färger och kontrast (mot vit bakgrund, krav 4.5:1)

| Variabel | Färg | Kontrast |
| --- | --- | --- |
| `$text` | `#2b2b33` | 14.04:1 |
| `$text-dampad` | `#6e6e7a` | 5.03:1 |
| `$primar` | `#d63a44` | 4.62:1 (vit text på knappen: 4.62:1) |
| `$hero-bakgrund` | `#6e5a5c` | vit text: 6.4:1 |

`$primar-ljus` (`#f6b5b9`) används bara till linjer och ramar, aldrig till text.

## Starta webbplatsen

```bash
dotnet run
```

Backoffice: `/umbraco`
