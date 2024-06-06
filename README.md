# Build
## Run docker
```dockerignore
docker build -t myos-buildenv .
```
## Build docker
```dockerignore
$currentDir = (Get-Location).Path
docker run --rm -it -v ${currentDir}:/root/env myos-buildenv
```

## Build ISO
```dockerignore
make build-x86_64
```

# Run in virtual machine qemu
```
qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso 
```
