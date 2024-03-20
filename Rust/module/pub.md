## pub

在 Rust 中，`pub` 关键字用于声明一个项（如函数、结构体、模块等）是公开的。然而，Rust 还提供了更细粒度的可见性控制，你可以使用 `pub(crate)`、`pub(in path)`、`pub(self)` 和 `pub(super)` 来限制项的可见性。

1. `pub(crate)`: 这个项只在当前 crate 中可见。这是在你想要创建 crate 内部 API 时的好选择。
2. `pub(in path)`: 这个项只在指定的模块（及其子模块）中可见。`path` 是一个相对于当前模块的路径。
3. `pub(self)`: 这个项只在当前模块中可见。这等价于不使用 `pub` 关键字。
4. `pub(super)`: 这个项只在父模块（及其子模块）中可见。

以下是一个例子：

```rust
mod outermost {
    pub(in outermost) fn outermost_fn() {}
    mod inner {
        pub(in outermost) fn inner_fn() {}
        pub(self) fn inner_fn2() {}
        pub(crate) fn inner_fn3() {}
        pub(super) fn inner_fn4() {}
    }
}
```

在这个例子中，`outermost_fn` 和 `inner_fn` 只在 `outermost` 模块中可见，`inner_fn2` 只在 `inner` 模块中可见，`inner_fn3` 在整个 crate 中可见，`inner_fn4` 只在 `outermost` 模块中可见。



