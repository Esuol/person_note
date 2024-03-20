## Clone

在 Rust 中，`Clone` trait 用于创建一个对象的副本。当你实现了 `Clone` trait，你就可以使用 `clone` 方法来复制一个对象。

以下是一个简单的例子，展示了如何为一个自定义类型 `Foo` 实现 `Clone` trait：

```rust
#[derive(Clone)]
struct Foo {
    bar: i32,
}
```

在这个例子中，我们使用 `#[derive(Clone)]` 属性为 `Foo` 结构体自动实现 `Clone` trait。

然后，我们就可以使用 `clone` 方法来复制 `Foo` 实例

```rust
let foo1 = Foo { bar: 42 };
let foo2 = foo1.clone();

assert_eq!(foo1.bar, foo2.bar);
```

在这个例子中，`foo1.clone()` 创建了一个 `foo1` 的副本，并将其赋值给 `foo2`。`assert_eq!(foo1.bar, foo2.bar);` 验证 `foo1` 和 `foo2` 的 `bar` 字段是否相等。

如果你的类型不能自动实现 `Clone` trait，或者你需要自定义复制行为，你可以手动实现 `Clone` trait。例如：

```rust
struct Foo {
    bar: i32,
}

impl Clone for Foo {
    fn clone(&self) -> Self {
        Self { bar: self.bar }
    }
}
```

在这个例子中，我们为 `Foo` 结构体手动实现 `Clone` trait。`clone` 方法创建一个新的 `Foo` 实例，其 `bar` 字段的值与原始实例相同。