## partialEq

在 Rust 中，`PartialEq` trait 用于比较两个值是否相等。以下是一个简单的例子，展示了如何为一个自定义类型 `Foo` 实现 `PartialEq` trait：

然后，我们就可以使用 `==` 和 `!=` 运算符来比较 `Foo` 实例：

```rust
let foo1 = Foo { bar: 42 };
let foo2 = Foo { bar: 42 };
let foo3 = Foo { bar: 43 };

assert!(foo1 == foo2);
assert!(foo1 != foo3);
```

在这个例子中，`foo1 == foo2` 返回 `true`，因为 `foo1` 和 `foo2` 的 `bar` 字段都是 `42`。`foo1 != foo3` 返回 `true`，因为 `foo1` 的 `bar` 字段是 `42`，而 `foo3` 的 `bar` 字段是 `43`。

如果你的类型不能自动实现 `PartialEq` trait，或者你需要自定义相等性比较，你可以手动实现 `PartialEq` trait。例如：

```rust
use std::cmp::PartialEq;

struct Foo {
    bar: i32,
}

impl PartialEq for Foo {
    fn eq(&self, other: &Self) -> bool {
        self.bar == other.bar
    }
}
```

在这个例子中，我们为 `Foo` 结构体手动实现 `PartialEq` trait。`eq` 方法比较两个 `Foo` 实例的 `bar` 字段是否相等。

### Eq

在 Rust 中，`Eq` trait 用于表示一个类型的值可以进行完全相等性比较。`Eq` trait 是 `PartialEq` trait 的子 trait，它没有定义任何新的方法，只是一个标记 trait，表示类型的所有值都是可比较的。

如果你的类型可以进行完全相等性比较，你应该为它实现 `Eq` trait。例如：

```rust
#[derive(PartialEq, Eq)]
struct Foo {
    bar: i32,
}
```

在这个例子中，我们使用 `#[derive(PartialEq, Eq)]` 属性为 `Foo` 结构体自动实现 `PartialEq` 和 `Eq` trait。

然后，我们就可以使用 `==` 和 `!=` 运算符来比较 `Foo` 实例：

```rust
let foo1 = Foo { bar: 42 };
let foo2 = Foo { bar: 42 };
let foo3 = Foo { bar: 43 };

assert!(foo1 == foo2);
assert!(foo1 != foo3);
```

注意，`Eq` trait 通常用于那些所有值都是可比较的类型，例如整数和字符串。对于那些包含浮点数的类型，由于 NaN（非数字）的存在，它们通常只能实现 `PartialEq` trait，而不能实现 `Eq` trait。

### Eq和patialEq关系，以及使用场景

在 Rust 中，`PartialEq` 和 `Eq` 都是用于比较两个值是否相等的 trait。它们的主要区别在于，`PartialEq` 允许部分相等性比较，而 `Eq` 要求完全相等性比较。

`PartialEq` trait 定义了一个 `eq` 方法，用于比较两个值是否相等。大多数类型都可以实现 `PartialEq`，并使用 `==` 和 `!=` 运算符进行比较。

`Eq` trait 是 `PartialEq` 的子 trait，它没有定义任何新的方法，只是一个标记 trait，表示类型的所有值都是可比较的。也就是说，对于任何两个值 `a` 和 `b`，`a == b` 或 `a != b` 总是成立的。

以下是一些使用场景：

- 如果你的类型的所有值都是可比较的，你应该为它实现 `Eq` trait。例如，整数和字符串都可以实现 `Eq`。
- 如果你的类型包含浮点数，由于 NaN（非数字）的存在，它们通常只能实现 `PartialEq` trait，而不能实现 `Eq` trait。因为 NaN 不等于任何值，包括它自己。
- 如果你的类型需要自定义相等性比较，你可以手动实现 `PartialEq` trait。例如，你可能有一个 `Person` 类型，你想要比较两个 `Person` 实例是否有相同的姓名，而不是比较它们的所有字段。

总的来说，`PartialEq` 和 `Eq` trait 都是 Rust 中比较两个值是否相等的工具。你应该根据你的类型的特性和需求来选择实现哪一个 trait。