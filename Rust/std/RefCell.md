## RefCell

在 Rust 中，`RefCell<T>` 是一个在运行时检查借用规则的工具。它代表了一个在运行时而不是在编译时执行借用规则的单元。

RefCell<T>` 有一个 `borrow()` 方法，返回一个 `Ref<T>` 类型的值，这个值实现了 `Deref` trait，所以可以被当作不可变引用。`RefCell<T>` 还有一个 `borrow_mut()` 方法，返回一个 `RefMut<T>` 类型的值，这个值实现了 `DerefMut` trait，所以可以被当作可变引用。

`RefCell<T>` 只能用于单线程场景。如果你需要在多线程中共享可变状态，你应该使用一种如 `Mutex<T>` 的并发类型。

以下是一个使用 `RefCell<T>` 的例子：

```rust
use std::cell::RefCell;

let c = RefCell::new(5);

let mut m = c.borrow_mut();

*m += 1;

println!("{}", c.borrow());
```

在这个例子中，我们首先创建了一个 `RefCell`，然后我们借用了一个可变引用，并增加了它的值。最后，我们打印了 `RefCell` 的值。注意，如果我们试图在已经存在一个可变引用的情况下再次借用一个可变引用，`RefCell` 会在运行时 panic。