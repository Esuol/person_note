## anyhow

https://github.com/dtolnay/anyhow

`anyhow` 是 Rust 的一个库，用于简化错误处理。它提供了一个 `anyhow::Error` 类型，可以包含任何实现了 `std::error::Error` trait 的错误类型。这使得你可以在一个函数中返回不同类型的错误，而无需创建一个自定义的错误枚举来包含所有可能的错误类型。

以下是 `anyhow` 的一些主要特性：

1. **简化错误处理**：`anyhow::Error` 可以包含任何错误，使得你可以在一个函数中返回不同类型的错误。
2. **错误链**：`anyhow::Error` 支持错误链，你可以使用 `context` 或 `with_context` 方法添加上下文信息，或者使用 `source` 方法获取原始错误。
3. **易于使用**：`anyhow::Error` 实现了 `std::error::Error`，`std::fmt::Display` 和 `std::fmt::Debug` trait，使得它可以被用在任何期望 `std::error::Error` 的地方，也可以被打印或调试。

以下是一个使用 `anyhow` 的例子：

```rust
use anyhow::{Context, Result};

fn read_file(path: &str) -> Result<String> {
    let content = std::fs::read_to_string(path).with_context(|| format!("failed to read file {}", path))?;
    Ok(content)
}

fn main() {
    match read_file("non_existent_file.txt") {
        Ok(content) => println!("File content: {}", content),
        Err(e) => println!("Error: {}", e),
    }
}
```

在这个例子中，`read_file` 函数返回一个 `Result<String, anyhow::Error>`。如果文件读取失败，它会返回一个 `anyhow::Error`，并使用 `with_context` 方法添加一个描述错误的消息。在 `main` 函数中，我们检查 `read_file` 的结果，如果出现错误，我们打印出错误的描述。

### anyhow 和 Result 的选择有什么区别？

`anyhow::Result` 和标准库的 `Result` 都是用于错误处理的枚举类型，但它们的用途和设计目标有所不同。

1. **anyhow::Result**：`anyhow::Result<T>` 是 `std::result::Result<T, anyhow::Error>` 的别名。`anyhow::Error` 可以包含任何实现了 `std::error::Error` trait 的错误类型。这使得你可以在一个函数中返回不同类型的错误，而无需创建一个自定义的错误枚举来包含所有可能的错误类型。`anyhow::Result` 主要用于应用程序，特别是那些不需要创建自定义错误类型的应用程序。
2. **std::result::Result**：标准库的 `Result<T, E>` 类型需要你为每个函数指定一个具体的错误类型 `E`。这使得你可以创建自定义的错误类型，以表示函数可能返回的所有错误。`std::result::Result` 主要用于库和需要创建自定义错误类型的应用程序。

总的来说，`anyhow::Result` 和 `std::result::Result` 在错误处理上互补。在库中，你可能会使用 `std::result::Result` 来创建自定义错误类型，然后在应用程序中，你可能会使用 `anyhow::Result` 来处理这些错误。
