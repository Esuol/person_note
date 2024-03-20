## Debug

在 Rust 中，`Debug` 是一个 trait，它用于格式化值以便进行调试输出。当你实现了 `Debug` trait，你就可以使用 `{:?}` 或 `{:#?}` 格式说明符来打印值。

以下是一个简单的例子，展示了如何为一个自定义类型 `Foo` 实现 `Debug` trait：

```rust
#[derive(Debug)]
struct Foo {
    bar: i32,
}
```

在这个例子中，我们使用 `#[derive(Debug)]` 属性为 `Foo` 结构体自动实现 `Debug` trait。

然后，我们就可以使用 `println!` 宏来打印 `Foo` 实例：

```rust
let foo = Foo { bar: 42 };
println!("{:?}", foo);
```

如果你的类型不能自动实现 `Debug` trait，或者你需要自定义调试输出，你可以手动实现 `Debug` trait。例如：

```rust
use std::fmt;

struct Foo {
    bar: i32,
}

impl fmt::Debug for Foo {
    fn fmt(&self, f: &mut fmt::Formatter<'_>) -> fmt::Result {
        write!(f, "Foo {{ bar: {} }}", self.bar)
    }
}
```

在这个例子中，我们为 `Foo` 结构体手动实现 `Debug` trait。`fmt` 方法接收一个 `Formatter`，并写入我们自定义的调试输出。