## Quote

`quote` 是一个 Rust 库，它提供了一种方便的方式来构造 `TokenStream`。`TokenStream` 类型是 Rust 的过程宏系统的核心类型，它表示一系列的令牌，这些令牌可以代表任何有效的 Rust 代码。

`quote` 是一个 Rust 的库，它提供了一种方便的方式来操作 Rust 代码的抽象表示。它主要用于编写过程宏（procedural macros）和编译器插件。

`quote` 库提供了 `quote!` 宏，这个宏可以接收 Rust 代码，并将其转换为 `TokenStream` 类型。`TokenStream` 类型是 Rust 的过程宏系统的核心类型，它表示一系列的令牌，这些令牌可以代表任何有效的 Rust 代码。

例如

```rust
let name = "world";
let tokens = quote! {
    println!("Hello, {}!", #name);
};
```

在这个例子中，`quote!` 宏接收了一个 `println!` 表达式，并将其转换为 `TokenStream`。`#name` 是一个插值表达式，它将 `name` 变量的值插入到生成的代码中。

此外，`quote` 库还提供了一些其他的功能，例如重复代码片段（通过 `#( ... )*` 和 `#( ... ),*`），插入标识符（通过 `#ident`）等等。

`__private::Span` 是 `quote` 库内部使用的类型，通常你不需要直接使用它。`Span` 类型表示一个源代码中的区域，它用于错误报告和宏扩展。