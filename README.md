<div align="center">

<img src="docs/screenshots/icone.png" alt="Ícone" width="128">

# 🔥 Naruto Shippuden: Ultimate Ninja Storm 3 Full Burst — Port Nativo

**O jogo de Xbox 360 rodando nativamente no Android (ARM64) e no PC (Windows x64), sem emulador de CPU.**

![Android](https://img.shields.io/badge/Android-11%2B-3DDC84?logo=android&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D6?logo=windows&logoColor=white)
![Arquitetura](https://img.shields.io/badge/arm64--v8a-64%20bits-orange)
![Gráficos](https://img.shields.io/badge/Vulkan-1.1-AC162C?logo=vulkan&logoColor=white)
![Estado](https://img.shields.io/badge/estado-em%20desenvolvimento-yellow)

[Sobre](#-sobre) · [Versão do jogo](#-versão-do-jogo-obrigatória) · [Requisitos](#-requisitos) · [Perguntas](#-perguntas-frequentes)

</div>

---

## 📖 Sobre

Este port **não é um emulador de Xbox 360**. O executável do jogo (`default.xex`) é **recompilado estaticamente** de PowerPC para ARM64 (celular) e x86-64 (PC): o resultado é código nativo, que roda direto no processador. A parte gráfica usa um backend Vulkan, otimizado para GPUs de celular.

> [!IMPORTANT]
> **Os pacotes não contêm nenhum arquivo do jogo.** Você precisa da sua **própria cópia** de *Naruto Shippuden: Ultimate Ninja Storm 3 Full Burst* para Xbox 360, na versão indicada em [Versão do jogo](#-versão-do-jogo-obrigatória).

> [!NOTE]
> **Estado: em desenvolvimento.** Os pacotes (APK e Windows) ainda não foram publicados. Este repositório já está organizado com a documentação; os downloads aparecerão na página de **Releases** quando houver uma versão estável.

### ✨ O que o port oferece

- Recompilação estática do jogo para **ARM64** e **x86-64**, sem interpretador de CPU.
- Menu inicial próprio, com escolha da pasta do jogo, resolução e opções gráficas.
- Antisserrilhado **FXAA** e escala **FSR / CAS** (AMD FidelityFX), opcionais.
- **Controles na tela** com editor (mover, redimensionar, esconder e ajustar a transparência).
- **Drivers de GPU customizados (Turnip)** em celulares **Snapdragon**, importados pelo menu.
- Painel de desempenho (FPS, resolução, CPU, GPU e RAM) e botão de enviar log.
- Versão de **PC** com janela ou tela cheia, teclado e controles de Xbox ou PlayStation.

## 📱 Requisitos

### Android

| | Mínimo | Recomendado |
|---|---|---|
| **Android** | 11 (API 30) | 13 ou mais novo |
| **Processador** | ARM64 (arm64-v8a) | Snapdragon 8 Gen 1 / Dimensity 8000 ou superior |
| **GPU** | Vulkan 1.1 | Mali-G710 / Adreno 730 ou superior |
| **RAM** | 4 GB | 8 GB ou mais |
| **Espaço** | espaço dos arquivos do jogo | — |

### 🖥️ PC

| | Mínimo | Recomendado |
|---|---|---|
| **Sistema** | Windows 10 64 bits | Windows 11 |
| **Processador** | x86-64 com AVX | 4 núcleos ou mais |
| **Placa de vídeo** | Vulkan 1.1 (drivers atualizados) | GTX 1060 / RX 580 ou superior |
| **RAM** | 4 GB | 8 GB ou mais |

## 💿 Versão do jogo (obrigatória)

O port é feito para **uma versão específica** do executável. O código é recompilado a partir deste arquivo, então o que vale é o `default.xex` ser **idêntico**: confira o hash abaixo.

| Campo | Valor |
|---|---|
| Jogo | Naruto Shippuden: Ultimate Ninja Storm 3 Full Burst (Xbox 360) |
| Title ID | `4E4D085C` |
| Media ID | `2576927D` |
| Versão do executável | `0.0.0.9` |

| Arquivo | Tamanho | SHA-1 | MD5 |
|---|---|---|---|
| `default.xex` | 11.218.944 bytes | `f7ad65e26a00df6c29c9d34b291819593e455e9f` | `fd8ac164bcc8e380e84644402b6a0666` |

<details>
<summary><b>Como conferir o hash</b></summary>

- **Windows (PowerShell):** `Get-FileHash default.xex -Algorithm SHA1`
- **Linux / macOS:** `sha1sum default.xex`
- **Android:** qualquer app de "hash checker" da Play Store.

</details>

## ❓ Perguntas frequentes

<details>
<summary><b>Quando sai o primeiro download?</b></summary>

Ainda não há data. Quando houver um pacote estável, ele será publicado em **Releases** com as instruções de instalação.

</details>

<details>
<summary><b>Funciona com outra versão ou região do disco?</b></summary>

Só se o `default.xex` for **idêntico** (mesmo SHA-1 da tabela). Com hash diferente, não funciona.

</details>

<details>
<summary><b>O código-fonte está disponível?</b></summary>

Não. Este é um projeto de código fechado. Os componentes de código aberto usados estão listados abaixo, com as respectivas licenças.

</details>

## 🙏 Créditos

Este projeto só foi possível graças a estes projetos de código aberto:

- [**XenonRecomp**](https://github.com/hedge-dev/XenonRecomp): recompilador estático de PowerPC (Xbox 360)
- [**Xenia Canary**](https://github.com/xenia-canary/xenia-canary): referência do hardware do Xbox 360 e base do backend Vulkan
- [**SDL 3**](https://github.com/libsdl-org/SDL): janela, entrada e áudio
- [**FFmpeg**](https://ffmpeg.org): decodificação de áudio XMA
- [**AMD FidelityFX FSR / CAS**](https://github.com/GPUOpen-Effects): escala e nitidez
- [**libadrenotools**](https://github.com/bylaws/libadrenotools): drivers de GPU customizados no Android

As licenças completas estão em [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## ⚖️ Aviso legal

Este é um projeto de fãs, **sem fins lucrativos**, sem nenhuma ligação com a Bandai Namco, a CyberConnect2, a Ubisoft, a VIZ Media, Masashi Kishimoto ou a Microsoft. *Naruto* e *Naruto Shippuden: Ultimate Ninja Storm 3 Full Burst* são marcas e obras de seus respectivos donos.

Os pacotes **não incluem** arquivos, vídeos, sons ou texturas do jogo: é preciso ter a sua própria cópia original. Não peça nem compartilhe arquivos do jogo nas issues.

---

<div align="center">
Feito com 🧡
</div>
