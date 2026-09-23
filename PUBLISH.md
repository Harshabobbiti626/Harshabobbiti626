# Publish your GitHub Profile Portfolio

Everything in this folder is a ready-to-push package for your special **profile README repo**.
A repo named exactly after your username renders `README.md` on your GitHub profile page.

## What's inside

| File | Purpose |
|---|---|
| `README.md` | The profile itself — hero art, about, projects, stack, live stats |
| `assets/iso-stack.svg` | Hand-authored animated 3D component (floating cubes) |
| `.github/workflows/snake.yml` | Nightly **snake animation** over your contribution graph → publishes SVGs to the `output` branch |
| `.github/workflows/3d-contrib.yml` | Nightly **3D contribution graph** → commits SVGs to `profile-3d-contrib/` on `main` |

## Steps (≈ 3 minutes)

**1. Create the repo**
Go to [github.com/new](https://github.com/new) → repository name must be exactly:

```
Harshabobbiti626
```

Set it **Public**, leave "Add a README" **unchecked**, create it.
(GitHub shows a hint: *“Harshabobbiti626/Harshabobbiti626 is a special repository…”*)

**2. Push this folder**

```bash
cd path/to/github-profile
git remote add origin https://github.com/Harshabobbiti626/Harshabobbiti626.git
git push -u origin main
```

**3. Let Actions write to the repo** *(required — the art generators commit files)*
Repo → **Settings → Actions → General → Workflow permissions** → select
**“Read and write permissions”** → Save.

**4. Generate the art once**
Repo → **Actions** tab → run **“Contribution Snake”** and **“3D Contribution Graph”**
manually via **Run workflow**. (They also re-run automatically every night.)

**5. Done** — refresh `github.com/Harshabobbiti626`.
Stats cards, pins and hero render instantly; the snake + 3D graph appear ~1 minute
after their workflows finish.

## Troubleshooting

- **Snake image missing** → check the Actions run succeeded; the SVGs live on the `output` branch, which the README references directly.
- **3D graph missing** → confirm workflow permissions (step 3); the files are committed to `main` under `profile-3d-contrib/`.
- **Stats cards stuck on “loading”** → github-readme-stats' public instance occasionally rate-limits; they recover on next page load.

## Optional polish

- On your profile, click **Customize pins** and pin the 3 flagship repos so they appear above the README.
- Add topics (`java`, `spring-boot`, `microservices`, `redis`, `kubernetes`…) to each repo for discoverability.
- Keep the email badge only if you're comfortable with it being public — it's already on your resume, but it will be visible to everyone here.
