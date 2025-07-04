# bfp-learner

## install

tools is on `/usr/share/bcc/tools/`.

```sh
sudo dnf install -y bcc bcc-tools kernel-devel-$(uname -r)
```

advanced bpf tools

```sh
sudo dnf install -y bpftool
```

bpf devel

```sh
sudo dnf install -y llvm clang libbpf-devel elfutils-libelf-devel
```

## QA


### LLVM registered more than once

Q: 
    Abort on startup: CommandLine Error: Option ... registered more than once!

Solve: 
    add -DENABLE_LLVM_SHARED=1 when use cmake to build.

Correlation issues:
    https://github.com/bpftrace/bpftrace/commit/debc79ef9ad4784258705a92ae70f9c7689a9c24
    https://github.com/iovisor/bcc/issues/2278