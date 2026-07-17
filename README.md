# ⚛️ Introduction to Quantum Computing with Qiskit
### 👩‍💻 Girls Code Too

> 🚀 Welcome! You're about to run **real quantum circuits** on your laptop.
> No physics degree needed — just curiosity and a terminal. Let's go!

---

## 👉 Start Here

**New to quantum? Open this first:**

### 🗳️ [Vote for Your First Experiment →](web/1stExperimentVote.html)
Pick the experiment you want to try — then follow the tutorial. Takes 2 minutes and sets you up for everything else.

---

## 🗂️ What's in this repo?

### 📓 Notebooks

| File | What it does |
|---|---|
| [`notebooks/hello-world.ipynb`](notebooks/hello-world.ipynb) | Your first quantum circuit in code (as in [quantum.cloud.ibm](https://quantum.cloud.ibm.com/docs/en/guides/hello-world)) 🔬 |

### 📄 Tutorials & Guides

| File | What it does |
|---|---|
| [`tutorials/student-note.md`](tutorials/student-note.md) | Novices walkthrough — no coding needed yet 📖 |
| [`tutorials/teacher-note.md`](tutorials/teacher-note.md) | Notes for teachers running this session 👩‍🏫 |

### 🌐 HTML Pages

| File | What it does |
|---|---|
| [`web/1stExperimentVote.html`](web/1stExperimentVote.html) | 🗳️ Vote for your first experiment — **start here!** |
| [`web/quantum-tutorial-novice.html`](web/quantum-tutorial-novice.html) | 🖥️ Create an account on IBM Cloud |
| [`notebooks/links-to-qiskit-tutorials.html`](notebooks/links-to-qiskit-tutorials.html) | Curated links to Qiskit tutorials 🌐 |

### 🖼️ Images

| File | What it does |
|---|---|
| [`web/qaccount-qr.png`](web/qaccount-qr.png) | QR code to create your IBM Quantum account 📱 |
| [`web/qrcodeform.png`](web/qrcodeform.png) | QR code for the experiment vote form 📋 |

---

## 1️⃣ Download the repository

**With Git (recommended):**
```bash
git clone https://github.com/your-username/qiskit-vscode-mps.git
cd qiskit-vscode-mps
```

**No Git? No problem — download a ZIP instead:**
1. Go to the repository page on GitHub and click **Code → Download ZIP** 📦
2. Unzip the archive and `cd` into the project root folder.

---

## 2️⃣ Install dependencies

Pick **either** method — both install the exact same packages. ✅

### 🅰️ Option A — pip *(standard, no extra tools needed)*

```bash
python -m venv .venv

# macOS / Linux:
source .venv/bin/activate

# Windows (PowerShell):
.venv\Scripts\Activate.ps1

pip install -r requirements.txt
```

### 🅱️ Option B — uv *(faster ⚡)*

Install `uv` first if you don't have it:

```bash
# macOS / Linux:
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows (PowerShell):
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Then just run:

```bash
uv sync
```

> 💡 **One-time only.** After the first install, `.venv` is ready to go. Only re-run if you change the dependencies.

---

## 3️⃣ Open in VS Code

```bash
code .
```

Or open VS Code manually → **File → Open Folder** → select the project root. 📂

---

## 4️⃣ Select the Python interpreter

1. Press `Ctrl+Shift+P` (or `⌘⇧P` on macOS) and type **Python: Select Interpreter** 🔍
2. Choose the interpreter that shows `.venv` in its path — something like:

   ```
   Python 3.x.x  ('.venv': venv)   ./.venv/bin/python
   ```

VS Code will remember this for every notebook in the project. 🧠

---

## 5️⃣ Run a notebook 🎉

1. Open any `.ipynb` file in VS Code.
2. Click **Select Kernel** (top-right of the notebook) and confirm the `.venv` interpreter.
3. Click **Run All** — or run cells one by one with `Shift+Enter`.

Watch the quantum magic happen! ✨

---

## Running all notebooks from the terminal

```bash
uv run jupyter nbconvert --to notebook --execute src/*.ipynb --inplace
```

Results (output, plots) are saved back into each `.ipynb` file. 

---

## Optional: JupyterLab UI

Prefer a browser interface instead of VS Code? Try JupyterLab!

**pip:**
```bash
pip install -r requirements-dev.txt
jupyter lab
```

**uv:**
```bash
uv sync --extra dev
uv run jupyter lab
```

A browser tab will open at `http://localhost:8888`. 🌐

---

*Made with ❤️ together with Bob*

# FROM THE ORIGINAL COMMUNITY TUTORIALS: Qiskit Community Tutorials

[![License](https://img.shields.io/github/license/Qiskit/qiskit-tutorials.svg?style=popout-square)](https://opensource.org/licenses/Apache-2.0)

Welcome to the [Qiskit](https://www.qiskit.org/) community tutorials!

In this repository, we've put together a collection of awesome community-contributed Jupyter notebooks that leverage the features of Qiskit in education and applications. Feel free to navigate this repository, to [Fork this repo](https://github.com/qiskit/qiskit-community-tutorials/fork), or to open the [Binder image](https://mybinder.org/v2/gh/qiskit/qiskit-community-tutorials/master?filepath=./index.ipynb).

## Contents

### 1 [Hello, Quantum World with Qiskit](hello_world/) 
Learn from the community how to write your first quantum program.

### 2 [Quantum Games with Qiskit](games/)
Learn quantum computing by having fun. How is there a better way!

### 3 [Quantum Information Science with Qiskit Terra](terra/index.ipynb)
Learn about and how to program quantum circuits using Qiskit Terra. 

### 4 [Textbook Quantum Algorithms with Qiskit Terra](algorithms/index.ipynb)
Learn about textbook quantum algorithms, like Deutsch-Jozsa, Grover, and Shor using Qiskit Terra. 

### 5 [Developing Quantum Applications with Qiskit Aqua](aqua/index.ipynb)
Learn how to develop the fundamentals of quantum applications using Qiskit Aqua

### 6 Awards
Learn from the great contributions to the [IBM Q Awards](https://qe-awards.mybluemix.net/)
* [Teach Me Qiskit 2018](awards/teach_me_qiskit_2018/index.ipynb)
* [Teach Me Quantum 2018](awards/teach_me_quantum_2018/index.ipynb)

## Contribution Guidelines

If you'd like to contribute to `Qiskit Community Tutorials`, please take a look at our
[contribution guidelines](.github/CONTRIBUTING.md). This project adheres to Qiskit's [code of
conduct](.github/CODE_OF_CONDUCT.md). By participating, you are expect to uphold to this code.

We use [GitHub issues](https://github.com/Qiskit/qiskit-tutorials-community/issues) for tracking requests and bugs. Please use our
[slack](https://qiskit.slack.com) for discussion and simple questions. To join our Slack community, use the
[link](https://join.slack.com/t/qiskit/shared_invite/enQtNDc2NjUzMjE4Mzc0LTMwZmE0YTM4ZThiNGJmODkzN2Y2NTNlMDIwYWNjYzA2ZmM1YTRlZGQ3OGM0NjcwMjZkZGE0MTA4MGQ1ZTVmYzk).
For questions that are more suited for a forum, we use the Qiskit tag in the [Stack
Exchange](https://quantumcomputing.stackexchange.com/questions/tagged/qiskit).

## Authors and Citation

`Qiskit Community Tutorials` is the work of [many people](https://github.com/Qiskit/qiskit-tutorials-community/graphs/contributors) who
contribute to the project at different levels. If you use Qiskit, please cite as per the included [BibTeX
file](https://github.com/Qiskit/qiskit/blob/master/Qiskit.bib).

## License

[Apache License 2.0](LICENSE.txt)
