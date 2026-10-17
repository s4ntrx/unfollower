<a><img src='https://i.imgur.com/LyHic3i.gif'/></a>
<h1 align="center"> 𝐔𝐍𝐅𝐎𝐋𝐋𝐎𝐖𝐄𝐑 </h1>

- **Be petty:** run a GitHub Actions workflow that automatically unfollows anyone in your following who doesn't follow you back.


<details>
<summary>NOTICE!!! (TAP TO READ)</summary>

- This runs entirely on **GitHub Actions** — no server, no VPS, no hosting costs.
- You **must fork this repo** — the workflow will not run on the original.
- The unfollow action is **permanent**. GitHub does not have an undo for unfollows.
- Scheduled workflows are **disabled after 60 days of repo inactivity**. Push any commit or run it manually to keep it alive.

</details>

<a><img src='https://i.imgur.com/LyHic3i.gif'/></a>

  <p align="center">
<a href="https://github.com/s4ntrx"><img title="GITHUB" src="https://img.shields.io/badge/GITHUB-S4NTRX-red.svg?style=for-the-badge&logo=github"></a>
<p/>
<p align="center">
<a href="https://github.com/s4ntrx?tab=followers"><img title="Followers" src="https://img.shields.io/github/followers/s4ntrx?label=Followers&style=social"></a>
<a href="https://github.com/s4ntrx/unfollower/stargazers/"><img title="STARS" src="https://img.shields.io/github/stars/s4ntrx/unfollower?&style=social"></a>
<a href="https://github.com/s4ntrx/unfollower/network/members"><img title="Forks" src="https://img.shields.io/github/forks/s4ntrx/unfollower?style=social"></a>
<a href="https://github.com/mwakidenis/unfollower/watchers"><img title="Watching" src="https://img.shields.io/github/watchers/s4ntrx/unfollower?label=Watching&style=social"></a>

<a><img src='https://i.imgur.com/LyHic3i.gif'/></a>

## 𝟏. 𝐅𝐎𝐑𝐊 𝐑𝐄𝐏𝐎 (𝐀 𝐌𝐔𝐒𝐓):

**👇FORK REPO**
<details>
<summary>𝗖𝗟𝗜𝗖𝗞 𝗛𝗘𝗥𝗘</summary>
  
- This is essential — GitHub Actions only run on **your own** fork, not on this repo.

<a href="https://github.com/s4ntrx/unfollower/fork"><img src="https://img.shields.io/badge/CLICK%20HERE-purple" alt="FORK" width="150"></a>
</details>

<a><img src='https://i.imgur.com/LyHic3i.gif'/></a>

### 𝟐. 𝐄𝐍𝐀𝐁𝐋𝐄 𝐀𝐂𝐓𝐈𝐎𝐍𝐒

<details>
<summary>TAP TO OPEN</summary>

Go to your forked repository and enable workflows:

- `Settings` -> `Actions` -> `General`
- Select **Allow all actions and reusable workflows**
- Click **Save**

</details>

<a><img src='https://i.imgur.com/LyHic3i.gif'/></a>

### 𝟑. 𝐆𝐄𝐍𝐄𝐑𝐀𝐓𝐄 𝐏𝐄𝐑𝐒𝐎𝐍𝐀𝐋 𝐀𝐂𝐂𝐄𝐒𝐒 𝐓𝐎𝐊𝐄𝐍:

<details>
<summary>GET YOUR PAT</summary>
<a href="https://github.com/settings/tokens"><img src="https://img.shields.io/badge/CLICK%20HERE-green" alt="Generate Token" width="150"></a>

- Click **Generate new token** -> **Generate new token (classic)**
- Under the `user` scope, tick the **`user:follow`** sub-scope
- Copy the token immediately — GitHub only shows it once
</details>

<a><img src='https://i.imgur.com/LyHic3i.gif'/></a>

### 𝟒. 𝐀𝐃𝐃 𝐓𝐇𝐄 𝐒𝐄𝐂𝐑𝐄𝐓:

<details>
<summary>TAP TO OPEN</summary>

In your forked repository:

1. Go to `Settings`
2. Go to `Secrets and variables` -> `Actions`
3. Click **New repository secret**
4. Name it exactly: **`GH_TOKEN`**
5. Paste your Personal Access Token as the value
6. Click **Add secret**

> Without `GH_TOKEN` the workflow will fail on the unfollow step.
</details>

<a><img src='https://i.imgur.com/LyHic3i.gif'/></a>

### 5. 𝐇𝐎𝐖 𝐓𝐎 𝐌𝐀𝐍𝐔𝐀𝐋𝐋𝐘 𝐓𝐑𝐈𝐆𝐆𝐄𝐑 𝐓𝐇𝐄 𝐖𝐎𝐑𝐊𝐅𝐋𝐎𝐖:

<details>
<summary>𝗧𝗔𝗣 𝗧𝗢 𝗢𝗣𝗘𝗡</summary>

The workflow is set to run automatically every 5 days, but you can also trigger it **manually at any time** without waiting for the schedule. This is useful for testing, or when you want to unfollow immediately.

---

**📱 Method 1 — From the GitHub Website (easiest)**

1. Open your forked repository in a browser: `https://github.com/YOUR_USERNAME/unfollower`
2. Click the **Actions** tab at the top of the repo.
3. In the **left sidebar**, click **Unfollow Non-Followers**.
4. On the right side, click the **Run workflow** dropdown button.
5. Make sure the branch is set to **main** (or your default branch).
6. Click the green **Run workflow** button.
7. Refresh the page — a new run will appear at the top with a **yellow dot** (running). Once it finishes, it turns **green** (success) or **red** (failed).

---

**💻 Method 2 — Using GitHub CLI (`gh`)**

If you have the [GitHub CLI](https://cli.github.com/) installed and authenticated, run:

```bash
gh workflow run "Unfollow Non-Followers" --repo YOUR_USERNAME/unfollower




