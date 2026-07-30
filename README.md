# Laserhub

Laserhub is a Stuttgart-based digital procurement platform for custom-manufactured metal and plastic
parts. Buyers upload CAD files to app.laserhub.com, get an automated feasibility check and an
instant quote across laser / plasma / flame cutting, tube laser cutting, bending, CNC turning and
milling, weldments and secondary processes, and Laserhub — as the contracting party — allocates the
order across a network of roughly 100 ISO 9001:2015 certified producers in Germany, Austria and
Switzerland.

- Website: https://laserhub.com
- Platform: https://app.laserhub.com
- Release notes: https://laserhub.com/release-notes/
- Backed by: point-nine

## API surface

**Laserhub publishes no public developer API.** Verified 2026-07-19:

- No `/api`, `/developers`, `/docs`, or `Schnittstelle`/ERP-integration page exists in the site's
  264-URL sitemap, and the platform overview pages document no API, SDK, or PLM/ERP connector.
- `api.laserhub.com` resolves to a **private AWS API Gateway** — every unauthenticated request
  returns `403 MissingAuthenticationTokenException`. It backs the first-party web app only.
- `developer.laserhub.com` and `docs.laserhub.com` do not resolve.
- `github.com/laserhub` is an unrelated personal account (one `TestLab` repo), not a Laserhub org.
- The closest machine-adjacent channel Laserhub documents is **ordering by email**
  (`anfrage@laserhub.com`), which its own release notes describe as still in a test phase for a
  subset of customers.

Consequently no `openapi/`, `mcp/`, `skills/`, `scopes/`, `authentication/`, `errors/`,
`data-model/`, `overlays/`, `arazzo/`, or `packages/` artifacts exist here — nothing was fabricated
to fill them.

## Artifacts

| Artifact | Path | Method |
|---|---|---|
| llms.txt | `llms/laserhub-llms.txt` | searched (verbatim, https://laserhub.com/llms.txt) |
| Changelog | `changelog/laserhub-changelog.yml` | searched (release-notes page) |
| Domain security | `security/laserhub-domain-security.yml` | probed |
| Well-known probe | `well-known/laserhub-well-known.yml` | searched (none published) |

Vulnerability-disclosure and trust-center probes returned no hits; no `/.well-known/security.txt`,
no bug-bounty program, and no status page (`status.laserhub.com` does not resolve) were found.
