# Teacher Note — IBM Quantum Novice Activity

> **Activity:** Students run a one-gate quantum coin-flip circuit on IBM Quantum Composer.
> **Suggested time:** 10–15 minutes hands-on, plus 5 minutes for discussion.
> **Level:** Novice, no prior quantum or coding knowledge needed.

---

## What Students Will Do

Students create a free IBM Quantum account, open the Composer drag-and-drop circuit builder, place one gate (the H gate) onto a single qubit, run the circuit on a simulator, and observe a near-50/50 random result. The entire path is browser-based with no software installation.

---

## Before the Session — Setup Checklist

- [ ] Confirm students have internet access and a browser (Chrome or Firefox recommended)
- [ ] Decide whether students will use personal email accounts or a shared school account for IBM Quantum
- [ ] If using a shared account, log in ahead of time and have Composer open on screen to save signup time
- [ ] Print or share the **student quick-start sheet** (`quantum-quickstart-student.md`) so students have the steps in hand
- [ ] Open the main tutorial (`quantum-tutorial-novice.md`) on your display for reference during the activity

---

## Suggested Timing

| Time | Activity |
|---|---|
| 0–2 min | Brief intro: "Today you're going to run a real quantum experiment" |
| 2–4 min | Students create IBM Quantum accounts (or you log in a shared one) |
| 4–7 min | Students open Composer and place the H gate |
| 7–9 min | Students run the circuit and look at results |
| 9–12 min | Class discussion (see talking points below) |
| 12–15 min | Optional: students try a second experiment from the ranked list |

---

## Link to materials

- 01 - Quantum Coin Flip: bottom of student-note.md 
- 02 - Schrodinger Qbit: ep3_Hello_World.ipynb in 2q-dim
- 03 - Quantum Teleportation: src/ with teacher. 
- 04 - Bell State Entanglement: ep3_Hello_World.ipynb
- 05 - Quantum Not Gate: src/ with teacher. 
- [BONUS] 06 - Matrix multiplication: src/ with teacher


---

## Talking Points

### What makes this quantum and not just random?
A regular computer generates random numbers using a deterministic algorithm — given the same starting state, it produces the same sequence. A quantum measurement is fundamentally random; no algorithm controls it. The H gate puts the qubit into a superposition where both outcomes have exactly equal probability, and the measurement outcome is settled by physics, not math.

### What is superposition?
Tell students to imagine a coin spinning in the air — it's neither heads nor tails yet. A qubit in superposition is something like that, except it's not a metaphor: the qubit genuinely doesn't have a definite value until it's measured.

### Why does the split vary between runs?
Each "shot" is an independent quantum measurement. With 1024 shots (the default), you'd expect roughly 512 zeros and 512 ones, but natural variation means you'll usually see something like 498/526. If a student gets 1024 zeros, something is wrong with the circuit (the H gate may be missing). This is a good debugging discussion.

### What else can quantum computers do?
Keep this brief and high-level: simulating molecules for drug discovery, optimising logistics routes, and generating secure random numbers for encryption.
---

## Frequently Asked Questions

**"Why do I need an account just to try it?"**
IBM Quantum's hardware is real and expensive. The free tier gives access to simulators instantly and real hardware via a queue.

**"Can I run this on real hardware instead of the simulator?"**
Yes — in Composer, students can choose a real backend from the Run menu. Results will be similar but may take longer (queue times vary from seconds to minutes). The simulator is faster and gives the same educational result.

**"What does the H stand for?"**
Hadamard — named after mathematician Jacques Hadamard. The gate is defined by its matrix, but students don't need that detail for this activity.

**"Is quantum computing the same as AI?"**
No. They're separate fields. AI runs on classical computers using statistics and data. Quantum computing uses quantum physics to process certain kinds of problems differently. They can potentially work together, but they're not the same thing.

---

## Extension Ideas

If students finish early or want to go deeper, direct them to the ranked experiment list in the main tutorial (`quantum-tutorial-novice.md`):

- **Bell State (Entanglement)** — add a second qubit and a CNOT gate; observe that results are always perfectly correlated
- **Quantum NOT Gate** — the simplest possible circuit; great for absolute beginners
- **IBM Quantum Learning** — [learning.quantum.ibm.com](https://learning.quantum.ibm.com) has free self-paced courses starting from zero

For students who want to try coding, the main tutorial includes an optional Python/Qiskit section, a browser-based IBM Quantum Lab path, and a simple example of sending a circuit to real IBM Quantum hardware.

## Optional Qiskit follow-on

If you want a fast extension after the no-code Composer activity, show students the Qiskit section at the end of the main tutorial. The key teaching point is that the workflow stays simple:

1. build a circuit
2. add a gate
3. measure it
4. run it on a simulator or real hardware

This is a nice bridge from drag-and-drop thinking to code thinking. It also helps students see that quantum hardware access is not some mysterious expert-only step — with Qiskit, it can be just a few extra lines.

---

## Notes on IBM Quantum Account Access

- Free tier accounts have access to simulators with no queue and limited real-device jobs
- No credit card is required
- If students are under 13, check your school's acceptable-use policy before creating individual accounts; a teacher-managed shared account is a safe alternative
- IBM Quantum's privacy policy is at [ibm.com/legal/privacy](https://www.ibm.com/legal/privacy)

---
