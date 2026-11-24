# 🔒 loopforge-secure

[![Security](https://img.shields.io/badge/type-secure%20setup-blue)](https://github.com/tunnabri-ops/loopforge-secure)
[![Language](https://img.shields.io/badge/UI-English-orange)](https://github.com/tunnabri-ops/loopforge-secure)

**Secure-by-default setup for a self-hosted AI coding workspace — signup off, localhost only, HTTPS in front.**

> বাংলা সংস্করণ নিচে আছে। / Bangla version below.

## ✨ Features

- **Signup disabled by default** — `.env.example` sets `AGENTFLOW_ALLOW_SIGNUP=false`
- **Localhost only** — `HOST=127.0.0.1`, `PORT=8090`; never exposed publicly
- **Hardening checklist** in `HARDENING.md` — HTTPS reverse proxy (Caddy / Nginx / Cloudflare Tunnel), strong admin password, restricted project creation and invites, MySQL volume backups, no Docker socket access
- **The problem, documented** — `secure-setup.md` explains the insecure defaults this setup fixes: listening on `0.0.0.0:8090`, open signup from the login page, and signed-in users reading project data across the instance

## 🚀 How to use

1. Copy `.env.example` to `.env`.
2. Work through the checklist in `HARDENING.md`.
3. Put a reverse proxy with HTTPS in front (Caddy / Nginx / Cloudflare Tunnel) — do **not** expose port 8090 publicly.

## ⚠️ Honest limits

- Needs Docker, Compose, Python 3, curl and MySQL — document each step before installing.
- Do **not** expose the Docker socket to the app.
- This repo is a secure setup guide, not the workspace app itself.

## 🇧🇩 বাংলা

**সিকিউর সেটআপ — নিজের সার্ভারে AI কোডিং ওয়ার্কস্পেস, নিরাপদ ডিফল্টে।**

- `.env.example` থেকে `.env` বানান — সাইনআপ বন্ধ, শুধু localhost
- সামনে HTTPS রিভার্স প্রক্সি (Caddy / Nginx / Cloudflare Tunnel) বসান
- 8090 পোর্ট কখনো পাবলিক করবেন না

## 📄 License

MIT — use it however you like; credit is appreciated.
