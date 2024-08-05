# Cuda backend for VTL
Voici l'architecture réécrite en format Markdown pour votre README :

```markdown
## Structure du répertoire backend/cuda/

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

### Description des dossiers

- `src/`: Code source principal
  - `kernels/`: Kernels CUDA (.cu files)
  - `memory/`: Gestion de la mémoire GPU
  - `utils/`: Utilitaires (gestion des erreurs, etc.)
  - `cuda_wrapper.v`: Wrapper principal pour les fonctions CUDA
- `include/`: Fichiers d'en-tête pour l'API CUDA en V
- `tests/`: Tests unitaires et de performance
- `examples/`: Exemples d'utilisation du backend CUDA
- `docs/`: Documentation du backend
- `build/`: Fichiers générés lors de la compilation
```
