[my-llama](https://github.com/edp1096/my-llama) runner for go module testing and example.

## Binary
* [MS-Windows cpu](https://github.com/edp1096/my-llama/releases/download/v0.1.15/my-llama_cpu.zip)
* [MS-Windows clblast](https://github.com/edp1096/my-llama/releases/download/v0.1.15/my-llama_cl.zip)
    * Require one of them installed
        * NVIDIA CUDA SDK
        * AMD APP SDK
        * AMD ROCm
        * Intel OpenCL


## Build

### CPU
* Require `llama.dll` from [here](https://github.com/edp1096/my-llama/releases)
```powershell
go build -tags cpu
```

### CLBlast
* Require `llama_cl.dll` and `clblast.dll` from [here](https://github.com/edp1096/my-llama/releases)
* Also require one of them installed
    * NVIDIA CUDA SDK
    * AMD APP SDK
    * AMD ROCm
    * Intel OpenCL
```powershell
go build -tags clblast -ldflags="-X main.deviceType=clblast"
```
