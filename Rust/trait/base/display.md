## Display

在 Rust 中，`Display` trait 用于格式化值以便进行友好的显示。当你实现了 `Display` trait，你就可以使用 `{}` 格式说明符来打印值。

以下是一个简单的例子，展示了如何为一个自定义类型 `Foo` 实现 `Display` trait：

```rust
se std::fmt;

struct Foo {
    bar: i32,
}

impl fmt::Display for Foo {
    fn fmt(&self, f: &mut fmt::Formatter<'_>) -> fmt::Result {
        write!(f, "Foo with bar: {}", self.bar)
    }
}
```

在这个例子中，我们为 `Foo` 结构体手动实现 `Display` trait。`fmt` 方法接收一个 `Formatter`，并写入我们自定义的显示输出。

然后，我们就可以使用 `println!` 宏来打印 `Foo` 实例：

```rust
let foo = Foo { bar: 42 };
println!("{}", foo);
```

在这个例子中，`println!("{}", foo);` 会打印出 `Foo` 实例的显示输出，例如 `Foo with bar: 42`。

注意，`Display` trait 通常用于用户友好的输出，而 `Debug` trait 用于调试输出。如果可能，你应该为你的类型实现这两个 trait。

### 如何在 Rust 中同时实现 `Debug` 和 `Display` trait？

在 Rust 中，你可以为一个类型同时实现 `Debug` 和 `Display` trait。这通常是一个好主意，因为 `Debug` trait 用于调试输出，而 `Display` trait 用于用户友好的输出。

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

impl fmt::Display for Foo {
    fn fmt(&self, f: &mut fmt::Formatter<'_>) -> fmt::Result {
        write!(f, "Foo with bar: {}", self.bar)
    }
}
```

在这个例子中，我们为 `Foo` 结构体手动实现了 `Debug` 和 `Display` trait。`Debug` 的 `fmt` 方法输出 `Foo { bar: 42 }`，而 `Display` 的 `fmt` 方法输出 `Foo with bar: 42`。

然后，我们就可以使用 `println!` 宏来打印 `Foo` 实例：

```rust
let foo = Foo { bar: 42 };
println!("{:?}", foo); // 使用 Debug trait
println!("{}", foo); // 使用 Display trait
```

在这个例子中，`println!("{:?}", foo);` 会打印出 `Foo` 实例的调试输出，而 `println!("{}", foo);` 会打印出 `Foo` 实例的显示输出。