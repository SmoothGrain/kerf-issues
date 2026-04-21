# Security Policy

Thanks for helping keep Kerf and its users safe.

## Reporting a vulnerability

**Email [security@smoothgrain.app](mailto:security@smoothgrain.app)** with:

- A description of the issue and the impact.
- Steps to reproduce (or a proof-of-concept).
- Your Kerf version, OS, and how you discovered the issue.
- Whether the issue is already public or shared with anyone else.

Please **do not** open a public issue, pull request, or discussion for security problems.

## What to expect

- **Acknowledgement** within 72 hours, usually sooner.
- **Initial triage and severity assessment** within 7 days.
- **Fix timeline**: depends on severity. Critical issues get a patch release ASAP; lower-severity issues land in the next scheduled release.
- **Coordinated disclosure**: 90-day default. We'll agree a disclosure date with you and credit you in the release notes unless you ask us not to.

## Scope

In scope:

- The Kerf desktop app (macOS, Windows, Linux) — installer, auto-update, renderer, main process, preload bridge.
- The device-auth flow between Kerf and `smoothgrain.app`.
- The static preview server Kerf runs on `127.0.0.1` while a workspace is open.
- The license / entitlement store on disk.
- Kerf's Vercel deploy integration (what the app does with a provided Vercel token).

Out of scope:

- Third-party services Kerf talks to (Vercel API, LemonSqueezy, Cloudflare R2). Report those to the respective vendors.
- Issues that require an already-compromised machine (e.g., another process on the same user account reading plaintext config) unless Kerf materially makes the compromise worse.
- Denial of service against Kerf's own processes on the user's own machine.
- Social engineering of Smoothgrain staff.

## Safe harbour

We won't pursue legal action for good-faith security research that:

- Stays within the in-scope targets above.
- Doesn't access, modify, or delete other users' data.
- Gives us reasonable time to investigate and fix before public disclosure.

## PGP

Not currently offered. If you need encrypted communication, email us and we'll set up a channel.
