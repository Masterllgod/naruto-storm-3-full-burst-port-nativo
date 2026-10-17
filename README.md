<div align="center">

<img src="docs/screenshots/icone.png" alt="Ícone" width="128">

# 🐸 Naruto Shippuden: Ultimate Ninja Storm 3 Full Burst — Port Nativo

**O jogo de Xbox 360 rodando nativamente no Android (ARM64) e no PC (Windows x64), sem emulador de CPU.**

![Android](https://img.shields.io/badge/Android-11%2B-3DDC84?logo=android&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D6?logo=windows&logoColor=white)
![Arquitetura](https://img.shields.io/badge/arm64--v8a-64%20bits-orange)
![Gráficos](https://img.shields.io/badge/Vulkan-1.1-AC162C?logo=vulkan&logoColor=white)
![Versão](https://img.shields.io/badge/vers%C3%A3o-0.3-blue)

[**⬇️ Baixar (Android e PC)**](../../releases/latest) · [Requisitos](#-requisitos) · [Instalação](#-instalação) · [Configurações](#%EF%B8%8F-configurações) · [Perguntas](#-perguntas-frequentes)

<img src="docs/screenshots/menu-pc.jpg" alt="Menu inicial" width="90%">

</div>

---

## 📖 Sobre

Este port **não é um emulador de Xbox 360**. O executável do jogo (`default.xex`) foi **recompilado estaticamente** de PowerPC para ARM64 (celular) e x86-64 (PC): o resultado é código nativo, que roda direto no processador. A parte gráfica usa um backend Vulkan adaptado e otimizado para GPUs de celular (Mali e Adreno), com um **render nativo** que faz as cópias e limpezas da memória de vídeo do Xbox 360 direto na GPU.

> [!IMPORTANT]
> **O APK e o pacote de PC não contêm nenhum arquivo do jogo.** Você precisa da sua **própria cópia** de *Naruto Shippuden: Ultimate Ninja Storm 3 Full Burst* para Xbox 360, na versão indicada em [Versão do jogo](#-versão-do-jogo-obrigatória).

### ✨ Destaques

- **Lutas a 30 FPS** (o limite do próprio jogo), com o conteúdo do **Full Burst** carregado.
- **⚡ Modo desempenho:** 24 FPS estáveis e com ritmo uniforme, mais leve, para celulares que não seguram 30. Fica em destaque no topo do menu, e a lógica do jogo acompanha o relógio (sem câmera lenta).
- **Resoluções no celular:** 360p, 540p, 720p e 1080p (nítido). No PC também há 2K e 4K.
- **Antisserrilhado FXAA e FXAA+** e **escala FSR 1.0 / CAS** da AMD, que podem ser ligados e desligados.
- **Controles na tela com o tema do Jiraiya** 🐸: cada botão é um selo de pergaminho com aro vermelho e as marcas do selo, que giram e brilham com o chakra verde do Monte Myoboku ao apertar.
- **Pensados para as lutas do Storm:** soco, pulo, ferramentas ninja, chakra, defesa, substituição e os dois suportes, mais **atalhos de um toque** para jutsu (術), jutsu secreto (奥) e corrida de chakra.
- **🎛️ Editor de controles** (botão ⚙): mova, aumente, diminua ou esconda cada botão, ajuste a transparência e escolha a **área da tela onde o analógico funciona**.
- **Drivers de GPU customizados (Turnip)** em celulares **Snapdragon**, importados direto pelo menu.
- **Áudio sem picotes** nas quedas, jutsus e suportes.
- **Painel de desempenho:** FPS, resolução e uso de CPU, GPU e RAM. Pode ser arrastado pela tela ou recolhido.
- **Modo 16:9 ou esticado** para a tela inteira.
- Menu inicial animado com tema do **Jiraiya** 🐸, o mesmo no celular e no PC: o Monte Myoboku ao entardecer, folhas e chakra dourado em volta do selo do 油, com os olhos do sapo espiando.
- **Versão de PC** com janela ou tela cheia, teclado e controles de Xbox ou PlayStation.

## 📸 Capturas

| Tela de título | Modos de jogo |
|:---:|:---:|
| <img src="docs/screenshots/titulo.jpg" width="100%"> | <img src="docs/screenshots/modos.jpg" width="100%"> |
| **Seleção de personagens** | **Antes da luta** |
| <img src="docs/screenshots/selecao.jpg" width="100%"> | <img src="docs/screenshots/versus.jpg" width="100%"> |
| **Luta** | |
| <img src="docs/screenshots/luta.jpg" width="100%"> | |

## 📱 Requisitos

### Android

| | Mínimo | Recomendado |
|---|---|---|
| **Android** | 11 (API 30) | 13 ou mais novo |
| **Processador** | ARM64 (arm64-v8a) | Snapdragon 8 Gen 1 / Dimensity 8000 ou superior |
| **GPU** | Vulkan 1.1 | Mali-G710 / Adreno 730 ou superior |
| **RAM** | 4 GB | 8 GB ou mais |
| **Espaço** | ~7 GB (arquivos do jogo) | — |

### 🖥️ PC

| | Mínimo | Recomendado |
|---|---|---|
| **Sistema** | Windows 10 64 bits | Windows 11 |
| **Processador** | x86-64 com AVX | 4 núcleos ou mais |
| **Placa de vídeo** | Vulkan 1.1 (drivers atualizados) | GTX 1060 / RX 580 ou superior (2K e 4K: RTX 3060 / RX 6700 ou superior) |
| **RAM** | 4 GB | 8 GB ou mais |

## 💿 Versão do jogo (obrigatória)

O port foi feito para **uma versão específica** do executável, a do **disco norte-americano** 🇺🇸🇨🇦. O código foi recompilado a partir deste arquivo, então o que vale é o `default.xex` ser **idêntico**: confira o hash abaixo.

| Campo | Valor |
|---|---|
| Jogo | Naruto Shippuden: Ultimate Ninja Storm 3 Full Burst (Xbox 360) |
| **Região do disco** | **América do Norte, NTSC-U** |
| Title ID | `4E4D085C` |
| Media ID | `2576927D` |
| Versão do executável | `0.0.0.9` |
| Trava de região do executável | somente NTSC-U (América do Norte) |

| Arquivo | Tamanho | SHA-1 | MD5 |
|---|---|---|---|
| `default.xex` | 11.218.944 bytes | `f7ad65e26a00df6c29c9d34b291819593e455e9f` | `fd8ac164bcc8e380e84644402b6a0666` |

<details>
<summary><b>Como conferir o hash</b></summary>

- **Windows (PowerShell):** `Get-FileHash default.xex -Algorithm SHA1`
- **Linux / macOS:** `sha1sum default.xex`
- **Android:** qualquer app de "hash checker" da Play Store.

</details>

### Estrutura da pasta do jogo

Extraia o disco e copie **a pasta inteira** para o celular. Ela precisa ter:

```
Naruto Shippuden Ultimate Ninja Storm 3 Full Burst/
├── default.xex        ← executável (precisa bater com o hash acima)
├── nxeart
├── AvatarAssetPack
├── data/              ← dados do jogo
└── datafb/            ← conteúdo do Full Burst
```

## 🚀 Instalação

### Android

1. Baixe o **APK** na página de [**Releases**](../../releases/latest) e instale. Talvez seja preciso permitir *"instalar apps de fontes desconhecidas"*.
2. Copie a pasta do jogo para o celular, por exemplo `Armazenamento interno/Jogos/Naruto Storm 3 Full Burst`.
3. Abra o app e toque em **ESCOLHER PASTA**.
4. Permita o **acesso a todos os arquivos**: o jogo lê os dados direto da pasta, sem copiar nada.
5. Escolha a pasta que contém o `default.xex`.
6. Ajuste as configurações e toque em **JOGAR** 🐸

### 🖥️ PC (Windows)

1. Baixe o **`.zip` do Windows** na página de [**Releases**](../../releases/latest) e extraia numa pasta.
2. Abra **`NarutoStorm3FullBurst.exe`**.
3. Clique em **ESCOLHER PASTA** e escolha a pasta do jogo, a que contém o `default.xex`.
4. Ajuste as configurações e clique em **JOGAR** (ou aperte Enter).

As configurações, os saves e o cache de shaders ficam na pasta onde você extraiu o port (`naruto.ini`, `data/`, `cache/`), não na pasta do jogo.

> [!TIP]
> Na primeira vez que cada cena aparece, o jogo compila shaders e pode engasgar um pouco. Nas próximas vezes eles já ficam salvos.

## ⚙️ Configurações

| Opção | O que faz | Impacto no desempenho |
|---|---|---|
| **Resolução 360p / 540p** | Renderiza com menos pixels | 🟢 Mais FPS: ideal para celulares mais fracos |
| **Resolução 720p** | Resolução original do Xbox 360 | ⚪ Padrão |
| **Resolução 1080p** | Imagem mais nítida na tela do celular | 🟠 Pesa um pouco a mais |
| **Resolução 2K / 4K** (PC) | Renderiza com 4x a 9x mais pixels | 🔴 Bem mais pesado |
| **Tela: 16:9 / Esticar** | Mantém a proporção original ou estica para a tela toda | ⚪ Nenhum |
| **Antisserrilhado: FXAA / FXAA+** | Suaviza as bordas serrilhadas | 🟠 Pesa um pouco a mais |
| **Escala na tela: FSR / CAS** | Amplia a imagem com mais nitidez (AMD FidelityFX) | 🟠 Pesa um pouco a mais |
| **⚡ Modo desempenho** (Android) | 24 FPS estáveis, até 540p, sem antisserrilhado e com escala simples | 🟢 Bem mais leve |
| **Painel de FPS** | Mostra FPS, resolução, CPU, GPU e RAM | ⚪ Quase nenhum |
| **Driver da GPU** (só Snapdragon) | Usa o driver do sistema ou um driver **Turnip** importado (`.zip` no formato AdrenoTools) | Depende do aparelho e do driver |

> [!NOTE]
> Se o FPS cair, ligue o **⚡ Modo desempenho**, ou use **Antisserrilhado: Off** e **Escala: Normal** e baixe a resolução.

## 🎮 Controles

- **Andar:** encoste o dedo na área do analógico (por padrão, a **metade esquerda** da tela). O analógico aparece ali e segue o dedo.
- **Botões** (com a letra do controle num selinho, porque as dicas do jogo falam "aperte B"):

| Ícone | Botão | Na luta |
|---|---|---|
| 👊 Punho (o maior) | B | Ataque |
| 🦘 Pulo | A | Pular |
| ✴️ Shuriken | X | Ferramentas ninja |
| 🌀 Espiral | Y | Chakra |
| 🛡️ Escudo (hexágono) | RT | Defesa |
| 🪵 Tronco (hexágono) | LT | Substituição |
| 👥 Suportes | LB / RB | Chamar os suportes |
| 術 (atalho) | Y, B | Jutsu |
| 奥 (atalho) | Y, Y, B | Jutsu secreto |
| 🏃 (atalho) | Y, A | Corrida de chakra |
| Direcional | ↑ ↓ ← → | Itens |
| ☰ / ⏸️ | BACK / START | Menu / pausa |

- **⚙ Editor de controles:** toque na engrenagem no topo. Arraste os botões, toque num deles para mudar o tamanho ou escondê-lo, ajuste a transparência e arraste os cantos do retângulo para mudar a área do analógico. **Restaurar padrão** volta tudo ao original.
- O botão do **olho** esconde os controles e o **⇔** alterna entre 16:9 e tela esticada.
- **Controle físico:** controles Bluetooth e USB compatíveis com Android são reconhecidos automaticamente.

### 🖥️ PC

Controles de Xbox e PlayStation funcionam direto. No teclado:

| Tecla | Botão | Tecla | Botão |
|---|---|---|---|
| **W A S D** | Analógico esquerdo | **Setas** | Analógico direito |
| **I J K L** | Direcional | **Enter** / **Tab** | START / BACK |
| **Espaço** | A | **E** | B |
| **Q** | X | **F** | Y |
| **1** / **3** | LB / RB | **Z** / **C** | LT / RT |
| **Ctrl esq. / dir.** | Apertar os analógicos | **F11** / **Alt+Enter** | Tela cheia |

## ❓ Perguntas frequentes

<details>
<summary><b>O jogo fecha ao abrir / tela preta</b></summary>

- Confira se o `default.xex` bate com o hash acima.
- Confira se a permissão de **acesso a todos os arquivos** foi dada.
- Confira se a pasta escolhida é a que contém o `default.xex`, e não uma pasta acima dela.
- Se você trocou o **Driver da GPU**, volte para **Sistema**.
- No Android, o botão **Enviar log** do menu manda o registro do que aconteceu: anexe-o quando abrir uma issue.

</details>

<details>
<summary><b>Dá para jogar a 60 FPS?</b></summary>

Não. O jogo original conta o tempo em quadros, travado em 30 por segundo: a 60 ele simplesmente roda duas vezes mais rápido. 30 FPS estáveis é o mesmo do Xbox 360.

</details>

<details>
<summary><b>Qual driver Turnip usar? Funciona no meu Mali?</b></summary>

A opção **Driver da GPU** só aparece em celulares **Snapdragon** (Adreno): os drivers Turnip são feitos para eles. Importe um `.zip` no formato do AdrenoTools pelo próprio menu. Se o jogo fechar com um driver novo, o menu oferece voltar para o driver do sistema. Em celulares com GPU Mali o jogo usa sempre o driver do sistema.

</details>

<details>
<summary><b>Funciona com a versão europeia (PAL) ou de outro disco?</b></summary>

A versão testada é a **norte-americana (NTSC-U)**. O código foi recompilado a partir desse `default.xex`, então outro disco só funciona se o `default.xex` dele for **idêntico** (mesmo SHA-1 da tabela). Se o hash for diferente, não funciona.

</details>

<details>
<summary><b>Funciona em celulares 32 bits ou x86? E em Linux ou macOS?</b></summary>

Não. Por enquanto só Android arm64-v8a e Windows x64.

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

As licenças completas estão em [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) e também dentro do app, no link **"Licenças"** do menu.

## ⚖️ Aviso legal

Este é um projeto de fãs, **sem fins lucrativos**, sem nenhuma ligação com a Bandai Namco, a CyberConnect2, a Ubisoft, a VIZ Media, Masashi Kishimoto ou a Microsoft. *Naruto* e *Naruto Shippuden: Ultimate Ninja Storm 3 Full Burst* são marcas e obras de seus respectivos donos.

O APK **não inclui** arquivos, vídeos, sons ou texturas do jogo: é preciso ter a sua própria cópia original. Não peça nem compartilhe arquivos do jogo nas issues.

---

<div align="center">
Feito com 🧡 e muito óleo de sapo (油).
</div>
