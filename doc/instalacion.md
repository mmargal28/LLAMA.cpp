## Instalación

Para instalar y usar `llama.cpp`, sigue los pasos a continuación.

### Requisitos previos

- CMake 3.15 o superior
- Un compilador de C++ moderno (como g++, clang++, etc.)
- Bibliotecas estándar de C++17

### Pasos de instalación

1. Clona el repositorio:

  ```bash
  git clone https://github.com/ggerganov/llama.cpp.git
  cd llama.cpp
2. Compilacion:
 ```bash
  # Crea una carpeta de compilación
  mkdir build
  cd build

  # Ejecuta CMake para configurar el proyecto
  cmake ..

  # Compila el proyecto
  make

  # (Opcional) Instala el proyecto
  sudo make install

