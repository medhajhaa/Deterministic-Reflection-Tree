# Reflection Tree Design Write-up

## 1. Overview

This project implements a **Deterministic Reflection Tree** designed to guide users through structured self-reflection. The system uses fixed questions and deterministic branching logic to generate meaningful insights without relying on any runtime AI or randomness.

The tree progresses through three psychological axes:
1. **Locus of Control** (Internal vs External)
2. **Orientation** (Contribution vs Entitlement)
3. **Radius of Concern** (Self vs Others)

---

## 2. Design Approach

The goal was to design a reflection flow that feels natural, structured, and psychologically grounded.

### Key decisions:
- Use **fixed multiple-choice questions** instead of free-text input
- Ensure **deterministic branching** (same inputs → same outputs)
- Maintain a **progressive flow** across axes instead of isolated questions
- Include **reflection nodes** to provide insights at each stage

---

## 3. Tree Structure

The tree is implemented as a structured `.tsv` file with the following node types:

- **Start node** – introduces reflection
- **Question nodes** – collect user input
- **Decision nodes** – determine branching based on answers
- **Reflection nodes** – provide insight and interpretation
- **Bridge nodes** – transition between axes
- **Summary node** – final reflection output

Each node includes:
- `id`
- `parentId`
- `type`
- `text`
- `options` (for questions)
- `target/signal` (for decisions)

---

## 4. Axis Design

### Axis 1: Locus of Control
Focus: Whether the user attributes outcomes to internal or external factors.

- Questions explore reactions to challenges and attention focus
- Branching categorizes responses into:
  - Internal orientation
  - External orientation
- Reflection emphasizes awareness and agency

---

### Axis 2: Contribution vs Entitlement
Focus: Whether the user leans toward contributing or expecting from others.

- Questions assess behavior in shared responsibilities
- Branching distinguishes:
  - Contribution mindset
  - Entitlement mindset
- Reflection encourages ownership and proactive behavior

---

### Axis 3: Radius of Concern
Focus: Whether the user thinks only about themselves or considers others.

- Questions explore priorities and concerns
- Branching identifies:
  - Self-centric thinking
  - Broader, outward thinking
- Reflection promotes perspective expansion

---

## 5. Branching Logic

- All branching is **deterministic**
- Each answer maps to a predefined signal
- Decision nodes route to specific reflection paths
- No randomness or dynamic interpretation is used

This ensures:
- Consistency
- Predictability
- Easy reproducibility

---

## 6. Design Trade-offs

### Simplicity vs Depth
- Kept the tree structured and readable
- Avoided overly complex branching to maintain clarity

### Fixed Options vs Flexibility
- Fixed options ensure deterministic behavior
- Trade-off: less personalization compared to open-ended input

### Clarity vs Coverage
- Focused on key psychological axes instead of covering too many dimensions

---

## 7. Psychological Basis

The design is inspired by established concepts:

- **Locus of Control** (Rotter)
- **Organizational Citizenship Behavior** (Organ)
- **Psychological Entitlement** (Campbell et al.)
- **Self-Transcendence** (Maslow)
- **Perspective-Taking**

The questions are designed to surface these patterns indirectly without being leading or judgmental.

---

## 8. What Could Be Improved

With more time, the following enhancements could be added:

- More nuanced branching within each axis
- Stronger personalization in reflection text
- Expanded summary combining signals across axes
- A runnable CLI/Web agent to execute the tree

---

## 9. Conclusion

This reflection tree demonstrates how structured questioning and deterministic logic can guide meaningful self-reflection. The design balances psychological depth with implementation simplicity, making it suitable for integration into lightweight systems.
