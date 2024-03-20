## IntoIterator

在 Rust 中，`IntoIterator` 是一个 trait，它定义了一个可以转换为迭代器的类型。这个 trait 有一个方法 `into_iter`，这个方法会消耗自身并返回一个迭代器。

以下是 `IntoIterator` trait 的定义：

```rust
pub trait IntoIterator where
    Self::IntoIter::Item == Self::Item,
{
    type Item;
    type IntoIter: Iterator;
    fn into_iter(self) -> Self::IntoIter;
}
```

这个 trait 有两个关联类型：`Item` 和 `IntoIter`。`Item` 是迭代器产生的元素的类型，`IntoIter` 是迭代器的类型。

当你实现了 `IntoIterator` trait，你就可以在你的类型上使用 `for` 循环。例如，`Vec<T>` 类型就实现了 `IntoIterator` trait，所以你可以在一个 `Vec<T>` 上使用 `for` 循环：

```rust
let v = vec![1, 2, 3];
for i in v {
    println!("{}", i);
}
```

在这个例子中，`for` 循环调用了 `into_iter` 方法，将 `v` 转换为一个迭代器，然后遍历这个迭代器的所有元素。