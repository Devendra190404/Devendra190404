# Daily GitHub Activity Setup

This repo uses GitHub Actions to append one line per day to `activity/activity.log`.

## Important: streak counting

GitHub **does not count** commits made with the default `GITHUB_TOKEN` toward your contribution graph.

For daily commits to count toward your **green squares / streak**, you must add a **Personal Access Token (PAT)** as a repository secret.

## One-time setup (5 minutes)

### 1. Create a Personal Access Token

1. Go to [GitHub Settings → Developer settings → Personal access tokens](https://github.com/settings/tokens)
2. **Generate new token (classic)**
3. Name: `daily-activity-profile`
4. Expiration: 90 days or No expiration (your choice)
5. Scopes: check **`repo`** (full control of private repositories)
6. Generate and **copy the token** (you won't see it again)

### 2. Add secret to this repository

1. Open [Devendra190404/Devendra190404 → Settings → Secrets and variables → Actions](https://github.com/Devendra190404/Devendra190404/settings/secrets/actions)
2. **New repository secret**
3. Name: `GH_PAT`
4. Value: paste your token
5. Save

### 3. Enable GitHub Actions

1. Go to **Actions** tab on the repo
2. Click **I understand my workflows, go ahead and enable them**

### 4. Test manually

1. Actions → **Daily Activity Update** → **Run workflow**
2. Wait ~30 seconds
3. Check your [contribution graph](https://github.com/Devendra190404) (may take a few minutes to update)

## Schedule

- Runs automatically every day at **12:05 AM IST**
- You can also trigger it manually from the Actions tab

## Notes

- Use this to keep your profile repo active; real project commits are always better for recruiters
- GitHub may change how automated commits are counted
- Ensure `72194247+Devendra190404@users.noreply.github.com` is linked to your GitHub account (Settings → Emails)
