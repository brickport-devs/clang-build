# Rui clang

Yet another [LLVM](https://llvm.org/) and [Clang](https://clang.llvm.org/) compiler toolchain built for **Android kernel** development.

## Host compatibility

This toolchain is built on latest Arch Linux, so compatibility with other distros cannot be guaranteed.

## Usage

GitHub limits the size of files allowed in repos, so currently this toolchain is hosted at [Project ICE git](https://git.project-ice.org/brickport-devs/rui-clang/).

To initialize, make sure you have this toolchain in your `PATH`:
```bash
export PATH="/path/to/rui-clang/bin:$PATH"
```

For an AArch64 cross-compilation setup, some variables must be passed directly to `make` as a command-line 
argument. It's recommended to create an alias in your shell like the following:
```bash
alias make='make LLVM=1 CC=clang PYTHON=python2 ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu- CROSS_COMPILE_ARM32=arm-linux-gnueabi- CROSS_COMPILE_COMPAT=arm-linux-gnueabi-'
```

## Credits

- [Nathan Chancellor](https://github.com/nathanchance) for his outstanding contributions to [CBL Project](https://github.com/ClangBuiltLinux).

- [Danny Lin](https://github.com/kdrag0n) for the launch script.
