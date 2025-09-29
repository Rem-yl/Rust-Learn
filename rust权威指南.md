# Rust权威指南第二版
## Rust入门

使用`cargo`管理rust项目

```bash
cargo new hello_world
cd hello_world
cargo build
cargo build --release   # 牺牲编译速度, 提高文件运行时速度
cargo run
cargo check # 检查代码是否能够通过编译, 不生成可执行文件
```

在 Rust 中,变量默认都是不可变的。一旦为变量赋予了某个值,这个值就不会发生任何变化。

```rust
let x = 5;  // x 是不可变的
x = 6;      // 错误! x 是不可变的
let mut y = 5;  // y 是可变的
y = 6;          // 正确! y 是可变的
```