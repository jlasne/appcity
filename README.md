# App City

**One tower per app. The city grows as founders move in.**

🌃 [appcity.jeremylasne.com](https://appcity.jeremylasne.com)

A pixel skyline at night where every building is a real app, drawn from its
real RevenueCat numbers. No ranking table, no dashboard. You just look at the
city and know who is doing well.

## How to read it

| You see | It means |
|---|---|
| A tall tower | High MRR. The tallest one fills the screen |
| A wide tower | Many active users |
| Lit windows | Subscribers. The paying share of the people inside |
| Dark floors on top | Subscribers lost in the last 30 days |
| A crane on the roof | The app grew this week |
| A crowd at the door | Free trials, one person per ten |
| The sign colour | Revenue tier: white, cyan at $25k, amber at $250k, gold at $1M |
| A `?` on the sign | The founder kept the app private |

Downtown is the middle: rank one stands in the centre, the rest fan out on
both sides. Scroll sideways to walk the street. Click a tower for its card.

## Add your app

1. In RevenueCat, make a V2 API key with only **Charts metrics** set to Read.
2. Press **Add your app**, paste the key and your project ID.
3. Your browser reads six numbers, the tower breaks ground on the spot.

The numbers refresh every day at 04:00 UTC. Thirty days of history build up,
so the chart and the churn floors appear from the second day.

**Privacy.** The key can read six aggregate numbers and nothing else: no
customers, no emails, no purchases. It is used once in your browser, then
kept server-side for the daily refresh, and is never shown to anyone. You can
hide your name, your app, or both.

## Under the hood

- One HTML file, no build step, no dependencies. Canvas 2D, integer-scaled
  pixel art, baked once and blitted every frame at 60 fps.
- Towers live in a small Convex table. The page talks to it through one
  endpoint. If the server is unreachable, your tower stays in your browser.
- Hosted on GitHub Pages from `main`.

Made with fun by [@jeremylasne](https://x.com/jeremylasne).
