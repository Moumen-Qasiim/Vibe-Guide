### Project 1: Student Task Tracker (Website)

**The Concept:** A standard ASP.NET Core MVC web application to manage homework assignments and deadlines.

**The Requirements (For the Coder Prompt):**

* Create a `Task` model containing a Title, DueDate, and IsComplete boolean.
* Create a web page displaying a list of all tasks.
* Add a form to submit a new task.
* Add a button/action to mark a task as complete.
* Use ASP.NET Core MVC with .NET 10.

**The Pipeline Execution:**

* **1. Coder:** Feed the requirements above to the Coder agent to generate the initial MVC implementation.
* **2. The Reviewer Target:** The Reviewer must strictly search for "Fat Controllers." It must flag any database context calls (`_context.Tasks.Add()`) or business logic happening directly inside the Controller, forcing the student to move it to a dedicated Service layer.
* **3. Tester:** Write xUnit tests specifically for the Controller, mocking the Service layer to ensure the Controller only handles HTTP routing and View rendering.
* **4. Documenter:** Generate a Markdown wiki documenting the URL routes, expected payload models, and the Razor View directory structure.

---

### Project 2: Wordle Clone State Engine (Game API)

**The Concept:** A backend API that manages the state of a 5-letter word guessing game.

**The Requirements (For the Coder Prompt):**

* Create a .NET 10 Web API endpoint to start a new game (randomly selects a hidden 5-letter word).
* Create an endpoint to submit a 5-letter guess.
* Return a JSON array indicating if each letter in the guess is Correct, Misplaced, or Wrong compared to the hidden word.
* Track the number of attempts and return a "Game Over" state after 6 tries.

**The Pipeline Execution:**

* **1. Coder:** Feed the requirements above to the Coder agent.
* **2. The Reviewer Target:** The Reviewer must check that the Controller holds absolutely zero game logic. The letter-matching algorithm must be encapsulated entirely within a `GameSession` model or a specific domain service.
* **3. Tester:** Write unit tests covering the letter-matching algorithm edge cases (e.g., handling duplicate letters in the guess vs. the target word).
* **4. Documenter:** Generate an OpenAPI/Swagger XML documentation block for the API endpoints, explaining exactly how a frontend game client should send guesses.

---

### Project 3: Expense Tracker (Mobile Backend)

**The Concept:** A REST API built to serve a mobile application, handling user expenses and category summaries.

**The Requirements (For the Coder Prompt):**

* Create a .NET 10 Web API with an endpoint to POST a new expense (Amount, Category, Date).
* Create an endpoint to GET a summary of expenses grouped by category (e.g., Food, Transport).
* Ensure the application validates that the expense amount cannot be negative and the category cannot be empty.

**The Pipeline Execution:**

* **1. Coder:** Feed the requirements above to the Coder agent.
* **2. The Reviewer Target:** The Reviewer must aggressively check for proper HTTP status codes and parameter validation. If the mobile app sends a negative expense amount, the Controller must return a `400 Bad Request`, not crash with a `500 Internal Server Error`.
* **3. Tester:** Write integration tests verifying that invalid JSON payloads from the mobile client are correctly rejected by the MVC model binding state (`ModelState.IsValid`).
* **4. Documenter:** Generate a strict API Contract (Markdown) that the mobile developers can read to understand the exact JSON structure they need to send and expect to receive.
