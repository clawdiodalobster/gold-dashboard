# 🦞 Gold Trading Dashboard

Professional gold trading dashboard with live charts and news feed.

## Features

- **Live TradingView Chart** - Full XAU/USD chart with technical indicators
- **Real-time Price Ticker** - Current spot gold price with % change
- **News Feed** - Latest gold market news and updates
- **Dark Theme** - Professional trading interface
- **Responsive** - Works on desktop and tablet

## Quick Start

1. Open `index.html` in your browser
2. That's it! Dashboard is ready to use.

## Adding Real News API (Optional)

For live news updates, get a free API key from:

### NewsAPI (Recommended)
1. Sign up at https://newsapi.org (free tier: 100 requests/day)
2. Get your API key
3. Update line ~160 in index.html:

```javascript
const response = await fetch('https://newsapi.org/v2/everything?q=gold+OR+xauusd+OR+precious+metals&sortBy=publishedAt&apiKey=YOUR_API_KEY_HERE');
const data = await response.json();
const articles = data.articles.slice(0, 10);
```

### Alternative News Sources
- **Alpha Vantage** - https://www.alphavantage.co (free)
- **Finnhub** - https://finnhub.io (free tier)
- **Polygon.io** - https://polygon.io (limited free)

## Price Data API

Currently using demo mode. For production:

1. **Metal Price API** - https://metalpriceapi.com (free tier available)
2. **Metals-API** - https://metals-api.com (paid)
3. **Twelve Data** - https://twelvedata.com (free tier)

## Deployment

### GitHub Pages (Free Hosting)
```bash
cd gold-dashboard
git init
git add .
git commit -m "Initial dashboard"
git remote add origin https://github.com/clawdiodalobster/gold-dashboard.git
git push -u origin main
```

Then enable GitHub Pages in repo settings.

### Local Server
```bash
python3 -m http.server 8000
# Visit: http://localhost:8000
```

## Customization

- **Change Symbol**: Edit `symbol: "OANDA:XAUUSD"` in the TradingView widget
- **Chart Interval**: Modify `interval: "15"` (1, 5, 15, 60, D, W, M)
- **Theme**: Switch to light theme with `theme: "light"`
- **Indicators**: Add/remove studies in the `studies` array

## Next Steps

- Add WebSocket connection for real-time price updates
- Implement price alerts
- Add technical indicator overlays
- Create watchlist for related assets (silver, platinum, mining stocks)
- Add historical performance charts

---

Built by Clawdio 🦞 | Mat's Lobster Assistant
