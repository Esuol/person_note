## once_cell

[once_cell](https://github.com/matklad/once_cell)

`once_cell`是一个Rust的库，它提供了两种主要的类型：`OnceCell`和`Lazy`。

`OnceCell`可能存储单个值，该值可以在运行时被初始化一次（从未初始化状态到某个值）。尝试再次初始化将不会改变存储的值。这对于延迟初始化全局变量、静态变量和其他一次性初始化的值非常有用。

```rust
use once_cell::sync::OnceCell;

static CELL: OnceCell<String> = OnceCell::new();

fn main() {
    CELL.set("Hello, world!".to_string()).unwrap();
    assert_eq!(CELL.get().unwrap().as_str(), "Hello, world!");
}
```

`Lazy`是一个将初始化逻辑和值存储结合在一起的类型，它保证初始化代码只运行一次，并提供对结果的直接访问。

```rust
use once_cell::sync::Lazy;

static DATA: Lazy<Mutex<HashMap<i32, String>>> = Lazy::new(|| {
    let mut m = HashMap::new();
    m.insert(13, "Spica".to_string());
    m.insert(74, "Hoyten".to_string());
    Mutex::new(m)
});

fn main() {
    println!("{:?}", DATA.lock().unwrap());
}
```

