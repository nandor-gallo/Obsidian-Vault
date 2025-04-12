The **GitHub CLI ( `gh` )** is a command-line tool made by GitHub that lets you **interact with GitHub directly from your terminal** — without needing to go to the website.

### ✅ What You Can Do with GitHub CLI:

- 🔧 **Create repos** ( `gh repo create` )
- 📥 **Clone repos** ( `gh repo clone` )
- 📂 **Push code** and set up remotes
- 📄 **Create PRs** ( `gh pr create` )
- 🧪 **View issues, PRs, workflows** ( `gh issue list`, `gh pr view` )
- ✅ **Merge PRs**, review code, comment — all from the terminal

---

### 📦 Example Use Case (Your Situation)

Say you have a local Git repo and want to upload it to GitHub. With GitHub CLI, you can do this in **one command**:

```bash
bashgh repo create my-repo-name --public --source=. --remote=origin --push
```

This will:

1. Create a GitHub repo named `my-repo-name`
2. Link your local repo to it
3. Push your code up

---

### 🛠️ How to Install GitHub CLI:

- **macOS (Homebrew)**:
	```bash
	bashbrew install gh
	```
- **Windows (winget)**:
	```powershell
	powershellwinget install --id GitHub.cli
	```
- **Linux**: Varies by distro – instructions here: [https://cli.github.com/](https://cli.github.com/)

Once installed, run:

```bash
bashgh auth login
```

This walks you through connecting your GitHub account securely.
