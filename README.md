# ETS4IRAN

Stand with the people of Iran for freedom.

## Structure

```
index.html          Main page (all sections)
styles.css          All styles
script.js           Animations + bilingual content (EN/FR)
assets/images/      All images (PNG, descriptively named for easy replacement)
```

## Editing Content

All text lives in `script.js` inside the `i18n` object. Each string has an `en` and `fr` version.

```js
const i18n = {
  en: { heroTitle1: "Stand With The People of", ... },
  fr: { heroTitle1: "Soutenez le Peuple", ... }
};
```

To change any text: find its key (e.g. `heroTitle1`), update both `en` and `fr` values.

## Editing Stats / Numbers

- **Death toll**: change `DEATH_TOLL` constant at the top of `script.js` — updates everywhere automatically
- **Stat card text**: search `revStat` keys in the `i18n` object
- **Bar chart values**: in `index.html`, each `.chart-row-bar` has `data-width` (percentage) and the label inside `<span>`

## Social & External Links

All links are centralized in the `LINKS` object at the top of `script.js`:

```js
const LINKS = {
  telegram: '...',       // Telegram group
  twitter: '...',        // X/Twitter share intent
  facebook: '...',       // Facebook share
  source: '...',         // Human rights report
  polishRefugees: '...', // USHMM source
  executions1988: '...', // HRW source
  bloodyNovember: '...', // HRW source
  ps752: '...',          // Gov of Canada
  mahsaAmini: '...',     // Amnesty International
  rev2025Hrw: '...',     // HRW — 2025 revolution
  rev2025Amnesty: '...', // Amnesty — 2025 revolution
  blackout: '...',       // Amnesty — internet blackout
  detention: '...',      // Amnesty — mass arrests
};
```

In HTML, links use `data-link="keyName"` and are resolved from this object on page load. Change any URL in one place and it applies everywhere.

## Replacing Images

Images in `assets/images/` are named descriptively — just replace the file keeping the same name:

```
hero-night-protests.png         Hero background
hero-freedom-sign.png           Hero gallery
hero-speak-about-iran.png       Hero gallery
wlf-protester-barricade.png     Hero gallery
persepolis-ruins.png            Iran & Its People
iran-landmarks-collage.png      Landmarks grid
polish-refugees-iran-1942.png   Hospitality story
protesters-facing-police.png    Regime section
shah-visiting-montreal.png      Diaspora section
shah-montreal-dinner.png        Diaspora section
canada-quebec-iran-shamrock.png Diaspora section
womens-protest-1979.png         Timeline — 1979
student-movement-1999.png       Timeline — 1999
green-movement-march.png        Timeline — 2009
protester-tear-gas-2017.png     Timeline — 2017
bloody-november-2019.png        Timeline — 2019
ps752-memorial.png              Timeline — 2020
woman-life-freedom-highway.png  Timeline — 2022
mahsa-amini-tribute.png         Timeline — 2022
revolution-flag-statue.png      Timeline — 2025
revolution-night-crowd.png      Revolution background
qr-code.png                     Call to action
```

To add a new image, drop it in `assets/images/` and reference it in `index.html`.

## Running Locally

Open `index.html` in a browser. No build step needed.
