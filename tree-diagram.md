```mermaid
flowchart TD

START[Start: Reflect on your day]

Q1[Q1: How was your day?]
Q2[Q2: Reaction to challenges?]
Q1B[Q1B: Where did your attention go?]

D1{Locus of Control}

A1_INT[Internal Reflection]
A1_EXT[External Reflection]

A1_CHECK{Day Type Check}

A1_INT_STRONG[Strong Internal Reflection]
A1_INT_MODERATE[Moderate Internal Reflection]
A1_EXT_STRONG[Strong External Reflection]

BRIDGE1[Bridge to Axis 2]

Q3[Q3: Contribution vs Entitlement]
D2{Orientation}

A2_CONTR[Contribution Reflection]
A2_ENT[Entitlement Reflection]

BRIDGE2[Bridge to Axis 3]

Q5[Q5: Primary Concern]
SUMMARY[Final Reflection Summary]

START --> Q1
Q1 --> Q2
Q2 --> Q1B
Q1B --> D1

D1 -->|Internal| A1_INT
D1 -->|External| A1_EXT

A1_INT --> A1_CHECK
A1_EXT --> A1_CHECK

A1_CHECK --> A1_INT_STRONG
A1_CHECK --> A1_INT_MODERATE
A1_CHECK --> A1_EXT_STRONG

A1_INT_STRONG --> BRIDGE1
A1_INT_MODERATE --> BRIDGE1
A1_EXT_STRONG --> BRIDGE1

BRIDGE1 --> Q3
Q3 --> D2

D2 -->|Contribution| A2_CONTR
D2 -->|Entitlement| A2_ENT

A2_CONTR --> BRIDGE2
A2_ENT --> BRIDGE2

BRIDGE2 --> Q5
Q5 --> SUMMARY
