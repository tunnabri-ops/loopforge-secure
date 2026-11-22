# LoopForge hardening checklist

- [ ] `AGENTFLOW_ALLOW_SIGNUP=false` (see .env.example)
- [ ] Bind 127.0.0.1 only, no public 8090
- [ ] HTTPS reverse proxy (Caddy / Nginx / Cloudflare Tunnel)
- [ ] Strong admin password + rotate default secrets
- [ ] Restrict who can create projects / invite users
- [ ] Back up the MySQL volume before upgrades
- [ ] Do NOT expose the Docker socket to the app
