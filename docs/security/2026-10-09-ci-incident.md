# CI incident containment — 2026-10-09

Repository: `ThreeAndTwo/ord`
Branch: `fractal`
Inspected head: `ea0a1b20e2abc1463eb604d1e383772a2ca86202`

Actions were disabled before this cleanup. Keep them disabled until the repository owner explicitly approves restoration.

The owner confirmed that this personal repository must not contain GitHub Actions workflows. This change removes every file under `.github/workflows` on this branch, regardless of its name.

Files removed in this change:

- `.github/workflows/ci.yaml` — original Git object `c1322ae10f9f7fee2832bcea6efd472cc435f2c4`.
- `.github/workflows/release.yaml` — original Git object `374d8f0b1b3e866a92b64ba8541f1dd125ee5497`.
- `.github/workflows/security-audit.yml` — original Git object `a5a0cbcf7f5aa30b5ac499d441e7ecc089fd1ea5`.

Evidence and limits

- Unauthorized workflows were observed attempting credential or repository-history disclosure. A successful workflow run alone does not prove data receipt or credential validity.
- Existing Git history is retained as evidence. No release, tag, force push, or history rewrite is part of this cleanup.
- Revoking a GitHub token does not rotate credentials issued by other services.
- The initial credential compromise and the authentication method used for the mass write remain under investigation.
- This record supersedes any earlier note suggesting that personal-repository workflows should be retained.
