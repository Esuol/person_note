## PathBuf

`PathBuf` 是 Rust 标准库中的一个类型，用于表示文件系统路径。它是 `Path` 类型的所有权版本，可以被安全地修改和增长。

`PathBuf` 提供了一系列方法来操作路径，例如：

- `push`：将一个路径片段添加到 `PathBuf` 的末尾。
- `pop`：移除 `PathBuf` 末尾的路径片段。
- `as_path`：将 `PathBuf` 转换为 `Path`。
- `join`：连接两个路径，返回一个新的 `PathBuf`。

以下是一个 `PathBuf` 的使用示例：

```rust
use std::path::PathBuf;

fn main() {
    let mut path = PathBuf::new();

    path.push("c:");
    path.push("Windows");
    path.push("System32");

    println!("Path: {}", path.display());
}
```

在这个例子中，我们创建了一个新的 `PathBuf`，然后使用 `push` 方法添加了几个路径片段。最后，我们使用 `display` 方法打印出完整的路径。

需要注意的是，`PathBuf` 和 `Path` 的操作都是跨平台的，Rust 标准库会根据当前的操作系统自动选择正确的路径分隔符。