# QueryNest
Redash-inspired SQL analytics MVP. Demo SQLite dataset, query runner, charts, and saved queries.

## Local
Node.js 20+. Run `npm install`, `npm --prefix server install`, `npm --prefix client install`, then `npm run dev`. UI: http://localhost:5173, API: http://localhost:4000/api. Demo credentials demo@querynest.dev / demo.

## Docker
Run `docker compose up --build`.

MIT licensed. This starter is demo-only; production deployments need security hardening and real connector support.

## Browser edition on theanalyst.in

The standalone browser application lives in `web/index.html` and is published at [https://theanalyst.in/querynest/](https://theanalyst.in/querynest/). It is a separate QueryNest implementation (not the SQL Playground page). It uses SQL.js, a real SQLite engine compiled to WebAssembly, and runs the demo database and imported CSV/SQLite files in the visitor's browser. Saved queries and dashboards are stored in that browser.

The GitHub Pages edition does not run the Express server. Its browser-local workspace does not provide multi-user authentication, shared server dashboards, central storage, or remote datasource connections. The Node/Express + better-sqlite3 API scaffold remains in `server/` for a separate server-hosted deployment.
