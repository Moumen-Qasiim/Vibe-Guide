# Web Backend Pipeline

**CRITICAL RULE:** Clear the AI context window between each step.

## Step 1: The Coder
> Implement a new `[Endpoint/Service/Handler Name]` for a backend using `[Node.js/Django/Go/etc.]`.
> Directory: `[Insert Path]`.
> Requirements:
> 1. `[Requirement 1]`
> 2. `[Requirement 2]`
> Follow standard REST/GraphQL practices and the system's `[Layered/Microservice]` architectural pattern. 
> Do not write any unit tests yet. Generate the implementation.

---

## Step 2: The Reviewer
> Act as a strict Senior Backend Security Reviewer for `[Language/Framework]`. 
> Analyze the following file: `[Insert File Path]`. 
> Check specifically for:
> - OWASP vulnerabilities (e.g., SQL injection, lack of input sanitization).
> - Blocking the event loop (for async environments) or threading deadlocks.
> - Missing rate limiting considerations or pagination on large queries.
> - Business logic leaking into the controller/routing layer.
> Output only the specific code diffs required to fix any violations.
> 
> Code to review:
> `[Insert Code]`

---

## Step 3: The Tester
> The following code from `[Insert File Path]` is architecturally verified. 
> Act as a Backend QA Automation Engineer. 
> Write isolated tests using `[Standard Testing Framework]`. 
> Mock the database layer and external HTTP calls. Test the happy path and all error/validation boundaries. 
> Save this in `[Tests Directory Path]`.
> 
> Verified Code:
> `[Insert Verified Code]`

---

## Step 4: The Documenter
> The implementation and tests for `[Service/Endpoint Name]` located at `[Insert Paths]` are complete, verified, and locked.
> Act as a Senior Technical Writer. 
> Generate `[Specify Artifact: e.g., an OpenAPI specification snippet / Architecture Decision Record / Markdown wiki]`.
> Base the documentation strictly on the provided code. Explain the business logic, endpoint parameters, and data models. 
> Output only the requested documentation artifacts. Do not output or modify the existing code.
>
> Verified Code & Tests:
> `[Insert Code]`
