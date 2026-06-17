# GitHub Backup — Step by Step

Connect your local Git repos (already initialized) to private GitHub repos for off-machine backup + sync. Replace `<YOU>` with your GitHub username.

> You do: create the account, create the repos, make a token. Everything else is paste-ready.

---

## Before you start
- A free GitHub account (github.com → Sign up) if you don't have one.
- We make **3 separate PRIVATE repos** — never one shared repo (keeps the walls).

## Part A — Create the repos (on github.com)
Do this for **obsidian-main** and **power-by-design** (hold Mercer — see the Wall section):
1. Go to **github.com/new**
2. **Repository name:** `obsidian-main` (then repeat for `power-by-design`)
3. **Visibility: Private** ✅
4. **Do NOT** check "Add a README", ".gitignore", or "license" — the vault already has files.
5. Click **Create repository**.

## Part B — Connect + push (Terminal)
```bash
# Main vault
git -C ~/Obsidian remote add origin https://github.com/<YOU>/obsidian-main.git
git -C ~/Obsidian push -u origin main

# Power by Design
git -C ~/Power-by-Design remote add origin https://github.com/<YOU>/power-by-design.git
git -C ~/Power-by-Design push -u origin main
```

## Part C — Auth on first push (Personal Access Token)
GitHub no longer accepts your password for git. When `git push` prompts:
- **Username:** your GitHub username
- **Password:** a **Personal Access Token (PAT)** — not your password.

Make a PAT: GitHub → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token** → give it **repository access** to your new repos → Generate → copy. Paste it as the password. macOS stores it in Keychain, so you do this once.

## Part D — Auto-backup (Obsidian Git plugin)
For each vault (open it in Obsidian first):
1. **Settings → Community plugins → Browse →** search **"Obsidian Git"** → Install → Enable.
2. **Settings → Obsidian Git →** set **Vault backup interval** to `10` (minutes) and enable **Push on backup**.

Now every change auto-commits and pushes.

---

## ⚠️ The Mercer wall — do this one differently
Mercer is your pen name. To keep it unlinkable to your identity:
- Create the **`mercer`** repo under a **separate GitHub account in the pen name** (or at minimum a private repo not tied to your real identity).
- Before pushing, set its commit email to that account's noreply:
  ```bash
  git -C ~/Mercer config user.email "<pen-name-id>@users.noreply.github.com"
  git -C ~/Mercer remote add origin https://github.com/<PEN-NAME>/mercer.git
  git -C ~/Mercer push -u origin main
  ```
- If you'd rather not run a second account, you *can* keep it private under your main account — but the repo owner becomes your identity, which weakens the wall. Your call.

## Sanity check after pushing
```bash
git -C ~/Obsidian remote -v
git -C ~/Obsidian log --oneline -1
```
