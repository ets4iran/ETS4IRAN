# ETS4IRAN

Stand with the people of Iran for freedom.

## Structure

```
index.html          Main page (all sections)
styles.css          All styles
script.js           Animations + bilingual content (EN/FR)
assets/images/      All images (PNG)
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

- **Death toll counter**: search `43000` in `script.js` (appears in `initCounter` calls)
- **Stat card text**: search `revStat` keys in the `i18n` object
- **Bar chart values**: in `index.html`, each `.chart-row-bar` has `data-width` (percentage) and the label inside `<span>`

## Adding / Replacing Images

Drop images into `assets/images/`, then update the `src` in `index.html`.

## Telegram / Social Links

- Telegram link: search `t.me` in `index.html`
- Twitter/Facebook share text: search `updateShareLinks` in `script.js`

## Running Locally

Open `index.html` in a browser. No build step needed.
