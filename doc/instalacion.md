# 📌 Instalación de `llama.cpp`

Guía para instalar y usar `llama.cpp` en tu sistema.

## ✅ Requisitos previos
Antes de comenzar, asegúrate de tener:
- **CMake** 3.15 o superior
- **Compilador de C++ moderno** (g++, clang++, etc.)
- **Bibliotecas estándar de C++17**
- **Soporte para GPU** (opcional, según tu hardware)

---

## 🔧 1. Instalación de dependencias
Ejecuta el siguiente comando para instalar las herramientas necesarias:

```bash
apt update && apt install -y cmake build-essential git
```

### 🚀 Soporte para GPU (Opcional)
Si tienes una tarjeta gráfica y quieres aprovecharla:

#### 🔴 Para GPUs **AMD** (ROCm)
```bash
apt install rocm-opencl-runtime -y
```

#### 🟢 Para GPUs **NVIDIA** (CUDA)
```bash
apt install nvidia-cuda-toolkit -y
```

---

## 💽 2. Clonar el repositorio
Descarga `llama.cpp` desde GitHub y accede al directorio:

```bash
git clone https://github.com/ggerganov/llama.cpp.git
cd llama.cpp
```

---

## 🔨 3. Compilación del código
Primero, crea un directorio para la compilación:

```bash
mkdir build && cd build
```

Luego, ejecuta **CMake** para configurar y compilar el proyecto:

```bash
cmake ..
cmake --build . --parallel
```

### 🔄 Compilación con soporte para GPU
Si deseas usar tu GPU, compila con la opción correspondiente:

#### 🔴 Para GPUs **AMD** (ROCm)
```bash
cmake .. -DLLAMA_HIPBLAS=ON
cmake --build . --parallel
```

#### 🟢 Para GPUs **NVIDIA** (CUDA)
```bash
cmake .. -DLLAMA_CUDA=ON
cmake --build . --parallel
```

---


