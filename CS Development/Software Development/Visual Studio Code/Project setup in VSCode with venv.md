[[Software Development]]
### 🔁 Project Setup Template for macOS

#### 🗂 Folder Structure:

```
my-python-project/
│
├── venv/              ← Virtual environment folder (auto-created)
├── main.py            ← Your Python script(s)
├── requirements.txt   ← For dependencies (optional)
└── .vscode/
    └── settings.json  ← VS Code project settings
```

---

### ✅ 1. Create the project and virtual environment

```
mkdir my-python-project
cd my-python-project
python3 -m venv venv
source venv/bin/activate
```

---

### ✅ 2. Create VS Code project settings

Create a folder `.vscode` and inside it, add a `settings.json` file:

```
mkdir .vscode
touch .vscode/settings.json
```

Paste this into `.vscode/settings.json`:

```
{
  "python.pythonPath": "venv/bin/python3",
  "python.formatting.provider": "black",
  "python.linting.enabled": true,
  "python.linting.pylintEnabled": true,
  "python.envFile": "${workspaceFolder}/.env",
  "terminal.integrated.profiles.osx": {
    "zsh (with venv)": {
      "path": "zsh",
      "args": ["-l", "-c", "source venv/bin/activate && exec zsh"]
    }
  },
  "terminal.integrated.defaultProfile.osx": "zsh (with venv)"
}
```

> 🧠 This assumes you’re using the **Zsh shell** (the default on macOS). If you're using **Bash**, change `"zsh"` to `"bash"` everywhere.

---

### ✅ 3. (Optional) Add `requirements.txt`

```
touch requirements.txt
```

When you install packages (e.g., `pip install pandas`), run:

```
pip freeze > requirements.txt
```

So you can recreate the environment later with:

```
pip install -r requirements.txt
```

---

### ✅ 4. Run & Debug in VS Code

- Select your interpreter with `Cmd + Shift + P` → `Python: Select Interpreter` → choose `./venv/bin/python`
- Press `F5` to debug or run your script with the green play button.

---

Let me know if you want this turned into a shell script that auto-sets up the whole folder for you!

##### You said:

for the args in the settings.json file my venv is .venv with a .

###### ChatGPT said:

Nice catch — if your virtual environment is named `.venv` (with the dot), you just need to adjust the paths in `settings.json` accordingly.

---

### 🛠️ Updated `settings.json` (for `.venv` folder on macOS with Zsh):

```
{
  "python.pythonPath": ".venv/bin/python3",
  "python.formatting.provider": "black",
  "python.linting.enabled": true,
  "python.linting.pylintEnabled": true,
  "python.envFile": "${workspaceFolder}/.env",
  "terminal.integrated.profiles.osx": {
    "zsh (with venv)": {
      "path": "zsh",
      "args": ["-l", "-c", "source .venv/bin/activate && exec zsh"]
    }
  },
  "terminal.integrated.defaultProfile.osx": "zsh (with venv)"
}
```

---

✅ Now VS Code will:

- Use `.venv/bin/python3` as the interpreter
- Automatically activate `.venv` every time you open a terminal
- Use `zsh` and re-run your environment smoothly

Let me know if you want a version of this using Bash instead of Zsh!