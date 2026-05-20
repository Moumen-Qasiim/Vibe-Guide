# Vibe Guide : Multi-Agent Vibe Coding Templates

This repository contains strict, synchronous prompt templates for executing a multi-agent "Vibe Coding" pipeline across different development domains. 

These templates enforce the **Coder ➔ Reviewer ➔ Tester ➔ Documenter** workflow.

## The Core Concept
Large Language Models (LLMs) cannot effectively review their own code in the same context window without heavy bias. To ensure robust architecture and prevent hallucinations, you must use isolated contexts.

1. **The Coder:** Generates the initial implementation based on intent.
2. **The Reviewer:** A fresh agent session that blindly reviews the code against domain-specific constraints.
3. **The Tester:** A third agent session that writes tests strictly for the verified, locked code.
4. **The Documenter:** A final agent session that generates pristine documentation artifacts from the locked codebase.

## How to Use
1. Select the template matching your development domain from the `templates/` folder.
2. Open your AI IDE (e.g., Antigravity, Cursor) or CLI agent.
3. Run **Step 1** to generate the code.
4. **CRITICAL:** Clear the chat or open a completely new agent session.
5. Run **Step 2** to review the code. Apply the diffs. Repeat until the Reviewer passes the file.
6. **CRITICAL:** Clear the chat or open a completely new agent session.
7. Run **Step 3** to generate tests for the locked file.
8. **CRITICAL:** Clear the chat or open a completely new agent session.
9. Run **Step 4** to generate documentation artifacts based strictly on the final code.
