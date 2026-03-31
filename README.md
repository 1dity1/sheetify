Sheetify
A lightweight spreadsheet app built from scratch using HTML, CSS, and JavaScript. You can edit cells, write formulas, style your data, and watch dependent cells update automatically — all in the browser, no installations needed.

Features
Cell Editing

Click any cell and start typing right away.
If a cell had a formula before, typing over it clears the formula and makes the cell independent.

Formulas

Write formulas like:

A1 + B1
A1 * 2
( A1 + B1 ) * 3


Cells are referenced using standard spreadsheet notation (A1, B2, etc.).
Arithmetic expressions are evaluated once cell references are substituted with their values.

Styling

Each cell can be styled independently:

Font family (e.g. Arial)
Font size
Bold, italic, underline
Horizontal alignment (left, center, right)
Text color
Background color



Dependency Tracking

Cells keep track of which other cells depend on them.
When a cell's value changes, all dependent cells recalculate automatically — including chains:

B1 = A1 + 5
C1 = B1 * 2
Change A1 → B1 updates → C1 updates.



Formula Removal

Typing directly into a cell that has a formula removes that formula.
All dependency links from parent cells are cleared automatically.


🛠️ Tech Stack

Frontend: HTML, CSS
Logic: Vanilla JavaScript (no frameworks)
Data Model: Each cell stores — text color, background color, font family, font size, alignment, bold/italic/underline states, value, formula, and a list of dependent children.


⚡ How It Works
Editing a Cell

When you leave a cell after typing:

If the value didn't change → nothing happens.
If a formula existed → it gets removed.


The new value is saved and all dependent cells update recursively.

Entering a Formula

Type a formula in the formula bar and press Enter.
Cell references are replaced with their current values and the expression is calculated.
Dependencies are registered so future changes propagate correctly.

Update Propagation

When a cell updates, it refreshes its value in both the UI and the data model.
All child cells that depend on it are then recalculated in the same way, down the chain.


⚠️ Current Limitations

Only basic arithmetic is supported: +, -, *, /, ().
No built-in functions like SUM or AVERAGE yet.
Cell ranges (like A1:A5) aren't supported.
No circular dependency detection — avoid formulas that reference each other or it'll loop.


▶️ How to Run

Clone the repository:

bash   git clone https://github.com/1dity1/sheetify.git

Open index.html in any browser.
Start typing in cells or enter formulas using the formula bar.


🔗 Links

<<<<<<< HEAD
Deployed Link: https://1dity1.github.io/sheetify/
=======
Deployed Link: https://1dity1.github.io/sheetify/
>>>>>>> 391e901489efc1ca19170844cecb2458e1aa85ca
