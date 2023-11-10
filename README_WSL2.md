# Build with WSL2 kernel

```
# Clone the kernel
git clone https://github.com/microsoft/WSL2-Linux-Kernel

# Install the build dependencies
sudo apt install build-essential flex bison dwarves libssl-dev libelf-dev

# Build the kernel
cd /path/to/WSL2-Linux-Kernel
make -j$(nproc) KCONFIG_CONFIG=Microsoft/config-wsl

# Build the module
export KERNELDIR=/path/to/WSL2-Linux-Kernel
cd /path/to/ldd3/<module>
make
```