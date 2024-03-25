## Deref

`Deref` 是 Rust 语言中的一个 trait，它允许开发者重载解引用运算符 `*`。这个 trait 主要用于实现自定义指针类型。

`Deref` trait 定义如下：

```rust
pub trait Deref {
    type Target: ?Sized;
    fn deref(&self) -> &Self::Target;
}
```

当你实现了 `Deref` trait，你就可以使用 `*` 运算符来解引用你的类型。例如：

```rust
use std::ops::Deref;

struct MyBox<T>(T);

impl<T> Deref for MyBox<T> {
    type Target = T;

    fn deref(&self) -> &T {
        &self.0
    }
}

fn main() {
    let x = 5;
    let y = MyBox(x);

    assert_eq!(5, *y);
}
```

在这个例子中，我们创建了一个 `MyBox<T>` 类型，并为它实现了 `Deref` trait。这样我们就可以使用 `*` 运算符来解引用 `MyBox<T>` 类型的实例，获取到内部的值。