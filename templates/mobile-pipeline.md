# Mobile Development Pipeline

**CRITICAL RULE:** Clear the AI context window between each step.

## Step 1: The Coder
> Implement a new `[Screen/Component/Service Name]` for a mobile application using `[Flutter/React Native/Swift/Kotlin]`.
> Directory: `[Insert Path]`.
> Requirements:
> 1. `[Requirement 1]`
> 2. `[Requirement 2]`
> Utilize standard `[State Management Pattern, e.g., Bloc, Redux, MVVM]`. Ensure responsive layout principles are followed.
> Do not write any unit or widget tests yet. Generate the implementation.

---

## Step 2: The Reviewer
> Act as a strict Senior Mobile Architecture Reviewer for `[Framework/Language]`. 
> Analyze the following file: `[Insert File Path]`. 
> Check specifically for:
> - Main UI thread blocking (heavy operations not offloaded).
> - Memory leaks or improper lifecycle management.
> - Platform-specific UI/UX guideline violations (Material/Cupertino).
> - Inefficient list rendering or state rebuilds.
> Output only the specific code diffs required to fix any violations.
> 
> Code to review:
> `[Insert Code]`

---

## Step 3: The Tester
> The following code from `[Insert File Path]` is architecturally verified. 
> Act as a QA Automation Engineer. 
> Write isolated tests using `[Standard Testing Framework, e.g., XCTest, JUnit, Flutter Test]`. 
> Cover widget/UI rendering states and mock any external API calls or hardware sensors. 
> Save this in `[Tests Directory Path]`.
> 
> Verified Code:
> `[Insert Verified Code]`
