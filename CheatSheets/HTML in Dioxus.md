
| **HTML Element**       | **Dioxus (RSX) Syntax**        | **Notes**                                                        |
| ---------------------- | ------------------------------ | ---------------------------------------------------------------- |
| `<div id="app"></div>` | `div { id: "app" }`            | Attributes use `:` instead of `=`                                |
| `<button class="btn">` | `button { class: "btn" }`      | `class` is a reserved keyword in Rust, but Dioxus allows it here |
| `<input type="text">`  | `input { r#type: "text" }`     | Use `r#type` if you want the raw keyword, or just `type: "text"` |
| `<img src="logo.png">` | `img { src: "logo.png" }`      | Self-closing tags don't exist; use `{}`                          |
| `onclick="fn()"`       | `onclick: move                 | _                                                                |
| ``                     | `// Comment`                   | Standard Rust comments work                                      |
|                        | h1 { "Title" }                 |                                                                  |
|                        | p { "Paragraph" }              |                                                                  |
|                        | span { "I am inside the div" } |                                                                  |
|                        | ul { li { "Item 1" } }         |                                                                  |
|                        | li { "Item 1" }                |                                                                  |
|                        | [[Event Handlers]]      |                                                                  |
