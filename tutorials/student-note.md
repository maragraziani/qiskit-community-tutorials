# ⚛️ Your First Quantum Experiment

> 🎯 **Mission:** Run a real experiment on a real quantum computer - in about 10 minutes.  
> Let's go! 🚀

---

## 🏆 Pick Your Experiment

Here are five things you can build with one or two quantum gates, ranked by student hype:

| # | Experiment | The pitch | Time |
|---|---|---|---|
| 1 | **Perfect Coin Flip** | A qubit is *genuinely* random — no algorithm, just nature 🌌 | 10 min |
| 2 | **Schrödinger's Qubit** | Watch a qubit literally be 0 and 1 at the same time 🐱 | 10 min |
| 3 | **Quantum Teleportation (baby version)** | Copy a qubit's state to another qubit without physically moving it 📡 | 20 min |
| 4 | **Entangled Pair (Bell State)** | Link two qubits so measuring one instantly decides the other ✨ | 15 min |
| 5 | **Quantum NOT Gate** | Flip a qubit from 0 → 1, the simplest gate ever 🔀 | 5 min |

👉 **Pick your favorite now** 

---

## 🧰 What You Need

- ✅ A free IBM Quantum account (~2 min to create)
- ✅ A web browser — that's literally it
- ❌ No downloads, no installs, no coding (yet!)

---

## Step 1 — Create Your Free IBM Quantum Account 🆓

1. Go to **[quantum.ibm.com](https://quantum.ibm.com)** in your browser.
2. Click **Sign up** (top-right corner).
3. Register with your email, or use a Google account.
4. Confirm your email if prompted, then log in.

> 💡 **Tip:** If your school already has an IBM Quantum account, ask your teacher for the login and skip straight to Step 2.

---

## Step 2 — Open IBM Quantum Composer 🎛️

IBM Quantum **Composer** is a drag-and-drop circuit builder that lives entirely in your browser. You drag gates onto a wire, hit Run, and your circuit executes on a real quantum computer (or a super-fast simulator).

1. After logging in, click **Composer** in the left-hand menu.
2. Click **New circuit** to open a blank canvas.

You'll see a horizontal wire labelled **q[0]** — that's your **qubit** (quantum bit). Think of it as a coin that hasn't been flipped yet.

> 🧠 **What's a qubit?**  
> A regular computer bit is always either 0 or 1 — like a light switch, on or off.  
> A **qubit** can be in a state called **superposition** — *both* 0 and 1 at the same time — until you look at it (measure it). The moment you measure, it snaps to one value randomly. That randomness isn't a bug; it's the laws of physics doing their thing.

---

## Step 3 — Build the Perfect Coin Flip Circuit 🪙

This circuit has exactly **one gate**: the **H gate** (Hadamard gate).

> 🧠 **What does the H gate do?**  
> It takes a qubit that starts as a definite 0 and throws it into superposition — a perfect 50/50 mix of 0 and 1. When you then measure it, quantum mechanics randomly picks one. Unlike `Math.random()` in code, this randomness is *fundamental* to the universe. Nothing decides it in advance.

### What to do

1. Find the gate labelled **H** in the left panel (look in "Standard" or "Common" gates).
2. **Drag the H gate** onto the **q[0]** wire and drop it in the middle.
3. Your circuit should look like this:

```
q[0]: ──[H]──── measure
```

4. Make sure there's a **Measure** symbol (📊 meter icon) at the end of the wire. If not, drag a **Measure** gate onto the wire after the H.

That's it. One gate. One qubit. That's a real quantum circuit. 🎉

---

## Step 4 — Run Your Circuit ▶️

1. Click the **Run** button (it may say "Run on ibm_sherbrooke" or "Run on simulator").
2. For instant results, choose **Statevector Simulator** or **QASM Simulator** — no queue wait, results in seconds.
3. Wait a few seconds…

### What you should see 📊

A bar chart with two bars — one for **0** and one for **1**. After **1024 shots** (the default number of times the circuit runs), you'll see roughly **~512 zeros and ~512 ones**. Close to perfect 50/50.

> 🎲 Every time you re-run it, you get a slightly different split — because quantum randomness is *real*. It's not a trick or a pseudo-random algorithm. Nature decides each shot.

**Congrats — you just ran a real quantum experiment!** 🥳

---

## Step 5 — What's Actually Happening? 🤔

| Classical bit | Qubit |
|---|---|
| Always 0 or 1 | Can be 0, 1, or *both at once* (superposition) |
| Randomness = software algorithm | Randomness = fundamental physics |
| Copied easily | Can't be perfectly copied (no-cloning theorem) |

When you added the H gate, you pushed the qubit into superposition. When you measured it, quantum mechanics "collapsed" that superposition into a single value — 0 or 1 — chosen by nature.

This is the same principle behind:
- 🔐 **Truly random encryption keys** (way harder to hack than software randomness)
- 💊 **Simulating molecules** for drug discovery
- 🔍 **Finding patterns** in massive datasets faster than any classical computer

You've just touched the basic building block of all of that. Not bad for 10 minutes. 😎

---

## 🧪 Want to Try the Other Experiments?

### Experiment 2 — Schrödinger's Qubit 🐱

Remove the Measure gate and switch to the **Statevector** visualisation in Composer. You'll see the qubit displayed as a vector pointing diagonally — visually representing *both* 0 and 1 at the same time.

> 🧠 This is the famous Schrödinger's cat thought experiment made real: the qubit is in two states simultaneously until you observe it (measure it), at which point it picks one.

---
---
## Experiment 3 - 

2. Click **New circuit**.
3. Make sure you have **3 qubits** (`q[0]`, `q[1]`, `q[2]`) and **3 classical bits** (`c[0]`, `c[1]`, `c[2]`).  
   Use the ➕ button on the left panel to add wires if needed.

### 2 · Prepare the state to teleport (Step 1)
- Drag an **H gate** onto `q[0]`.  
  This puts `q[0]` into the `|+⟩` superposition — the state Alice wants to send to Bob.

### 3 · Create the Bell pair (Step 2)
- Drag an **H gate** onto `q[1]`.
- Drag a **CNOT gate** with **control on `q[1]`** and **target on `q[2]`**.  
  (`q[1]` and `q[2]` are now entangled — this is the shared resource between Alice and Bob.)

### 4 · Bell measurement — Alice's side (Step 3)
- Drag a **CNOT gate** with **control on `q[0]`** and **target on `q[1]`**.
- Drag an **H gate** onto `q[0]`.
- Drag a **Measure** block onto `q[0]` → wire it to classical bit `c[0]`.
- Drag a **Measure** block onto `q[1]` → wire it to classical bit `c[1]`.

### 5 · Classical feed-forward corrections — Bob's side (Step 4)
Composer supports **if-conditions** (the double-line wire):

1. Drag an **X gate** onto `q[2]`.  
   Click the gate → open its properties panel → enable **Condition** → set it to `c[1] == 1`.
2. Drag a **Z gate** onto `q[2]` (after the X).  
   Same steps: enable **Condition** → set it to `c[0] == 1`.

> **Tip:** In Composer the conditional wire is shown as a double horizontal line running from the classical register up to the gate. If you don't see it, zoom in — it is thin!

### 6 · Measure Bob's qubit (Step 5)
- Drag a **Measure** block onto `q[2]` → wire it to classical bit `c[2]`.

### 7 · Run and verify
1. Click **Simulate** (statevector or QASM simulator — either works).
2. In the **Probabilities** panel, look at the distribution of `c[2]` (Bob's bit).  
   You should see **~50 % `0`** and **~50 % `1`**, matching the `|+⟩` state.
3. The `c[0]` and `c[1]` columns will be equally spread across `00 01 10 11` — this is expected.

### Quick reference — gate mapping

| Qiskit code | Composer gate name |
|---|---|
| `qc.h(q)` | **H** (Hadamard) |
| `qc.cx(ctrl, tgt)` | **CX / CNOT** (drag control dot onto ctrl wire, ⊕ onto target) |
| `qc.x(q)` | **X** (Pauli-X / NOT) |
| `qc.z(q)` | **Z** (Pauli-Z) |
| `qc.measure(q, c)` | **Measure** (drag onto qubit wire, then click the classical bit) |
| `with qc.if_test((cr[n], 1)):` | Gate property → **Condition** toggle in Composer |

---

### Experiment 4 — Entangled Pair (Bell State) 🔗

1. Start a new circuit with **two qubits** (q[0] and q[1]).
2. Add an **H gate** to q[0].
3. Add a **CNOT gate** (controlled-NOT) with q[0] as control and q[1] as target.
4. Add measurement to both qubits.
5. Run it.

You'll only ever see **00** or **11** — never 01 or 10. The two qubits are **entangled**: once you measure one, the other instantly "knows" what to be, no matter how far apart they are.

> 🧠 Einstein called this "spooky action at a distance" — he didn't believe it was real. It is. Experiments have confirmed it many times over.

---

### Experiment 5 — Quantum NOT Gate (Great Warmup) 🔀

1. Start with a single qubit q[0] — it starts as 0.
2. Add an **X gate** (the quantum NOT gate).
3. Add measurement.
4. Run it. You'll see **100% ones** — you flipped the qubit reliably every single time.

> 🧠 The X gate is the quantum equivalent of flipping a light switch. No randomness here — it's a deterministic operation.

---

## 💻 Optional Next Step — Try It in Code with Qiskit

If dragging gates was fun, the next level is writing the same experiment in Python with **Qiskit** — IBM's open-source quantum computing library. Same circuit, now in code.

### 🪙 Coin flip in Qiskit

```python
from qiskit import QuantumCircuit
from qiskit_aer import AerSimulator

qc = QuantumCircuit(1, 1)   # 1 qubit, 1 classical bit to store the result
qc.h(0)                     # H gate → superposition!
qc.measure(0, 0)            # measure qubit 0, store result in bit 0

sim = AerSimulator()
result = sim.run(qc, shots=1024).result()
print(result.get_counts())
```

Expected output:
```
{'0': 508, '1': 516}
```

Not always exactly 50/50 — but always close. That's quantum randomness for you.

---

### 🔗 Qiskit version of the Entangled Pair

Check out the full notebook: [hello-world.ipynb](../notebooks/hello-world.ipynb)

### 📚 More Qiskit tutorials

[links-to-qiskit-tutorials.html](../notebooks/links-to-qiskit-tutorials.html)

---

### 🚀 Why Qiskit is cool

You're not learning a toy tool you'll throw away later. Qiskit is what **real researchers** use for actual quantum experiments. The circuit you wrote above is structurally identical to circuits running on IBM's quantum hardware right now.

### Running on real IBM Quantum hardware 🖥️

```python
from qiskit import QuantumCircuit
from qiskit_ibm_runtime import QiskitRuntimeService, SamplerV2 as Sampler

qc = QuantumCircuit(1)
qc.h(0)
qc.measure_all()

service = QiskitRuntimeService()                              # connects to your IBM account
backend = service.least_busy(operational=True, simulator=False)  # finds a free real machine
sampler = Sampler(mode=backend)
job = sampler.run([qc], shots=1024)
result = job.result()
print(result)
```

This code:
1. 🔌 Connects to your IBM Quantum account
2. 🤖 Finds a real quantum machine that's online and not too busy
3. 📤 Sends your circuit to that machine
4. 📥 Returns the results to your screen

From **one Python file** to **running on real quantum hardware**. That's it.

---

### 🎮 Mini Challenges

Try these tiny tweaks once the coin flip works:

- Run the same circuit with **100 shots** instead of 1024 — does it get less accurate?
- Replace the `H` gate with an `X` gate — what do you expect? What do you get?
- Build a **2-qubit Bell State** (Experiment 4) in code
- Run once on the simulator and once on real hardware — spot the difference!

> 💡 Easiest way to code without installing anything: use **IBM Quantum Lab** — a full Jupyter notebook environment in your browser.

---

## 🌍 Where to Go Next

| Resource | Link | What it is |
|---|---|---|
| IBM Quantum Learning | [learning.quantum.ibm.com](https://learning.quantum.ibm.com) | Free courses, beginner → advanced 📘 |
| Qiskit Learn | [qiskit.org/learn](https://qiskit.org/learn) | Interactive lessons with code 💻 |
| IBM Quantum Challenges | (check IBM Quantum site) | Online events — solve puzzles, earn badges 🏅 |

---

*Congrats, You got this! ⚛️*
