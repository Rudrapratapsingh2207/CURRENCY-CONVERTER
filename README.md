# Currency Converter 💱

A simple, live currency converter built with vanilla HTML, CSS, and JavaScript. Enter an amount, pick your currencies, and get a real exchange rate — no frameworks, no backend.

## Demo

Try it live: [currency-converter](https://rudrapratapsingh2207.github.io/CURRENCY-CONVERTER/)

## Features

- Convert between 150+ world currencies
- Real-time exchange rates pulled from a live API
- Country flags for each currency, updated automatically on selection
- Swap button to instantly flip "From" and "To" currencies
- Input validation (blocks empty, negative, or non-numeric amounts)
- Visual loading state while fetching the rate
- Tactile, "pressed" button styling

## Tech Stack

- **HTML** — page structure
- **CSS** — styling and layout
- **JavaScript** — API calls, DOM updates, and conversion logic
- **[Currency API](https://github.com/fawazahmed0/currency-api)** — free, no-key exchange rate data

## Project Structure

```
.
├── index.html      # Page markup
├── sty.css         # Styling
├── script.js       # Conversion logic, flag updates, API calls
└── codes.js        # Currency-code → country-code mapping (for flags)
```

## Getting Started

No build tools or installs required — it's a static site.

1. Clone the repo
   ```bash
   git clone https://github.com/Rudrapratapsingh2207/CURRENCY-CONVERTER.git
   ```
2. Open `index.html` in your browser

That's it — you're converting.

## How It Works

- `codes.js` maps each currency code (e.g. `INR`) to its country code (e.g. `IN`) so the right flag can be shown
- `script.js` populates both dropdowns from that list, syncs the flag image on change, and swaps currencies on the ⇄ icon
- On clicking **Get Exchange Rate**, it fetches the base currency's full rate table from the API and pulls out the rate for the target currency
- The result is calculated, rounded to 2 decimal places, and displayed

## Deploying

Since this is a static site, GitHub Pages works great:

1. Push your code to GitHub
2. Go to **Settings → Pages**
3. Under **Source**, select the `main` branch
4. Your converter will be live at `https://your-username.github.io/CURRENCY-CONVERTER/`

## License

Feel free to use, modify, and share this project.
