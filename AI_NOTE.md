# Note on AI-Assisted Development

## Tools I Used

I used **Claude (claude.ai)** during this project, mainly when I got stuck or wasn't sure about syntax. I wouldn't say it built the project for me — I had to understand what I wanted first, then use it to help me figure out specific parts I wasn't confident about.

The two main areas where Claude helped were:

1. **The email validation regex** — I knew I needed to check if an email "looks valid" but I didn't remember the exact regex pattern off the top of my head. I asked Claude to explain how regex works for email, and it walked me through `/^[^\s@]+@[^\s@]+\.[^\s@]+$/`. I now understand what each part means.

2. **localStorage with objects** — I initially tried storing the customer object directly and kept getting `[object Object]` back when I retrieved it. Claude told me I needed `JSON.stringify()` when saving and `JSON.parse()` when reading. That was a small but important fix.

Everything else — the form structure, the tier logic, the points formula, the validation checks — I wrote myself and tested manually by registering dummy customers.

## Challenges I Faced

The trickiest part was keeping the dropdown in sync with the table. When I added a new customer, the table updated fine but the dropdown in the "Add Points" form still showed old data. I had to figure out that I needed to call `refreshDropdown()` every time I registered a customer or added points — not just once on page load. I solved this by tracing through the code step by step and checking where the data was being updated vs where the UI was being rebuilt.

Another small issue: I used `var` throughout instead of `let`/`const` because that's what I'm more comfortable with from my JavaScript basics. It works the same for this use case.
