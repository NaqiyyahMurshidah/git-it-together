# 👥 Git It Good Innit — Repo 2: `git-it-together`

**Difficulty:** 🟡 Intermediate — Collaborative
**Skills practiced:** Forking, branching, pull requests, team collaboration

---

## 📖 The Scenario

Your team just got hired at a startup and HR needs a team profile page live by end of day. Each member creates their own profile card and submits it via a pull request. The designer (that's also you) has already set up the base page — you just need to fill it with people.

The trick? Everyone works on a **different file** so you won't step on each other's toes. This is intentional — good team workflow is about avoiding unnecessary conflicts before they happen.

*(We'll deal with conflicts in Repo 3. For now, let's build something together cleanly.)*

---

## 📁 Repo Structure

```
index.html          ← The main team page (combines all member cards)
members/
  example.html      ← Template — copy this to create your profile
styles.css          ← Shared stylesheet (don't modify this)
README.md           ← You are here
```

---

## 🚀 Step-by-Step Instructions

### Step 1 — One person forks the repo

**Only ONE member of your team does this step.**

1. Fork this repo to your GitHub account (top-right Fork button)
2. This forked repo becomes your **team's shared repo**
3. Go to **Settings → Collaborators** on the forked repo
4. Add each teammate's GitHub username so they can push to it

> 💡 The fork URL will look like: `https://github.com/YOUR-USERNAME/git-it-together`

---

### Step 2 — Everyone clones the team repo

All team members (including the person who forked) run:

```bash
git clone https://github.com/FORKING-MEMBERS-USERNAME/git-it-together.git
cd git-it-together
```

---

### Step 3 — Each person creates their own branch

Each member creates a branch named after themselves:

```bash
git checkout -b feature/add-yourname
```

For example:
```bash
git checkout -b feature/add-sarah
git checkout -b feature/add-marcus
```

---

### Step 4 — Create your profile file

1. Copy the template file:
   ```bash
   cp members/example.html members/yourname.html
   ```
   Use your first name, lowercase, no spaces. e.g. `members/sarah.html`

2. Open your new file and fill in all the fields marked with `← CHANGE THIS`:
   - Your emoji avatar
   - Your name
   - Your role/title
   - A short bio (2–3 sentences)
   - A fun fact
   - Your favourite emoji

3. Open `members/yourname.html` in your browser to preview it!

---

### Step 5 — Add yourself to the main page

Open `index.html` and find the comment block that says `TEAM MEMBERS GO HERE`.

Add your member card **inside the `team-grid` div**, directly after the comment block:

```html
<div class="member-card">
  <div class="member-avatar">YOUR_EMOJI</div>
  <div class="member-name">Your Name</div>
  <div class="member-role">Your Role</div>
  <div class="member-bio">Your bio goes here.</div>
  <div class="fun-fact"><span>Fun fact:</span> Your fun fact here.</div>
  <div class="fav-emoji">YOUR_EMOJI</div>
</div>
```

> 📌 **Each member edits a DIFFERENT section** — you're adding your own card to `index.html`, not changing anyone else's. This is intentional — we'll tackle merge conflicts in Repo 3!

---

### Step 6 — Stage and commit

```bash
git add members/yourname.html
git add index.html
git status
git commit -m "Add profile card for Your Name"
```

---

### Step 7 — Push your branch

```bash
git push origin feature/add-yourname
```

---

### Step 8 — Open a Pull Request

1. Go to the team's forked repo on GitHub
2. You'll see a banner: **"Compare & pull request"** — click it
3. Write a short description of what you added
4. Submit the PR

---

### Step 9 — Review and merge as a team

As a team, look at each other's PRs:
- Check that the profile card looks right
- Leave a comment (even just a 👍)
- Merge each PR once it's reviewed

After all PRs are merged, the `index.html` will show the full team!

---

## ⚠️ Note on Merge Conflicts

You might notice that **multiple people are editing `index.html`**. If two people push conflicting changes to the same section of `index.html`, GitHub will warn you about a merge conflict.

If this happens:
1. Pull the latest main branch: `git pull origin main`
2. Git will mark the conflict in the file
3. Manually resolve it (keep both cards!)
4. Stage and commit the resolved file
5. Push again

> 🔮 Want to understand merge conflicts properly? That's what Repo 3 is for!

---

## 📝 Writeup Submission

Write up your experience CTF-style. Your writeup should include:

- **Links to each team member's merged Pull Request** on GitHub
- **Screenshot of the final `index.html`** page showing all team cards
- **What each member contributed** — whose profile is whose
- **Git commands used** — the key commands each person ran
- **Reflection** — did anyone run into a merge conflict? How did you resolve it?

> 🏁 Submit your writeup as a markdown file (`writeup.md`) pushed to the team repo, or as a shared Google Doc / Notion link.

---

*Part of the **Git It Good Innit** workshop series.*
