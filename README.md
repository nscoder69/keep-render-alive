# Keep Render Backend Alive

This repository runs a GitHub Actions workflow on a 5-minute schedule to ping Render backends:
1. **ESPORTS ARENA**: `https://esports-arena-906z.onrender.com/api/v1/public/ping`
2. **PROJECT ARENA**: `https://project-arena-backend.onrender.com/api/public/ping` & `https://project-arena.onrender.com/api/public/ping`

## Features
- **Prevent Render Sleep**: Render free-tier instances go to sleep after 15 minutes of inactivity. Pinging every 5 minutes keeps the instances warm 24/7.
- **Valid Health Endpoints**: Hits `/api/public/ping` which returns HTTP 200 OK (`pong`).
- **Manual Trigger**: Can be manually triggered anytime via the **Actions** tab on GitHub using `workflow_dispatch`.
