_Sumaya Uddin_<br>
_Professor Amartya Sen_<br>
_CSI 3150 - Web and Mobile Systems_<br>
_September 20, 2026_<br>

# Assignment 1A - DevPulse UI Architecture

### **_1. User Journey Funnel_**

#### <u>User Stories (for reference)</u>:

- **Story 1 (Value Proposition & Sticky Navigation)**: As an infrastructure engineer landing on DevPulse, I want to `review core value metrics, access landmark navigation links, and see a high-contrast "Deploy Free Cluster" CTA above the fold.`

- **Story 2 (Infrastructure Feature Grid)**: As a DevOps lead, I want to `scan key platform capabilities (Latency Tracking, Log Aggregation, Auto-Remediation) in a structured content layout.`

- **Story 3 (Compute Tier Comparison)**: As an engineering manager, I want to `compare three cluster hosting tiers ("Developer", "Pro Cluster", "Enterprise Dedicated") with an elevated visual badge on the most popular plan.`

- **Story 4 (Workload Estimation Form)**: As a systems architect, I want to `enter our node count and log throughput requirements into a form with numeric bounds to verify tier compatibility.`

- **Story 5 (API Provisioning Lead Capture)**: As a developer, I want to `submit a pre-registration form with required fields to receive API sandbox provisioning details.`

#### <u>Less Than Equal 4 Click User Journey Funnel</u>:

- **Starting State**:
  - Initial viewport upon entering the DevPulse website.
- **Action 1**:
  - User lands on the page and identifies the primary signifier: the navigation bar along with the brand logo and "Deploy Free Cluster" call-to-action [CTA] button.
- **Action 2**:
  - User scrolls down or clicks on navigation link to reach the three hosting tiers.
- **Action 3**:
  - User inspects the tiered cards where the "Pro Cluster" card is visually elevated (badge signifier).
- **Action 4**:
  - User submits log throughput and node count requirements into a number input field and clicks the primary registration CTA (Generate API Keys).
- **Terminal State**:
  - Visual confirmation upon submission of form.

---

### **_2. Don Norman Usability & Constraint Audit_**

| Norman Principle           | UI Component / Feature Context         | Specific HTML Element or Attribute Used to Enforce Principle                                                  |
| :------------------------- | :------------------------------------- | :------------------------------------------------------------------------------------------------------------ |
| Signifier                  | Primary Action Button (Above the Fold) | anchor tag: `<a></a>`                                                                                         |
| Signifier                  | Recommended Tier Indicator             | `<div class="popular-tag"><strong>Most Popular</strong></div>`                                                |
| Physical/System Constraint | Workload Estimator: Node Count         | `min`="1000" `max`="1000000"                                                                                  |
| Physical/System Constraint | Operator Contact Field                 | `required`                                                                                                    |
| Feedback Loop              | Form Submission / Live Anchors         | Once submit button is clicked, the page `refreshes`, updates URL to include `#`, and sends user to the `top`. |

---

### **_3. Semantic Component & Working Tree_**

```
body
  header
    div<logo>
    nav
      a<capabilities>
      a<comparison>
      a<compatibility>
    CTA button <Deploy Free Cluster>
  main
    section<hero>
        h1<title of page>
        p<subtitle/short text> (Core Value Metrics)
        img<>
    section<capabilities>
      header
        h2<section-title>
        p<section-subtitle>
      div<features-grid>
        article<feature-1>
          h3<feature-name> (Latency Tracking)
          p<describe feature>
          img<>
        article<feature-2>
          h3<feature-name> (Log Aggregation)
          p<describe feature>
          img<>
        article<feature-3>
          h3<feature-name> (Auto-Remediation)
          p<describe feature>
          img<>
    section<comparison>
      header
        h2<section-title>
        p<section-subtitle>
      div<tier-grid>
        article<tier-1>
          h3<tier-name> (Developer)
          p<describe tier>
          div<tier-price>
            span<tier-values>
          ul<tier-features>
            li<features-list>
          CTA Button <Deploy Developer>
        article<tier-2>
          div<popular-tag>
          h3<feature-tier> (Pro Cluster)
          p<describe tier>
          div<tier-price>
            span<tier-values>
          ul<tier-features>
            li<features-list>
          CTA Button <Join Pro Cluster>
        article<tier-3>
          h3<feature-tier> (Enterprise Dedicated)
          p<describe tier>
          div<tier-price>
            span<tier-values>
          ul<tier-features>
            li<features-list>
          CTA Button <Become Dedicated Today>
    section<registration>
      div<form-wrapper>
        header
          h2<section-title>
          p<section-subtitle>
        form<registration-form>
          div<form-group>
            label<contact-email>
            input<type="email" required>
          div<form-group>
            label<node-count>
            input<type="number" min="" max="" step="1000" required>
            span<constraints>
          div<form-group>
            label<log-throughput>
            input<type="number" min="" max="" step="1000" required>
            span<constraints>
          button<Generate API Keys>
  footer
    div<footer-container>
      div<logo>
      div<links>
        a<capabilities>
        a<comparison>
        a<compatibility>
        a<scroll to top> (Hero Section)
      CTA Button <Deploy Free Cluster>
```

---
