## Instalación

Para instalar y usar `llama.cpp`, sigue los pasos a continuación.

### Requisitos previos
Saber si usaremos tarjeta grafica o no y que marca tenemos AMD O NVIDIA.
- CMake 3.15 o superior
- Un compilador de C++ moderno (como g++, clang++, etc.)
- Bibliotecas estándar de C++17

### Pasos de instalación
1. Instalar y actualizar dependencias.
```bash
apt update && apt install -y cmake build-essential git
```
2. Dependencias de graficas.
Librerias ROCm
```bash
apt install rocm-opencl-runtime -y
```
Librerias CUDA
```bash
apt install nvidia-cuda-toolkit -y
```
2. Clona el repositorio:
```bash
  git clone https://github.com/ggerganov/llama.cpp.git
  cd llama.cpp
```
2. Compilacion:
 ```bash
 # Crea una carpeta de compilación y entramos en ella.
mkdir build && cd build
```
 ```bash
 # Ejecuta CMake para configurar el proyecto y compilar
cmake ..
cmake --build . --parallel
```
 ```bash
 #Para graficas AMD
cmake .. -DLLAMA_HIPBLAS=ON
cmake --build . --parallel
#Para n
