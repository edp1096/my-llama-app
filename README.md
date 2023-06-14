[my-llama](https://github.com/edp1096/my-llama) runner for go module testing and example.

## Binary
* [MS-Windows](https://github.com/edp1096/my-llama/releases)

## Build
* `CGO_ENABLED` must be set to `1`

### CPU
* Require `llama.dll` from [here](https://github.com/edp1096/my-llama/releases)
```powershell
go build [-tags cpu]
```

### CLBlast
* Require
    * `llama_cl.dll` and `clblast.dll` from [here](https://github.com/edp1096/my-llama/releases)
    * One of them
        * NVIDIA CUDA SDK
        * AMD APP SDK
        * AMD ROCm
        * Intel OpenCL
```powershell
go build -tags clblast
```

### CUDA
* Require
    * `llama_cu.dll` from [here](https://github.com/edp1096/my-llama/releases)
    * [CUDA Toolkit 12](https://developer.nvidia.com/cuda-downloads?target_os=Windows&target_arch=x86_64)
```powershell
go build -tags cuda
```
