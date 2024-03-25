## Mutex

`Mutex<T>` 是 Rust 中的一个类型，它表示一个互斥锁（Mutex 是 Mutual Exclusion 的缩写）。它用于在多线程环境中保护共享数据，确保同一时间只有一个线程能够访问数据。

`Mutex<T>` 提供了 `lock` 方法，用于获取锁。当一个线程调用 `lock` 方法时，如果锁已经被其他线程持有，那么这个线程就会阻塞，直到锁被释放。当锁被释放后，阻塞的线程中的一个会获得锁，并继续执行。

`lock` 方法返回一个 `MutexGuard`，这是一个智能指针，它实现了 `Deref` 和 `DerefMut` trait，所以我们可以直接对它进行解引用，以访问内部的数据。当 `MutexGuard` 被丢弃时，它会自动释放锁。

以下是一个使用 `Mutex<T>` 的例子：

```rust
use std::sync::Mutex;
use std::thread;

fn main() {
    let counter = Mutex::new(0);
    let mut handles = vec![];

    for _ in 0..10 {
        let counter = &counter;
        let handle = thread::spawn(move || {
            let mut num = counter.lock().unwrap();
            *num += 1;
        });
        handles.push(handle);
    }

    for handle in handles {
        handle.join().unwrap();
    }

    println!("Result: {}", *counter.lock().unwrap());
}
```

在这个例子中，我们创建了一个 `Mutex`，然后在 10 个线程中共享它。每个线程都尝试获取锁，然后增加计数器的值。最后，我们打印出计数器的值，它应该是 10。

需要注意的是，尽管 `Mutex<T>` 可以安全地在多线程中共享数据，但它并不能防止死锁。如果不正确地使用 `Mutex<T>`，例如在持有锁的情况下再次尝试获取锁，或者在一个线程中获取了多个锁但释放的顺序不正确，都可能导致死锁。

### MutexGuard 是什么？

`MutexGuard` 是 Rust 中 `std::sync::Mutex` 的一个关联类型，当你调用 `Mutex` 的 `lock` 方法时，它会返回一个 `MutexGuard`。

`MutexGuard` 是一个智能指针，它代表了对 `Mutex` 中数据的锁定访问。只有当 `MutexGuard` 被丢弃（drop）时，锁才会被释放，其他线程才能获取到锁。

`MutexGuard` 实现了 `Deref` 和 `DerefMut` trait，这意味着你可以直接对 `MutexGuard` 进行解引用，以访问 `Mutex` 中的数据。

以下是一个使用 `MutexGuard` 的例子：

```rust
use std::sync::Mutex;

fn main() {
    let m = Mutex::new(5);

    {
        let mut num = m.lock().unwrap();
        *num = 6;
    } // `num` goes out of scope and releases the lock here.

    println!("m = {:?}", m);
}
```

在这个例子中，我们首先创建了一个 `Mutex`，然后通过 `lock` 方法获取了一个 `MutexGuard`。我们可以直接对 `MutexGuard` 进行解引用，以访问和修改 `Mutex` 中的数据。当 `MutexGuard` 在作用域结束时出于范围，锁就会被释放。