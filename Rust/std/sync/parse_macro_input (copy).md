## parse_macro_input

`parse_macro_input!` 是 `syn` 库中的一个宏，用于解析过程宏的输入。过程宏是一种在编译时接收 Rust 代码（例如，一个函数、结构体或者表达式）并生成新的 Rust 代码的宏。

`parse_macro_input!` 宏接收两个参数：一个是要解析的输入，另一个是期望的类型。例如，如果你想要解析一个表达式，你可以这样使用 `parse_macro_input!` 宏：

```rust
let expr = parse_macro_input!(input as syn::Expr);
```

在这个例子中，`input` 是过程宏的输入，`syn::Expr` 是期望的类型。`parse_macro_input!` 宏会尝试将输入解析为一个表达式，如果解析成功，它会返回一个 `syn::Expr` 实例。如果解析失败，它会产生一个编译错误。

`syn` 库提供了许多用于解析 Rust 代码的类型，例如 `syn::Item`（用于解析项，例如函数或结构体）、`syn::Stmt`（用于解析语句）等等。你可以根据你的需要选择合适的类型。