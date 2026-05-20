# Game Development Pipeline

**CRITICAL RULE:** Clear the AI context window between each step.

## Step 1: The Coder
> Implement a new `[Script/System/Entity Name]` for a game using `[Unity/Unreal/Godot]`.
> Directory: `[Insert Path]`.
> Requirements:
> 1. `[Requirement 1]`
> 2. `[Requirement 2]`
> Follow `[ECS/OOP/Component-based]` architecture constraints.
> Do not write any tests or documentation yet. Generate the core logic.

---

## Step 2: The Reviewer
> Act as a strict Senior Engine Architecture Reviewer for `[Game Engine]`. 
> Analyze the following file: `[Insert File Path]`. 
> Check specifically for:
> - Garbage collection spikes (e.g., allocating memory inside `Update()` or `Tick()`).
> - Mixing physics calculations with rendering logic.
> - Inefficient distance checks or collision handling.
> - Hardcoded references instead of serialized fields or dependency injection.
> Output only the specific code diffs required to fix any violations.
> 
> Code to review:
> `[Insert Code]`

---

## Step 3: The Tester
> The following code from `[Insert File Path]` is architecturally verified. 
> Act as a Game QA Automation Engineer. 
> Write isolated logic tests using `[Engine Testing Framework]`. 
> Mock the engine's time/physics dependencies where possible to cover the core mechanic states. 
> Save this in `[Tests Directory Path]`.
> 
> Verified Code:
> `[Insert Verified Code]`
