## Arc

`Arc<T>` 是 Rust 中的一个类型，它代表一个线程安全的引用计数指针（Arc 是 Atomic Reference Count 的缩写）。它用于在多线程环境中共享数据，当最后一个引用离开作用域时，数据会被自动清理。

`Arc<T>` 提供了 `clone` 方法，用于创建一个新的 `Arc` 实例，这个新的实例和原始实例指向同一块数据，但引用计数会增加。当 `Arc` 实例被丢弃时，引用计数会减少。当引用计数变为 0 时，数据会被清理。

以下是一个使用 `Arc<T>` 的例子：

```rust
use std::sync::Arc;
use std::thread;

fn main() {
    let five = Arc::new(5);

    for _ in 0..10 {
        let five = Arc::clone(&five);

        thread::spawn(move || {
            println!("{:?}", *five);
        });
    }
}
```

在这个例子中，我们创建了一个 `Arc`，然后在 10 个线程中共享它。每个线程都有一个 `Arc` 的副本，它们都指向同一块数据。当所有线程都结束时，最后一个 `Arc` 会被丢弃，数据会被清理。

需要注意的是，尽管 `Arc<T>` 可以安全地在多线程中共享数据，但它并不能提供数据的互斥访问。如果你需要在多线程中修改数据，你可能需要使用 `Mutex<T>` 或 `RwLock<T>` 来提供互斥访问。