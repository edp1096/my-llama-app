[my-llama](https://github.com/edp1096/my-llama) runner for go module testing

## Build

### CPU
* Require `llama.dll` from [here](https://github.com/edp1096/my-llama/releases)
```powershell
$env:CGO_LDFLAGS=$null
go build -tags cpu -o bin/
```

### CLBlast
* Require `llama_cl.dll` and `clblast.dll` from [here](https://github.com/edp1096/my-llama/releases)
* Also require one of them installed
    * NVIDIA CUDA SDK
    * AMD APP SDK
    * AMD ROCm
    * Intel OpenCL
```powershell
$env:CGO_LDFLAGS=$null
go build -tags clblast -ldflags="-X main.deviceType=clblast" -o bin/
```
