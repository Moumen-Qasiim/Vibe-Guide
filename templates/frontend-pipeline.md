# Web Frontend Pipeline

**CRITICAL RULE:** Clear the AI context window between each step.

## Step 1: The Coder
> Implement a new `[Component/Page/Hook Name]` for a web frontend using `[React/Vue/Angular/Svelte]`.
> Directory: `[Insert Path]`.
> Requirements:
> 1. `[Requirement 1]`
> 2. `[Requirement 2]`
> Ensure semantic HTML and adherence to `[CSS Framework/Tailwind]` styling. 
> Do not write any component tests yet. Generate the code.

---

## Step 2: The Reviewer
> Act as a strict Senior Frontend Architecture Reviewer for `[Framework]`. 
> Analyze the following file: `[Insert File Path]`. 
> Check specifically for:
> - Accessibility (a11y) violations (missing ARIA tags, poor contrast scaling).
> - Unnecessary re-renders or inefficient DOM manipulation.
> - Hydration mismatches or lack of suspense/loading states.
> - Improper client-side state mutations.
> Output only the specific code diffs required to fix any violations.
> 
> Code to review:
> `[Insert Code]`

---

## Step 3: The Tester
> The following code from `[Insert File Path]` is architecturally verified. 
> Act as a Frontend QA Automation Engineer. 
> Write isolated component tests using `[Testing Framework, e.g., Jest, Vitest, React Testing Library]`. 
> Mock API responses and routing, and ensure user interactions (clicks, inputs) are asserted. 
> Save this in `[Tests Directory Path]`.
> 
> Verified Code:
> `[Insert Verified Code]`
