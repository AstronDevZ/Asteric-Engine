# 🌌 Asteric Engine

**Asteric Engine** é uma game engine 3D leve, potente e modular em Java, desenvolvida com **LWJGL 3** (Lightweight Java Game Library). Projetada para ambientes Linux com foco de desenvolvimento no Visual Studio Code, ela oferece renderização 3D em tempo real, manipulação de física e um fluxo de trabalho intuitivo para a criação de jogos e simulações.

---

## 🚀 Funcionalidades

- **Renderização 3D Avançada:** Suporte a Shaders GLSL, carregamento de modelos 3D (`.obj`) e texturas.
- **Gerenciamento de Pipeline:** Contexto OpenGL modularizado via LWJGL 3.
- **Sistema de Input & Janelas:** Manipulação nativa de eventos e periféricos (teclado e mouse) usando GLFW.
- **Matemática 3D:** Operações vetoriais e matriciais integradas via [JOML](https://github.com/JOML-CI/JOML) (Java OpenGL Math Library).
- **Otimizado para Linux:** Configurado para rodar com máximo desempenho e baixo overhead no ecossistema Linux.

---

## 📋 Pré-requisitos

Antes de clonar e executar o projeto, certifique-se de ter os seguintes softwares instalados em seu sistema Linux:

1. **Java Development Kit (JDK 17 ou superior):**
   ```bash
   sudo apt update
   sudo apt install openjdk-17-jdk
   ```
2. **Build Tool (Gradle ou Maven):**
   * *Recomendado (Gradle):*
     ```bash
     sudo apt install gradle
     ```
3. **Visual Studio Code:**
   * Com as seguintes extensões instaladas:
     * **Extension Pack for Java** (Microsoft)
     * **Gradle for Java** (Microsoft)
4. **Drivers de Vídeo (Mesa / Nvidia / AMD):**
   * Certifique-se de ter suporte a **OpenGL 3.3+** habilitado.
     ```bash
     glxinfo | grep "OpenGL version"
     ```

---

## 📥 Como Baixar e Configurar

### 1. Clonar o Repositório

Abra o terminal e execute:

```bash
git clone https://github.com/seu-usuario/asteric-engine.git
cd asteric-engine
```

### 2. Abrir no VS Code

Abra o diretório do projeto no VS Code:

```bash
code .
```

O VS Code reconhecerá automaticamente a estrutura Java/Gradle. Aguarde o download das dependências do LWJGL.

---

## 🛠️ Como Executar e Buildar

### Via Terminal
Para compilar e iniciar a engine:

```bash
./gradlew run
```

Para gerar o arquivo executável (`.jar`):

```bash
./gradlew build
```

### Via VS Code
1. Abra a aba **Run & Debug** (`Ctrl + Shift + D`).
2. Selecione a configuração **"Run Asteric Engine"** e pressione `F5`.

---

## 🗂️ Estrutura do Projeto

```text
asteric-engine/
├── .vscode/               # Configurações de execução e debug do VS Code
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/asteric/
│   │   │       ├── core/       # Loop principal, janela e tempo
│   │   │       ├── graphics/   # Shaders, malhas, texturas e renderizador
│   │   │       ├── math/       # Utilitários de matrizes e vetores
│   │   │       └── Main.java   # Ponto de entrada da Engine
│   │   └── resources/
│   │       ├── shaders/        # Códigos fonte GLSL (Vertex e Fragment)
│   │       └── textures/       # Imagens e materiais
├── build.gradle           # Configuração das dependências do LWJGL e JOML
└── README.md
```

---

## 📄 Licença

Este projeto é distribuído sob a licença **MIT**. Veja o arquivo `LICENSE` para mais detalhes.
