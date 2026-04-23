| **Category**     | **Immutable (Fixed/Read-only)** | **Mutable (Flexible/Changeable)** | **Logic Difference**                                  |
| ---------------- | ------------------------------- | --------------------------------- | ----------------------------------------------------- |
| **Variables**    | `let x = 5;`                    | `let mut x = 5;`                  | `mut` allows re-assignment.                           |
| **Lists**        | `let v: &[i32]` (Slice)         | `let mut v: Vec<i32>`             | Vectors can grow; Slices are fixed "views."           |
| **Text**         | `let s: &str = "Hi";`           | `let mut s: String = ...`         | `String` can be edited; `&str` is static.             |
| **Dioxus State** | `signal.read()`                 | `signal.write()`                  | `.write()` triggers a UI re-render.                   |
| **References**   | `&data`                         | `&mut data`                       | `&mut` allows a function to edit the original data.   |
| **Ownership**    | `let a = b;`                    | `let mut a = b.clone();`          | Use `.clone()` if you need a separate, editable copy. |
