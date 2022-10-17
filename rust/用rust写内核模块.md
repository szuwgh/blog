### 1、拉取rust_for_linux 代码

```
git clone https://github.com/Rust-for-Linux/linux.git
```

### 2、设置rust 环境
```
rustup override set $(scripts/min-tool-version.sh rustc)
rustup component add rust-src
make allnoconfig x86_64_defconfig qemu-busybox-min.config rust.config
```
### 3、编译linux内核
```
make CC=clang
```
### 4、制作根文件系统

### 5、用qemu启动内核

### 6、编写hello内核模块并运行