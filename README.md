# App City

One tower per app, at night. https://appcity.jeremylasne.com

A single HTML file, no build. Height is MRR, size is active users, lit
windows are subscribers, the crowd at the door is free trials, a crane means
the app grew this week.

Founders add their app with a RevenueCat V2 key limited to Charts metrics
read. The browser reads the six numbers once, then the key goes to the
server, which re-reads every tower daily at 04:00 UTC and keeps thirty days
of history. The backend is the Convex deployment in
[jeremyportfolio/overlap](https://github.com/jlasne/jeremyportfolio/tree/main/overlap/convex),
file `city.ts`.

Hosted on GitHub Pages from `main`.
