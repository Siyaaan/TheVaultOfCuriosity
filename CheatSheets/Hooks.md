
1. State & Reactivity

| **Hook**                   | **Usage**                                                  | **Example**                                   |
| -------------------------- | ---------------------------------------------------------- | --------------------------------------------- |
| **`use_signal`**           | The go-to hook for reactive state.                         | `let mut val = use_signal(                    |
| **`use_memo`**             | Derived state. Only recalculates when dependencies change. | `let double = use_memo(move                   |
| **`use_context`**          | Accesses "Global" state provided by an ancestor.           | `let theme = use_context::<Signal<Theme>>();` |
| **`use_context_provider`** | Makes state available to all child components.             | `use_context_provider(                        |

2. Side Effects & Async

| **Hook**           | **Purpose**                                                           |
| ------------------ | --------------------------------------------------------------------- |
| **`use_resource`** | Used to programmatically change pages (e.g., `nav.push(Route::Home)`) |


3. Lifecycle & References

| **Hook**           | **Usage**                                                | **Example**                       |
| ------------------ | -------------------------------------------------------- | --------------------------------- |
| **`use_node_ref`** | Grabs a reference to a specific HTML element in the RSX. | `let input_ref = use_node_ref();` |
| **`use_drop`**     | Runs code when the component is unmounted (destroyed).   | `use_drop(                        |

4. Navigation (Dioxus Router)

|**Hook**|**Purpose**|
|---|---|
|**`use_navigator`**|Used to programmatically change pages (e.g., `nav.push(Route::Home)`)|
|**`use_route`**|Returns the current active route and its parameters.|