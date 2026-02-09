# 🎮 Projeto Jogo em Python (POO) — Batalha por Turnos

Este repositório contém um **mini jogo de batalha por turnos no terminal**, desenvolvido em **Python** com foco na prática de **Programação Orientada a Objetos (POO)**.

O jogo simula um combate entre um **Herói** (controlado pelo usuário) e um **Inimigo** (controlado pelo jogo). A cada rodada, o jogador escolhe entre **ataque normal** e **ataque especial**, enquanto o inimigo revida automaticamente. Os danos são calculados com base no **nível** do personagem e possuem variação aleatória para deixar a batalha mais dinâmica.

---

## 🧠 Conceitos de POO aplicados

O projeto foi estruturado com classes e herança para representar os elementos do jogo:

- **Encapsulamento**: atributos privados (`__nome`, `__vida`, `__nivel`) com métodos de acesso (`get_nome`, `get_vida`, `get_nivel`).
- **Herança**: `Heroi` e `Inimigo` herdam de `Personagem`.
- **Polimorfismo (sobrescrita)**: método `exibir_detalhes()` é redefinido em `Heroi` e `Inimigo`.
- **Abstração por composição**: a classe `Jogo` atua como orquestradora da lógica da batalha.

---

## ⚔️ Como funciona o jogo

### Personagens
- **Personagem (classe base)**  
  Contém nome, vida e nível, além de:
  - `atacar(alvo)`: dano aleatório baseado no nível
  - `receber_ataque(dano)`: reduz a vida sem permitir valores negativos
  - `exibir_detalhes()`: mostra status do personagem

- **Herói**
  - Possui uma **habilidade especial**
  - Pode executar:
    - Ataque normal
    - **Ataque especial** (`ataque_especial`) com dano maior

- **Inimigo**
  - Possui um **tipo** (ex.: "Voador")

### Batalha por turnos
1. O jogo exibe os detalhes do herói e do inimigo.
2. O usuário escolhe:
   - `1` → Ataque normal
   - `2` → Ataque especial
3. Se o inimigo ainda estiver vivo, ele ataca o herói.
4. O combate termina quando a vida de um deles chega a 0.

---

## 🎯 Funcionalidades

- ✅ Batalha por turnos no console
- ✅ Escolha de ataque pelo jogador (normal ou especial)
- ✅ Dano variável com `random` baseado no nível do personagem
- ✅ Exibição de status (nome, vida, nível + habilidade/tipo)
- ✅ Mensagens de vitória/derrota ao final

---

## 🛠️ Tecnologias utilizadas

- **Python 3**
- Biblioteca padrão: `random`

---

## 📁 Estrutura do projeto

```text
Projeto-Jogo-Python/
├── jogo.py
└── README.md
