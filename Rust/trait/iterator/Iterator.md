## Iterator

在 Rust 中，`Iterator` 是一个 trait，它定义了一个可以产生一系列值的类型。这个 trait 主要有一个方法 `next`，这个方法在每次调用时返回序列中的下一个值。

以下是 `Iterator` trait 的定义：

```rust
pub trait Iterator {
    type Item;
    fn next(&mut self) -> Option<Self::Item>;
    // 其他方法...
}
```

这个 trait 有一个关联类型：`Item`。`Item` 是迭代器产生的元素的类型。

`next` 方法返回一个 `Option<Self::Item>`。当迭代器还有元素时，`next` 返回 `Some(element)`；当迭代器没有元素时，`next` 返回 `None`。

除了 `next` 方法，`Iterator` trait 还提供了许多其他方法，如 `map`、`filter`、`fold` 等。这些方法可以用来转换、过滤或者组合迭代器的元素。

例如，以下是一个使用 `Iterator` 的例子：

```rust
let v = vec![1, 2, 3];
let mut iter = v.iter();

assert_eq!(iter.next(), Some(&1));
assert_eq!(iter.next(), Some(&2));
assert_eq!(iter.next(), Some(&3));
assert_eq!(iter.next(), None);
```

在这个例子中，我们创建了一个向量 `v`，然后通过调用 `iter` 方法获取了一个迭代器 `iter`。然后我们反复调用 `next` 方法来获取迭代器的元素，直到迭代器没有元素为止。

### 如何自定义Iterator

在 Rust 中，你可以通过实现 `Iterator` trait 来自定义迭代器。以下是一个简单的例子：

```rust
struct Counter {
    count: u32,
}

impl Counter {
    fn new() -> Counter {
        Counter { count: 0 }
    }
}

impl Iterator for Counter {
    type Item = u32;

    fn next(&mut self) -> Option<Self::Item> {
        self.count += 1;

        if self.count < 6 {
            Some(self.count)
        } else {
            None
        }
    }
}

fn main() {
    let mut counter = Counter::new();

    while let Some(n) = counter.next() {
        println!("{}", n);
    }
}
```

在这个例子中，我们定义了一个 `Counter` 结构体，这个结构体有一个 `count` 字段。然后我们为 `Counter` 实现了 `Iterator` trait。在 `next` 方法中，我们增加 `count` 的值，然后如果 `count` 小于 6，我们就返回 `Some(count)`，否则我们就返回 `None`。这样，我们就创建了一个可以产生 1 到 5 的迭代器。

在 `main` 函数中，我们创建了一个 `Counter` 实例，然后使用 `while let` 循环来遍历这个迭代器的所有元素