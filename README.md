# Nexus relay

Small Node relay used by the Nexus panel and app.

- `GET /health`   liveness
- `GET /status`   load (active/total streams)
- `GET /proxy?url=`  stream/JSON proxy (public, used by the app)
- `GET /stalker?portal=...&mac=...`  Stalker channel list (panel only)

Environment: `PORT`, `AUTH_TOKEN` (optional), `RELAY_KEY` (optional:
when set, `/stalker` requires the `x-relay-key` header).

Deploy: Render free (`render.yaml`) or any Node 18+ host.
