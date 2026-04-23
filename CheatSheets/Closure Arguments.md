closure arguments in general are what builds the other house.
In other words, it is what makes the stored data from variable be processed by the [[Dioxus Event Handlers]] with the help of [[move]] which takes ownership of that data first.

- **`|_|`**: "Just do the thing."
    
- [[evt]]: "Give me the details (text, coordinates, keys)."
    
- [[move]]: "Make sure this closure owns the data so it doesn't crash later."


Fn (Immutable Borrow): Takes parameters by immutable reference. Used when the closure only reads captured data.
FnMut (Mutable Borrow): Takes parameters by mutable reference. Used when the closure modifies captured data.
FnOnce (Ownership): Consumes the captured variables. Used when the closure is called only once. 

[[Ownership]]