# Note on AI-Assisted Development

## Tools I Used

I used **Claude (claude.ai)** as an AI-assisted development tool during this project. I mainly used it when I needed help understanding specific JavaScript concepts or checking parts of my approach. The project structure, feature decisions, points logic, validation flow, and final testing were completed by me.

The main areas where Claude helped were:

1. **Email validation regex**
   I knew the form needed to check whether an email address was in a valid format, but I was not fully confident writing the regex from memory. Claude helped explain the pattern `/^[^\s@]+@[^\s@]+\.[^\s@]+$/`, including what each part does. After understanding it, I used it in my validation logic.

2. **Using localStorage with objects**
   I initially tried storing customer data directly and noticed that objects were not being saved correctly. Claude helped me understand that browser localStorage only stores strings, so I needed to use `JSON.stringify()` when saving data and `JSON.parse()` when reading it back. This helped me store customer records properly between page refreshes.

3. **Comparing simple options**
   I also used Claude to think through whether I should use a database or localStorage. I chose localStorage because this is a small browser-based case study, and it keeps the project easy to run without requiring installation, backend setup, or database configuration.

## Challenges I Faced

One challenge was keeping the customer dropdown and summary table updated at the same time. At first, when I registered a new customer, the table updated correctly but the dropdown still showed old data. I solved this by tracing where the data changed and then calling the dropdown refresh function after customer registration and points updates.

Another challenge was balancing simplicity with functionality. I wanted the app to be easy to run, but still show proper validation, points calculation, bonus multipliers, stored customer records, and a clear summary. I chose plain HTML, CSS, and JavaScript because it was enough for the requirements and avoided unnecessary framework setup.

I used `var` in the JavaScript because I am comfortable with basic JavaScript syntax and wanted to keep the code consistent throughout the project. In a larger project, I would use `let` and `const` more carefully to improve scope control and code quality.

Overall, AI helped me work through specific development questions, but I made the final decisions, wrote the application flow, tested the features manually, and adjusted the code to match the case study requirements.
