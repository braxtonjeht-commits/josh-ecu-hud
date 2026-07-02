# Changelog — josh-ecu-hud

All notable changes to the shop wall display.

## 2026-07-02

- `e4bbd51` Sanitized `order_id` in the card render (same class of gap as the dashboard) — previously rendered without the `s()` sanitizer.

### Shared backend
The Supabase project this app reads from (`josh-ecu-shop`) had its RLS policies locked down and a trigger regression fixed on this date — see [josh-ecu-dashboard/CHANGELOG.md](https://github.com/braxtonjeht-commits/josh-ecu-dashboard/blob/main/CHANGELOG.md) for the full writeup. This app was verified read-only (`SELECT` on `orders` only, no writes) before the lockdown and needed no policy changes of its own.
