# Building KVM Unit Tests for illumos

The procedure to build the tests is straight-forward.
Note the local patches that use an explicit linker
instead of `${CC}` to link, and note that we use build
with clang and use the LLVM version of objcopy.

* ./configure --arch=x86_64
* PATH=/usr/gnu/bin:$PATH make OBJCOPY=/opt/ooce/llvm-12.0/bin/llvm-objcopy CC=clang
