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
index.html          ← The main team page — loads all member cards via iframes
members/
  member1.html      ← Member 1's profile (already wired up in index.html)
  member2.html      ← Member 2's profile (already wired up in index.html)
  member3.html      ← Member 3's profile (already wired up in index.html)
  member4.html      ← Member 4's profile (already wired up in index.html)
  example.html      ← Reference template showing the structure
profile/
  member1.png       ← Member 1's profile picture (replace with your own)
  member2.png       ← Member 2's profile picture (replace with your own)
  member3.png       ← Member 3's profile picture (replace with your own)
  member4.png       ← Member 4's profile picture (replace with your own)
assets/             ← Workshop logo & mascot images (don't modify)
styles.css          ← Shared stylesheet (don't modify this)
README.md           ← You are here
```

`index.html` already calls each member file using iframes — the main page is ready. Your only job is to fill in your assigned `memberN.html` file.

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

The facilitator will assign each member a number (1–4). Create a branch for your number:

```bash
git checkout -b feature/member1
```

Replace `member1` with your assigned number (e.g. `feature/member2`, `feature/member3`, `feature/member4`).

---

### Step 4 — Fill in your profile file

You've been assigned a file in the `members/` folder — open it in your editor:

- Member 1 → `members/member1.html`
- Member 2 → `members/member2.html`
- Member 3 → `members/member3.html`
- Member 4 → `members/member4.html`

Replace all the placeholder text with your own info:

| Placeholder | Replace with |
|---|---|
| `profile/memberN.png` | Replace the file with your own photo (keep the same filename) |
| `YOUR NAME` | Your full name |
| `YOUR ROLE` | Your role, title, or how you'd describe yourself |
| The bio text | 2–3 sentences about yourself |
| The fun fact text | One fun or surprising fact |
| `❓` | Your single favourite emoji |

Open your file directly in a browser to preview your card before committing!

> 📌 `index.html` is **already wired up** — it loads all four member files using iframes. You do NOT need to edit `index.html` at all. Just fill in your assigned file.

---

### Step 5 — Stage and commit

```bash
git add members/memberN.html profile/memberN.png   # replace N with your number
git status
git commit -m "Add profile for Your Name"
```

---

### Step 6 — Push your branch

```bash
git push origin feature/memberN   # replace N with your number
```

---

### Step 7 — Open a Pull Request

1. Go to the team's forked repo on GitHub
2. You'll see a banner: **"Compare & pull request"** — click it
3. Write a short description of what you added
4. Submit the PR

---

### Step 8 — Review and merge as a team

As a team, look at each other's PRs:
- Check that the profile card looks right
- Leave a comment (even just a 👍)
- Merge each PR once it's reviewed

After all PRs are merged, open `index.html` in a browser — all four cards will appear automatically since the iframes are already pointing to each member file!

---

## ⚠️ Note on Merge Conflicts

Because each person only edits their own `memberN.html` file and nobody touches `index.html`, merge conflicts are very unlikely in this exercise. This is intentional — structuring a project so team members work on separate files is a good habit.

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
