## RefCell

在 Rust 中，`RefCell<T>` 是一个在运行时检查借用规则的工具。它代表了一个在运行时而不是在编译时执行借用规则的单元

在 Rust 中，我们通常使用 `&mut T` 来进行可变借用，但这需要在编译时就满足借用规则。然而，有些时候我们无法在编译时就确定这些规则，这时就可以使用 `RefCell<T>`。

`RefCell<T>` 有两个主要的方法：`borrow` 和 `borrow_mut`，它们分别用于获取 `RefCell` 的不可变引用和可变引用。这两个方法都会在运行时检查借用规则，如果违反了规则，程序就会 panic。

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

### RefCell 可以用于哪些场景？

`RefCell<T>` 主要用于在编译时无法确定借用规则，但又需要在运行时安全地共享可变状态的场景。以下是一些具体的使用场景：

1. **实现内部可变性（Interior Mutability）**：在 Rust 中，我们通常使用 `&mut T` 来进行可变借用，但这需要在编译时就满足借用规则。然而，有些时候我们希望能够在一个拥有不可变引用的上下文中改变数据，这时就可以使用 `RefCell<T>`。例如，我们可能有一个需要缓存结果的函数，当函数被调用时，我们希望能够更新缓存，即使函数的引用是不可变的。

```rust
use std::cell::RefCell;

struct Cacher<T>
where
    T: Fn(u32) -> u32,
{
    calculation: T,
    value: RefCell<Option<u32>>,
}

impl<T> Cacher<T>
where
    T: Fn(u32) -> u32,
{
    fn new(calculation: T) -> Cacher<T> {
        Cacher {
            calculation,
            value: RefCell::new(None),
        }
    }

    fn value(&self, arg: u32) -> u32 {
        match *self.value.borrow() {
            Some(v) => v,
            None => {
                let v = (self.calculation)(arg);
                *self.value.borrow_mut() = Some(v);
                v
            }
        }
    }
}

// 在这个例子中，我们创建了一个 Cacher 结构，它使用 RefCell 来存储一个可选的值。当我们调用 value 方法时，它会检查是否已经有缓存的值，如果没有，它会计算值，然后更新缓存。
```

1. **实现自引用类型**：有些时候，我们可能需要创建一个数据结构，其中的一部分需要引用另一部分。在 Rust 中，这通常很难实现，因为这可能会导致借用规则的违反。然而，我们可以使用 `RefCell<T>` 来安全地实现这种自引用类型。

```rust
use std::cell::RefCell;
use std::rc::Rc;

struct Node {
    value: i32,
    parent: RefCell<Rc<Node>>,
    children: RefCell<Vec<Rc<Node>>>,
}

// 在这个例子中，我们创建了一个 Node 结构，它使用 RefCell 来存储一个可变的父节点引用和一个可变的子节点列表。这样我们就可以在运行时安全地修改节点的父节点和子节点。
```

1. **在运行时检查借用规则**：在某些复杂的情况下，我们可能无法在编译时就确定所有的借用规则。例如，我们可能有一个数据结构，它的某些部分在某些条件下是可变的，但在其他条件下是不可变的。在这种情况下，我们可以使用 `RefCell<T>` 在运行时进行借用检查。

```rust
use std::cell::RefCell;

fn main() {
    let shared = RefCell::new(1);

    let _first_borrow = shared.borrow();
    let _second_borrow = shared.borrow();

    // This would panic at runtime
    // let _third_borrow = shared.borrow_mut();
}

// 在这个例子中，我们首先创建了一个 RefCell，然后进行了两次不可变借用。这是允许的，因为 RefCell 允许多个不可变借用。然而，如果我们试图在这之后进行可变借用，程序就会在运行时 panic，因为 RefCell 不允许在存在不可变借用的同时进行可变借用。
```



需要注意的是，`RefCell<T>` 只能用于单线程场景，如果需要在多线程中共享可变状态，应该使用 `Mutex<T>` 或 `RwLock<T>`。