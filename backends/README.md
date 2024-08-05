# All Backends in VTL Engine

VTL Engine supports the following backends:
   - Cuda
   - OpenMP
   - Vulkan

## Cuda
 First install cuda toolkit: https://developer.nvidia.com/cuda-downloads
  ### usage:
  ```vlang
        import vtl
        vtl_tensor := vtl.from_array([1.0, 2, 3, 4], [2, 2])!
        vtl_tensor.cuda()
        println('My device: ${vtl_tensor.device}')

  ```


## OpenMP
  ### usage:
```vlang
        import vtl
        vtl_tensor := vtl.from_array([1.0, 2, 3, 4], [2, 2])!
        // pragma omp target in loop
        // TODO: add pragma omp target in loop
        for i in 0 .. vtl_tensor.shape[0] {
            for j in 0 .. vtl_tensor.shape[1] {
                vtl_tensor[i, j] = vtl_tensor[j, i] + 1
                println('from thread: ${vtl_tensor[i, j]}')
            }
        }

```

## Vulkan
  ### usage:
  ```vlang
        import vtl
        vtl_tensor := vtl.from_array([1.0, 2, 3, 4], [2, 2])!
        // send vtl_tensor to gpu
        vtl_tensor.vulkan().gpu()
        // send vtl_tensor to cpu
        vtl_tensor.vulkan().cpu()
        // note: if gpu is not available, cpu will be used by default and 
        // vtl_tensor.vulkan().gpu() will be ignored in this case
        println('My device: ${vtl_tensor.device}')

  ```
