# CUDA Backend for VTL

## Repository Structure for backend/cuda/
```
backend/cuda/
├── src/
│   ├── kernels/
│   │   ├── basic_ops.cu
│   │   ├── advanced_ops.cu
│   │   └── ...
│   ├── memory/
│   │   ├── allocation.v
│   │   └── transfer.v
│   ├── utils/
│   │   ├── error_handling.v
│   │   └── cuda_helpers.v
│   └── cuda_wrapper.v
├── include/
│   └── cuda_api.v
├── tests/
│   ├── unit_tests/
│   └── performance_tests/
├── examples/
├── docs/
└── build/
```

### Directory Descriptions

- `src/`: Main source code
  - `kernels/`: CUDA kernels (.cu files)
  - `memory/`: GPU memory management
  - `utils/`: Utilities (error handling, etc.)
  - `cuda_wrapper.v`: Main wrapper for CUDA functions
- `include/`: Header files for CUDA API in V
- `tests/`: Unit tests and performance tests
- `examples/`: Examples of CUDA backend usage
- `docs/`: Backend documentation
- `build/`: Files generated during compilation
```
