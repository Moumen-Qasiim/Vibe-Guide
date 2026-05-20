### Project 1: Student Task Tracker (Website)

**The Concept:** A standard ASP.NET Core MVC web application to manage homework assignments and deadlines.

**The Requirements (For the Coder Prompt):**

* Create a `Task` model containing a Title, DueDate, and IsComplete boolean.
* Create a web page displaying a list of all tasks.
* Add a form to submit a new task.
* Add a button/action to mark a task as complete.
* Use ASP.NET Core MVC with .NET 10.
---

### Project 2: Wordle Clone State Engine (Game API)

**The Concept:** A backend API that manages the state of a 5-letter word guessing game.

**The Requirements (For the Coder Prompt):**

* Create a .NET 10 Web API endpoint to start a new game (randomly selects a hidden 5-letter word).
* Create an endpoint to submit a 5-letter guess.
* Return a JSON array indicating if each letter in the guess is Correct, Misplaced, or Wrong compared to the hidden word.
* Track the number of attempts and return a "Game Over" state after 6 tries.
---

### Project 3: Expense Tracker (Mobile Backend)

**The Concept:** A REST API built to serve a mobile application, handling user expenses and category summaries.

**The Requirements (For the Coder Prompt):**

* Create a .NET 10 Web API with an endpoint to POST a new expense (Amount, Category, Date).
* Create an endpoint to GET a summary of expenses grouped by category (e.g., Food, Transport).
* Ensure the application validates that the expense amount cannot be negative and the category cannot be empty.
