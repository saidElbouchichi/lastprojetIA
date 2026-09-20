# StudioPro — Project Notes

## What this is
A single-file, Spotify-inspired music player (`index.html`) — no build step,
no dependencies, vanilla HTML/CSS/JS. See `README.md` for feature list,
color palette, and file structure (CSS ~lines 7–418, HTML body ~419–589,
JS ~596 on).

## Design tooling
When a task calls for new UI/design work (new components, layout changes,
visual polish, new views), use the **21st.dev MCP server** (configured as
`21st`, HTTP transport at `https://21st.dev/api/mcp`) to source or generate
the design/component instead of hand-rolling it from scratch. Adapt whatever
it returns to this project's single-file structure and existing CSS custom
properties (`--green`, `--black`, `--dark`, `--surface`, `--text`, etc.) —
don't introduce a build step or external framework to use it; port the
markup/CSS into `index.html` inline.

**Known issue:** as of 2026-09-20, this server showed `! Needs authentication`
via `claude mcp list`, and this sandboxed environment's outbound network
policy was blocking egress to `21st.dev:443` entirely (proxy `connect_rejected`).
Before relying on it, verify the API key is valid on the 21st.dev dashboard
and confirm the environment's network policy allows `21st.dev`.
