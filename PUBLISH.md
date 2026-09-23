# Publish your GitHub Profile Portfolio

This folder is a ready-to-push package for your special **profile README repo**
(`Harshabobbiti626/Harshabobbiti626`). The repo already exists and your remote
history has been merged locally — pushing is a clean fast-forward.

## What's inside

| File | Purpose |
|---|---|
| `README.md` | The profile — 3D hero, Kairvex ecosystem, stack, live stats, cozy artifacts |
| `assets/iso-stack.svg` | Hand-authored animated 3D component (floating cubes) |
| `assets/desk.svg` | Cozy artifact — typing code, steaming coffee, sleeping cat |
| `assets/orbit.svg` | Cozy artifact — waving astronaut, planet, orbiting cube |
| `assets/kairvex-banner.jpg` | Your Kairvex banner (moved from repo root) |
| `.github/workflows/3d-contrib.yml` | Nightly **3D contribution graph** → commits SVGs to `profile-3d-contrib/` on `main` |

## Steps (≈ 2 minutes)

**1. Push**

```bash
cd path/to/github-profile
git push origin main
```

A GitHub sign-in window appears once (no cached credentials on this machine).
If the push is ever rejected, `git push --force-with-lease origin main` is safe here —
nothing is lost: your banner is preserved in `assets/` and your draft content is merged.

**2. Let Actions write to the repo** *(required — the art generator commits files)*
Repo → **Settings → Actions → General → Workflow permissions** →
**“Read and write permissions”** → Save.

**3. Generate the skyline once**
Repo → **Actions** → run **“3D Contribution Graph”** via **Run workflow**.
It re-runs automatically every night.

**4. Done** — refresh `github.com/Harshabobbiti626`.
Hero, banner, artifacts and stats render instantly; the 3D skyline appears ~1 minute
after the workflow finishes.

## Notes

- **kairvex-\* links** point to `github.com/Kairvex-Eco-System/<repo>` — they 404 until
  those repos are created/published under the org. The links are already canonical, so
  no README change is needed when the repos go live.
- **Phone badge** is intentionally included per your draft — it is visible to everyone;
  delete the Phone line in `✦ Connect` any time to remove it.
- **Stats cards** use `github-profile-summary-cards` (the classic `github-readme-stats`
  public instance was rate-limiting; this one is verified stable).

## Troubleshooting

- **3D skyline missing** → confirm workflow permissions (step 2); files are committed to `main` under `profile-3d-contrib/`.
- **Banner not showing** → ensure `assets/kairvex-banner.jpg` was pushed (it's part of this repo).
- **Animations not playing** → they run in all modern browsers; if you view the raw file in an editor they appear static.
