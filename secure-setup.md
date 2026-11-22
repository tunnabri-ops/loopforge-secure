# LoopForge — secure default setup

Source: https://github.com/Tencent/LoopForge

## The problem
Default install listens on `0.0.0.0:8090`, new accounts can sign up from the login page, and signed-in users can read project data across the instance.

## Secure fix
- Set `AGENTFLOW_ALLOW_SIGNUP=false` by default (see `.env.example`)
- Bind to localhost + HTTPS reverse proxy / IP restriction, do NOT expose 8090 publicly
- Add a one-command Windows / Cloudflare Tunnel quick-start
- Current setup needs Docker, Compose, Python 3, curl and MySQL — document each step
