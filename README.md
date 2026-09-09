# Cab Operations Management System

Production-oriented cab operations platform built from scratch.

## Architecture
- Android driver app: Kotlin + Jetpack Compose + Room
- Backend: TypeScript + Node.js
- Database/Auth/Storage: Supabase + PostgreSQL
- Admin web: Next.js + React
- GPS: Android Fused Location Provider
- Camera: CameraX
- OCR: ML Kit-ready modular verification layer
- Source control: GitHub

## Core rules
- Sessions are continuous work periods, not calendar-day records.
- Every operational transaction carries a client-generated UUID for idempotency.
- Revenue is separate from expenses and trip-specific charges.
- Offline-first mobile workflow with queued sync.
- Audit important corrections; do not hard-delete financial/operational records.

## Repository layout
```text
apps/
  admin-web/
  driver-android/
services/
  api/
packages/
  shared/
database/
  migrations/
docs/
  architecture/
.github/
  workflows/
```

Development and production environments must use separate data/configuration.
