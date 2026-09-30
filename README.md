<div align="center">

# 🔵 voidbr-ollama-cuda

**https://github.com/VoidLinuxBR/voidbr-ollama-cuda**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

</div>

---

Bibliotecas **CUDA** do [Ollama](https://github.com/ollama/ollama) para o **VoidBR Linux**:
aceleração em placas **NVIDIA** para o [voidbr-ollama](https://github.com/voidlinuxbr/voidbr-ollama).

Vêm do mesmo tarball oficial do `voidbr-ollama` (sha256 conferido) e ficam num pacote
separado porque ocupam ~2,1 GB — quem não tem NVIDIA não precisa delas.

| Caminho | Tamanho |
|---|---|
| `/usr/lib/ollama/cuda_v12/` | ~1,3 GB |
| `/usr/lib/ollama/cuda_v13/` | ~850 MB |

O Ollama escolhe a versão conforme o driver NVIDIA instalado (pacote `nvidia`).

```bash
sudo xbps-install -S voidbr-ollama-cuda
sudo sv restart ollama
```

O assistente do **VoidBR AI** (`voidbr-ai --setup-ai`) instala este pacote sozinho quando
encontra uma placa NVIDIA.

> Atualize sempre junto com o `voidbr-ollama` (mesmo `pkgver`): as bibliotecas precisam
> ser da mesma versão do binário.
