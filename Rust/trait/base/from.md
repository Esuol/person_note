From 

在 Rust 中，`From` trait 用于定义一种类型如何从另一种类型转换得到。以下是一个简单的例子，展示了如何为一个自定义类型 `Foo` 实现 `From<i32>` trait：

```rust
struct Foo {
    value: i32,
}

impl From<i32> for Foo {
    fn from(item: i32) -> Self {
        Foo { value: item }
    }
}

let foo = Foo::from(42);
// 或者使用 into 方法进行类型转换：
let foo: Foo = 42.into();
```

在这个例子中，`Foo` 结构体有一个 `value` 字段，类型为 `i32`。我们为 `Foo` 实现了 `From<i32>` trait，`from` 方法接收一个 `i32` 类型的参数，并返回一个新的 `Foo` 实例，其 `value` 字段与传入的 `i32` 值相同。

在这两个例子中，我们都使用 `42` 来创建了一个 `Foo` 实例。