# Planka (LazyCat LPK)

Real-time kanban board for small teams.

- Upstream: https://github.com/plankanban/planka
- Image: ghcr.io/plankanban/planka:2.2.1 (mirror mode, digest-matched)
- License: PLANKA Community License 1.1 (see `content/licenses/LICENSE.md`)
- Containers: Planka + PostgreSQL 16

## License note

The upstream repo reports NOASSERTION because this is a bespoke licence, not a standard SPDX one.
Reading `LICENSE.md` in full:

- **Copyright License** grants the right to use, copy, **distribute**, make available and
  prepare derivative works.
- **Permitted Use** covers personal/hobby/educational use, internal use inside your own
  organisation, private hosting for friends and family, and non-profits.
- **Restricted Use** forbids offering PLANKA as a hosted service to third parties for
  commercial gain.
- **Limitations** require that licensing and copyright notices are preserved.

Distributing the app to individual users who run it on their own devices falls under
Permitted Use, so the licence text ships unmodified in `content/licenses/`.

## Notes

- Admin account is created from `DEFAULT_ADMIN_EMAIL` / `DEFAULT_ADMIN_PASSWORD` /
  `DEFAULT_ADMIN_USERNAME` — the password comes from a deploy param, so there is no
  built-in credential.
- `BASE_URL` is set to the app's https domain; `TRUST_PROXY=true` for the LazyCat proxy.
- The Redis service from the upstream compose is optional and has been omitted.
- Not yet verified on a real device.
