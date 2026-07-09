# tt-stats — Stroom Racing TT Stats Engine viewer
Purpose: temp public viewer for all StroomHelix short-track (Trackside Topics) computed stats.
Stack: single-file static (index.html, vanilla JS + Chart.js CDN), data baked to /data/*.json from the six public.v_stats_* Supabase views (Stats Engine v1 / DR-064).
Design: Stroom Master Design System v5.0 — data-theme="dark" data-vertical="racing" (#E53935 Apex), Archivo + IBM Plex Mono, tabular-nums on numerics, glass header, glow cards, motion tokens per spec.
Deploy: `npx wrangler pages deploy . --project-name=tt-stats` (CF creds in stroom-site-build skill).
Data refresh: rerun the bake script (pull v_stats_* via service key → data/*.json) and redeploy. Views auto-recompute from published claims, so a rebake after any ingest updates everything.
Tabs: Leaders / Drivers (search + profile w/ season chart + streaks) / Track Records (progression chart) / Win Streaks / Divisions (field-size health). Global venue filter.
Owner: Kevin Striegle (kevin@stroomlabs.com).
