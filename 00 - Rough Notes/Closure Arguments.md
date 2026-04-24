closure arguments in general are what builds the other house.
In other words, it is what makes the stored data from variable be processed by the [[Event Handlers]] with the help of [[move]] which takes ownership of that data first.




```rust
oninput : move |event| {
	task.set(event.value());
},
```

[[Event Handlers]] : [[move]] | [[closure parameters]] | {
	//code
}

```
[[Event Handlers]] : [[move]] | [[closure parameters]] | {
	//code
}
```