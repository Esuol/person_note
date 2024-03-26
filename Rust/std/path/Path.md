## Path

`Path` 是 Rust 标准库中的一个类型，用于表示文件系统路径。它是 `PathBuf` 类型的借用版本，不能被修改，但可以用于读取路径的各个部分。

`Path` 提供了一系列方法来读取和操作路径，例如：

- `parent`：返回路径的父目录。
- `file_name`：返回路径的文件名。
- `extension`：返回路径的文件扩展名。
- `is_absolute`：检查路径是否是绝对路径。
- `is_relative`：检查路径是否是相对路径。

以下是一个 `Path` 的使用示例：

```rust
use std::path::Path;

fn main() {

  let path = Path::new("/tmp/foo/bar.txt");

  println!("Parent: {:?}", path.parent());

  println!("File name: {:?}", path.file_name());

  println!("Extension: {:?}", path.extension());

  println!("Is absolute: {}", path.is_absolute());

  println!("Is relative: {}", path.is_relative());

}
```

在这个例子中，我们创建了一个新的 `Path`，然后使用各种方法读取了路径的各个部分。

需要注意的是，`Path` 和 `PathBuf` 的操作都是跨平台的，Rust 标准库会根据当前的操作系统自动选择正确的路径分隔符。

### 如何在 Rust 中检查路径是否存在？

在 Rust 中，你可以使用 `std::path::Path` 的 `exists` 方法来检查一个路径是否存在。以下是一个示例：

```rust
use std::path::Path;

fn main() {
    let path = Path::new("/tmp/foo/bar.txt");

    if path.exists() {
        println!("Path exists");
    } else {
        println!("Path does not exist");
    }
}
```

在这个例子中，我们首先创建了一个 `Path`，然后使用 `exists` 方法来检查这个路径是否存在。如果路径存在，我们打印 "Path exists"，否则我们打印 "Path does not exist"。

需要注意的是，`exists` 方法只能检查路径是否存在，它不能告诉你这个路径是一个文件还是一个目录。如果你需要检查路径是一个文件还是一个目录，你可以使用 `is_file` 或 `is_dir` 方法。

### 如何在 Rust 中创建一个新的目录？

