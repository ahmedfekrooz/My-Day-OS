# My Day OS — Phase 1 MVP

A mobile-first responsive web planner with local browser persistence.

## Run locally
For best PWA behavior, serve this folder over HTTP rather than opening `index.html` as a file:
- Python: `python -m http.server 8000`
- Open `http://localhost:8000`

You can also deploy the folder to any static HTTPS host. On supported browsers, use **Add to Home Screen / Install app**.

## Implemented in this MVP
- Responsive Today dashboard and time-block timeline
- Create/edit/delete/complete tasks
- Categories, priorities, status, estimated duration, due date
- Daily and weekly recurrence (basic recurring display)
- Overlap warnings with explicit confirmation
- Unscheduled task inbox, search, filters, sorting
- Week calendar, goals, habits, daily reflection, basic insights
- English/Arabic interface direction toggle, light/dark theme, 12/24-hour time
- Routine preferences and manual city/country prayer settings
- Prayer times fetched from AlAdhan when online, with local cache
- JSON export/import
- PWA manifest and a simple app-shell service worker

## Important MVP limitations
- Data is stored in the current browser's localStorage. It does not sync across devices, and clearing browser data can erase it. Export backups regularly.
- This is a single-user local-first prototype; no authentication, cloud database, encryption-at-rest layer, or account recovery is configured.
- Prayer times require internet for a fresh date/location. Confirm the calculation method and times with your local mosque/authority.
- Google Calendar, push notifications, natural-language parsing, actual AI planning, drag-to-reschedule, monthly view, and native mobile packaging are not implemented yet. The “Plan my day” feature is a transparent local heuristic, not an AI integration.
- Recurrence is intentionally basic in this MVP; editing a recurring series does not provide per-occurrence exceptions.
- PWA service worker requires HTTPS or localhost. Browser notification/push infrastructure is not configured.

## Next steps for Phase 2
1. Move persistence to a backend such as Supabase; add authentication and row-level security.
2. Implement Google OAuth and event-ID-based, idempotent Calendar sync.
3. Add geolocation with explicit permission, robust prayer-time settings, and notification infrastructure.
4. Add automated tests for recurrence, timezone/date boundaries, overlap detection, RTL and mobile layouts.
