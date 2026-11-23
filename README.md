# 🎾 Racket Inc. – README (alleen voor mij)

Zet deze map op je computer. Open `index.html` in je browser en je ziet je site.
Zet `contract.pdf` in dezelfde map, dan werkt de "Regels"-link.

## Een spel toevoegen

1. Open `index.html` in een teksteditor (Kladblok, VS Code, …).
2. Zoek `const GAMES = [`.
3. Plak onder het laatste spel (voor `];`) een van de templates hieronder.
4. Opslaan en de pagina verversen. Klaar!

Het spel opent **in dezelfde website** (in een scherm over de pagina heen), je wordt dus nooit doorgestuurd. De bezoeker sluit het met ✕ of `Esc`.

### Template A: spel is een link of bestand (meest gebruikt)

```js
  {
    titel: "Naam van mijn spel",
    omschrijving: "Korte uitleg van het spel.",
    afbeelding: "images/mijnspel.png",   // jouw afbeelding-link of bestand
    spel: "games/mijnspel/index.html",   // jouw spel-link of bestand
    label: "Nieuw"                       // mag leeg blijven: ""
  },
```

Let op de **komma** achter `}`.

- Afbeelding: maak een map `images` naast `index.html` en zet je plaatjes erin, of gebruik een volledige link (`https://...`).
- Spel: maak een map `games` en zet elk spel in een eigen map, of gebruik een link naar je eigen gehoste spel.
- Geen afbeelding? Laat `afbeelding: ""` staan en vul `emoji: "🎯"` in.

### Template B: het hele spel zit in `index.html`

```js
  {
    titel: "Naam van mijn spel",
    omschrijving: "Korte uitleg.",
    emoji: "🎯",
    afbeelding: "",
    label: "",
    html: `<body> ...hier je volledige spel-code... </body>`
  },
```

In Template B moet `</script>` geschreven worden als `<\/script>`.

## Mapstructuur

```
racket-inc/
├── index.html
├── contract.pdf
├── README.md
├── images/      ← je afbeeldingen
└── games/       ← je spelletjes
```

## Handige tips

- **Spel laadt niet?** Sommige websites (bv. YouTube, Google) blokkeren het insluiten van hun pagina's. Je eigen spellen werken altijd.
- **Kleur aanpassen:** het kleurcirkeltje bovenin. Bezoekers kunnen dat ook; het wordt onthouden. De standaardkleur verander je bij `--accent:#7c3aed` in de CSS.
- **Online zetten (gratis):** sleep de map naar Netlify Drop, GitHub Pages of Cloudflare Pages.
- **Volgorde:** de volgorde in `GAMES` is de volgorde op de site.
- **Contract wijzigen:** vervang `contract.pdf` door een nieuwe versie met dezelfde naam.

Alle spelletjes zijn eigendom van Racket Inc.
