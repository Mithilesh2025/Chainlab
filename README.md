# CHAINLAB — Interactive Backward Chaining Explainer

An interactive, browser-based learning tool that demonstrates **backward chaining**, a goal-driven reasoning technique used in Artificial Intelligence and expert systems.

**Project:** Foundations of AI (26AI601)  
**Version:** 3.0  
**Created by:** Mithilesh R  
**Technology:** HTML, CSS, JavaScript

## Overview

Backward chaining starts with a goal (a conclusion we want to establish) and works backward through **IF–THEN rules** until it reaches known facts. When a required premise cannot be proven, the engine backtracks and tries an alternative supporting rule. CHAINLAB makes this reasoning process visual and interactive.

## Features

- **Step-by-step backward chaining** — advance, go back, play automatically, reset, or jump to the final result.
- **Interactive AND/OR proof tree** — see goals, inference rules, subgoals, known facts, successful branches and failed alternatives.
- **Instant proof answer** — see whether a goal can be established from the knowledge base, with a short explanation.
- **Guided learning** — introductory theory, algorithm walkthrough, and an interactive teaching example.
- **Custom knowledge-base editor** — enter facts, IF–THEN rules and a goal; run the engine on your own problem.
- **Execution history and quiz mode** — inspect reasoning stages and predict proof outcomes.
- **Three themes** — Orchid Dusk, Neon Forest (black, neon green and cyan), and Solar Paper (ivory, sandalwood and yellow).
- **Independent Motion and Effects controls** — configure scroll/page motion separately from proof/decorative effects.
- **Responsive interface** — runs on desktop and mobile browsers.

## Try the examples

| Scenario | Learning focus |
| --- | --- |
| Campus lab access | A goal that can be proven by combining facts and supporting rules |
| Museum entry | A goal that cannot be established because the knowledge base lacks required evidence |
| Network connection | Multi-step reasoning through network-related rules |

For an unsuccessful proof, **not proven** means the currently supplied facts and rules do not support the conclusion; it does not automatically mean the conclusion is false.

## Run locally

1. Download this repository using **Code → Download ZIP**, or clone it:
   ```bash
   git clone https://github.com/Mithilesh2025/Chainlab.git
   ```
2. Open `index.html` in Chrome, Edge, Firefox, or another modern browser.

The website is a **self-contained HTML file**. No npm installation, build tools, backend, or API key is required.

## Website deployment (GitHub Pages)

This repository can be published as a static site with GitHub Pages:

1. Open **Settings → Pages** for this repository.
2. Under **Build and deployment**, choose **Deploy from a branch**.
3. Select branch **main**, folder **/(root)**, and save.
4. When deployment completes, GitHub will show a **Visit site** link.

Expected URL after Pages is enabled:

**https://mithilesh2025.github.io/Chainlab/**

> The address above is the expected GitHub Pages URL. Availability depends on GitHub Pages being enabled and the deployment succeeding.

## How to understand the visualizer

1. Choose an example and a **goal** to prove.
2. Watch the **instant result** or predict it using Quiz Mode.
3. Select **Step-by-step** and press **Next** to see which rule is applied and how its premises become subgoals.
4. Observe the green proven branches and distinct failed-branch indicators.
5. Select **Complete tree** to inspect the full proof attempt.
6. Optionally open the knowledge-base editor to change facts or rules and compare results.

## Algorithm (simplified)

```text
PROVE(goal):
    if goal is a known fact:
        return TRUE

    for each rule whose conclusion is goal:
        if every premise in the rule can be proved:
            return TRUE

    return FALSE
```

The implemented engine also supports alternative rules, proof history and detection of circular reasoning paths.

## Repository structure

```text
Chainlab/
├── index.html   # Full website: markup, styles and JavaScript
├── README.md    # Project guide
└── .nojekyll    # Prevents unnecessary Jekyll processing on GitHub Pages
```

## Educational purpose

This project is designed to help learners connect the theory of backward chaining with visible inference steps, backtracking, and proof outcomes. It is intended as an educational explainer rather than a general-purpose theorem prover.

---

**CHAINLAB v3.0** · Built by **Mithilesh R** · Foundations of AI
