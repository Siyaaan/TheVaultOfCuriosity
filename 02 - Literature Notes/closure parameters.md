closure parameters is a tiny version of a function(). It is used to modify a data from a variable to another instantly. "||" (pipe) is same as "()" (parenthesis) which takes a parameter. Function communicate with another function while closure parameters communicate variables from other variable.

## Example

```
// 🏗️ THE CLOSURE PARAMETER CHEAT SHEET
// Goal: Define how "Source Material" enters your "Permanent Logic"

// 1. EMPTY: No external data needed. Self-contained logic.
// Borrow:
let _ = || { ... };
// Owned (+ move):
let _ = move || { ... };

// 2. INFERRED: Take the whole source. Rust determines the type (e.g., FormEvent).
let _ = |val| { ... };

// 3. EXPLICIT: Strict filtering. Only allow a specific type.
let _ = |val: i32| { ... };

// 4. IGNORED: Acknowledge the data exists, but choose not to "file" it.
// Highly common in Dioxus for onclick: move |_| { ... }
let _ = |_| { ... };

// 5. REFERENCE: Just "glancing" at the note without taking ownership.
let _ = |ref val| { ... };

// 6. MUTABLE: Permission to "edit" the incoming data immediately.
let _ = |mut val| { ... };

// 7. DESTRUCTURED: "Atomization." Breaking a complex source into parts instantly.
let _ = |(a, b)| { ... };

// 8. Used to represent ui interactions
let _ = |event| { ... };
```

