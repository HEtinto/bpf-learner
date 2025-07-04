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