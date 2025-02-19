## 🛠️ 1. Descargar un modelo
Para usar `llama.cpp`, necesitas un modelo GGUF. Descarga uno desde [Hugging Face](https://huggingface.co/Qwen), por ejemplo:

```bash
mkdir -p /models
cd /models
wget https://huggingface.co/Qwen/Qwen2-VL-7B-GGUF/resolve/main/Qwen2-VL-7B-Instruct-Q4_0.gguf
wget https://huggingface.co/Qwen/Qwen2-VL-7B-GGUF/resolve/main/mmproj-Qwen2-VL-7B-Instruct-f32.gguf
```

---

## 🔍 2. Probar el modelo
Para verificar que todo funciona correctamente, ejecuta:

```bash
cd ~/llama.cpp/build/bin
./llama-qwen2vl-cli -m /models/Qwen2-VL-7B-Instruct-Q4_0.gguf --mmproj /models/mmproj-Qwen2-VL-7B-Instruct-f32.gguf -p 'Describe this image.' --image '/models/test.jpg'
```

---

