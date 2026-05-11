# Cena 3D OpenGL — Atividade PA2 (Parte 2)

Projeto desenvolvido para a disciplina de **Computação Gráfica** da Universidade Franciscana (UFN).  
O objetivo é construir uma cena 3D interativa utilizando **OpenGL + Python**, adicionando múltiplos modelos 3D com translações, rotações, escalas e iluminação.

---

## 🎮 A Cena - Pré-View

A cena contém os seguintes objetos:

| Objeto | Arquivo | Posição na Cena |
|---|---|---|
| 🟫 **Cubo** (texturizado) | geometria procedural | Ao fundo, à direita |
| 🐱 **Gato** | `OBJS/Cat/Cat.obj` | Centro da cena |
| 😺 **Garfield** | `OBJS/Garfield/20430_Cat_v1_NEW.obj` | Esquerda |
| 🐢 **Tartaruga** | `OBJS/Tartaruga/13103_pearlturtle_v1_l2.obj` | Direita |

<img width="783" height="587" alt="Captura de tela de 2026-05-10 21-14-54" src="https://github.com/user-attachments/assets/a76db582-4e9f-48a1-af8d-f1190a2e4c10" />

<img width="783" height="587" alt="Captura de tela de 2026-05-10 21-15-13" src="https://github.com/user-attachments/assets/c80314a4-cd5d-4b2d-a109-0db952ac645a" />

<img width="783" height="587" alt="Captura de tela de 2026-05-10 21-15-35" src="https://github.com/user-attachments/assets/6000fa40-7cf5-4988-be26-1f1b00ebad3e" />

Todos os objetos possuem translações, rotações e escalas individuais, e a cena conta com um **chão de grama texturizado** e **duas fontes de luz** (branca e azulada).

### Controles

| Tecla / Ação | Função |
|---|---|
| `W A S D` | Mover câmera (frente/trás/lados) |
| `Page Up / Page Down` | Subir / descer |
| Mouse | Olhar ao redor (estilo FPS) |
| `Q / E` | Girar a cena no eixo Y |
| `R / F` | Inclinar a cena no eixo X |
| `ESC` | Fechar o programa |

---

## 🛠️ Como Rodar

### 1. Pré-requisitos

- Python **3.10+**
- `git`
- Sistema operacional **Linux** (testado no Ubuntu com driver Mesa/Intel)

### 2. Clonar o repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd PA2-parte2-computacao-grafica-objetos
```

### 3. Criar o ambiente virtual

```bash
python3 -m venv venv
```

### 4. Ativar o ambiente virtual

```bash
source venv/bin/activate
```

> Para desativar depois: `deactivate`

### 5. Instalar as dependências

```bash
pip install -r requirements.txt
```

### 6. Executar o projeto

```bash
SDL_VIDEODRIVER=x11 python3 Aula11_opengl_textura_camera_iluminacao.py
```

> ⚠️ O prefixo `SDL_VIDEODRIVER=x11` é necessário em sistemas Linux com driver Mesa para evitar erros de contexto EGL.

---

## 📦 Dependências

| Biblioteca | Versão | Função |
|---|---|---|
| `pygame` | 2.6.1 | Janela, input de teclado/mouse |
| `PyOpenGL` | 3.1.10 | Renderização 3D (OpenGL) |
| `Pillow` | 12.2.0 | Carregamento de texturas (imagens) |
| `PyWavefront` | 1.3.3 | Parser de arquivos `.obj` |
| `pyglet` | 2.1.14 | Suporte auxiliar OpenGL |

---

## 📁 Estrutura do Projeto

```
PA2-parte2-computacao-grafica-objetos/
│
├── Aula11_opengl_textura_camera_iluminacao.py   # Código principal
├── requirements.txt                              # Dependências Python
│
├── OBJS/                     # Modelos 3D
│   ├── Cat/                  # Gato (modelo base)
│   ├── Garfield/             # Garfield
│   └── Tartaruga/            # Tartaruga
│
└── Texturas/                 # Texturas da cena
    ├── textura.jpg           # Textura do cubo
    ├── textura-chao-grama/   # Chão de grama
    ├── textura-cubo1/
    ├── textura-cubo2/
    ├── textura-cubo3/
    └── textura-parede-tijolo/
```

---

## 👤 Autor

Desenvolvido por **Matheus Nogueira** — UFN, Computação Gráfica, 2025/1.
