_Sumaya Uddin_<br>
_Professor Amartya Sen_<br>
_CSI 3150 - Web and Mobile Systems_<br>
_September 20, 2026_<br>

# Assignment 1A - DevPulse UI Architecture

### **_1. User Journey Funnel_**

#### User Stories:

- **Story 1 (Value Proposition & Sticky Navigation)**: `As an infrastructure engineer
landing on DevPulse, I want to review core value metrics, access landmark navigation
links, and see a high-contrast "Deploy Free Cluster" CTA above the fold.`

- **Story 2 (Infrastructure Feature Grid)**: `As a DevOps lead, I want to scan key platform
capabilities (Latency Tracking, Log Aggregation, Auto-Remediation) in a structured
content layout.`

- **Story 3 (Compute Tier Comparison)**: `As an engineering manager, I want to compare
three cluster hosting tiers ("Developer", "Pro Cluster", "Enterprise Dedicated") with an
elevated visual badge on the most popular plan.`

- **Story 4 (Workload Estimation Form)**: `As a systems architect, I want to enter our node
count and log throughput requirements into a form with numeric bounds to verify tier
compatibility.`

- **Story 5 (API Provisioning Lead Capture)**: `As a developer, I want to submit a
pre-registration form with required fields to receive API sandbox provisioning details.`

#### Less Than Equal 4 Click User Journey Funnel:

1.

---

### **_2. Don Norman Usability & Constraint Audit_**

| Norman Principle           | UI Component / Feature Context         | Specific HTML Element or Attribute Used to Enforce Principle |
| :------------------------- | :------------------------------------- | :----------------------------------------------------------- |
| Signifier                  | Primary Action Button (Above the Fold) |                                                              |
| Signifier                  | Recommended Tier Indicator             |                                                              |
| Physical/System Constraint | Workload Estimator: Node Count         |                                                              |
| Physical/System Constraint | Operator Contact Field                 |                                                              |
| Feedback Loop              | Form Submission / Live Anchors         |                                                              |

---

### **_3. Semantic Component & Working Tree_**

```
index.html
    <head>
    <body>
        <header>
            <span>
            <nav>
            <a>
        <main>
            <div>
                <h1>
            <section>
                <article>
            <section>
            <section>
        <footer>
```

---
