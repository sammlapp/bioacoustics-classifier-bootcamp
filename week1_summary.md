# Lecture Outline: Intro to Bioacoustic ML Classifier Development

**Session length:** ~75 minutes

---

## Course Goals & Framing
- Build intuition about how **ML classifiers** work in bioacoustics.  
- Learn to:
  - Build and evaluate classifiers.  
  - Understand common pitfalls (data mismatch, small datasets, inherent limits).  
  - Judge when a model is **ready for real-world application**.  

---

## Course Structure & Participation
- Weekly **75-minute meetings**.  
- Assignments between sessions (flexible workload).  
- Participation not dependent on completing every task.  
- Strategies for catching up if behind.  

---

## The Annotation Bottleneck
- **Labeling data** (e.g., box annotations) is the biggest time sink.  
- Strategies:
  - Continue annotating while training with **partial data**.  
  - Emphasis on **annotation planning** from the start.  

---

## Collaboration & Reproducibility
- Work together on debugging and sharing approaches.  
- Use **shared GitHub repositories**:
  - Include example notebooks and scripts at each step.  
  - Build a **public collection** of worked examples for future students.  
- Best practices:
  - `.gitignore` to exclude large/sensitive files.  
  - Private repos allowed, but no stigma around messy code.  

---

## Technical Setup
- **Main tools**:
  - VS Code (Python integration, debugging, Git/GitHub, AI-assisted coding).  
  - Conda environments (reproducible package management).  
  - OpenSoundscape ≥ v0.12.  
- **Setup steps**:
  - Install Anaconda / Miniconda.  
  - Create & activate environments.  
  - Export environments (`.yml`) for reproducibility.  

---

## GitHub Workflow Basics
- Git concepts:
  - Commits, pushes, pulls.  
  - Branching as optional, but not required.  
- Workflow practice:
  - `git init` / `git clone`  
  - Making commits  
  - Pulling updates from others  
- VS Code integration with GitHub.  

---

## Discussion: LLMs, AI, and Coding with AI

### Overview
- LLMs (e.g., ChatGPT, Claude, Copilot) can accelerate science but also introduce risks.
- Key tension: **useful accelerators vs. obfuscating errors**.
- Important to consider the **mode/level** of LLM use for coding.

---

### Levels of LLM Use in Coding

1. **Level 1 – Minimal assistance**
   - Completing half a line of code (syntax help).
   - Asking how to use a specific function.
   - Debugging a specific error message.
   - Example: *“How to compute average size per category in a pandas DataFrame?”*
   - Benefits: fast, precise, great learning tool (ask for line-by-line explanations).
   - Caveat: Works well in Python, less reliable in other languages (e.g., R).

2. **Level 2 – Multi-line autocomplete**
   - VS Code/Copilot autocompletes multiple lines at once.
   - Pros: Fast, syntax-error-free, accelerates code writing.
   - Cons: May implement logic differently than intended, leading to subtle errors.
   - Efficiency of generated code often poor.

3. **Level 3 – Full script generation**
   - Ask LLM to write entire scripts (10–100+ lines).
   - Pros: Speed, suggests useful architecture and packages, may work out of the box.
   - Cons: Higher risk of **logic errors** (runs but does wrong thing).
   - Example: revising a script to handle different coordinate systems.

4. **Level 4 – Agentic / “vibe” coding**
   - LLM integrated into coding environment (e.g., Claude Code).
   - Capabilities:
     - Create/edit multiple files.
     - Run code, observe outputs/errors, iteratively fix.
     - Engage interactively: “Here’s what I did, what’s next?”
   - Pros: Extremely powerful for rapid prototyping of large projects.
   - Cons:
     - Verbose, overly complex code.
     - May use unfamiliar packages/languages.
     - Hard to debug and understand.
     - Attribution/ownership questions (e.g., GitHub commits tagged with Claude).

---

### Strategic Use
- **For critical workflows** (e.g., analysis pipelines with specific requirements):
  - Stick to Level 1 and maybe Level 2.
  - Retain full control and understanding.
- **For exploratory or low-stakes tasks** (e.g., making a figure):
  - Levels 3–4 can be valuable.
  - Focus on whether the **output looks correct**, not necessarily on each line of code.

---

### Attribution
- GitHub may automatically list LLMs (e.g., Claude) as co-authors on commits.
- Open question: what counts as authorship when prompts generate large codebases?
- Current state: LLMs not eligible as journal authors, but may appear in GitHub commit history.

---


## Today’s Agenda & Wrap-Up
- Main focus: **environment setup**.  
- Walkthrough:
  - VS Code vs Jupyter notebooks.  
  - Conda workflows.  
  - GitHub for code sharing.  
- Expect some **debugging issues** (e.g., package install, VS Code config).  
- Confirm working environment for next session.  
