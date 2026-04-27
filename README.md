# Deterministic Reflection Tree

A structured system for guiding users through daily self-reflection using a deterministic decision tree.

---

##  Overview

This project models reflection as a **tree of questions, decisions, and outputs**.

- Users answer fixed multiple-choice questions
- Each answer leads to a predefined path
- The system produces a consistent reflection outcome

 Same input → same output (no randomness, no AI at runtime)

---

##  Core Design

The reflection is built across three psychological axes:

### 1. Locus of Control
- Internal → Focus on what I can control
- External → Focus on external factors

### 2. Contribution vs Entitlement
- Contribution → What I gave
- Entitlement → What I expected

### 3. Radius of Concern
- Self → Personal focus
- Others → Broader impact

These axes are processed sequentially to build deeper reflection.

---

##  How It Works

1. User starts reflection
2. Answers structured questions
3. Decision nodes route responses
4. Reflection nodes provide insights
5. Final summary combines all signals

Flow:
```
START → Axis 1 → Axis 2 → Axis 3 → SUMMARY
```

---

## Project Structure

```
Deterministic-Reflection-Tree/
│
├── tree/
│   ├── reflection-tree.tsv     # Tree data (main deliverable)
│   ├── tree-diagram.md         # Visual diagram (Mermaid)
│
├── write-up.md                 # Design rationale
├── reflection-tree-design.docx # Optional extended document(brief)
└── README.md                   # Project overview
```

---

## Tree Data Format

The tree is stored in a TSV file with the following columns:

- `id` → Node identifier  
- `parentId` → Parent node  
- `type` → start / question / decision / reflection / bridge  
- `text` → Content shown to user  
- `options` → Answer choices  
- `target` → Next node (for transitions)  
- `signal` → Logic for branching  

---

## Deterministic Behavior

- No randomness  
- No free-text input  
- No API or AI usage  
- Fully predefined paths  

Ensures consistency and reproducibility

---

##  Diagram

The tree structure is visualized using Mermaid.

To view:
- Open `tree/tree-diagram.md` on GitHub  
- Or paste into https://mermaid.live  

---

##  Design Highlights

- Clear and structured question flow  
- Meaningful behavioral distinctions  
- Progressive multi-axis reflection  
- Balanced simplicity and depth  

---

##  Future Improvements

- More nuanced branching logic  
- Enhanced summary generation  
- web-based implementation  
- Tracking reflection over time  

---

##  Author

Medha Jha
