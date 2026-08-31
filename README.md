# 📇 Agenda de Contatos - *Projeto Didático em Java*

![Java Version](https://img.shields.io/badge/Java-11%2B-orange?style=flat-square&logo=openjdk)
![Course](https://img.shields.io/badge/Disciplina-POO-blue?style=flat-square)
![Institution](https://img.shields.io/badge/IFCE-Campus%20Maranguape-green?style=flat-square)
![Current Version](https://img.shields.io/badge/Vers%C3%A3o-v0.0.0-informational?style=flat-square)

## 📌 Sobre o Repositório

Este repositório faz parte do projeto **Agenda de Contatos**, desenvolvido como material didático e prático para a disciplina de **Programação Orientada a Objetos (POO)** do **4º semestre** do *Instituto Federal de Educação, Ciência e Tecnologia do Ceará (IFCE) — Campus Maranguape*.

O objetivo central é construir uma aplicação Java de forma **incremental e evolutiva**. Através dessa abordagem, o estudante acompanha na prática o surgimento de novos problemas de software e compreende a real necessidade de aplicar novas estruturas de dados, boas práticas e paradigmas da programação.

---

## 🎯 Versão Atual: `v0.0.0`

### Finalidade Didática
A versão **`v0.0.0`** é o ponto de partida (*kickoff*) da aplicação. Nela, a agenda é capaz de armazenar **apenas um único contato por vez**, utilizando variáveis primitivas e do tipo `String`. 

> ⚠️ **Limitação Proposital:** Ao cadastrar um novo contato, os dados do contato anterior são sobrescritos. Esta limitação serve como elemento motivador para o estudo de **Arrays** e **Coleções (Collections)** nas versões seguintes.

---

## 🛠️ Funcionalidades Implementadas

- [x] **Adicionar Contato:** Recebe nome e telefone do contato (sobrescreve o existente).
- [x] **Listar Contato:** Exibe os dados do contato armazenado, se houver.
- [x] **Buscar Contato:** Verifica se o contato armazenado corresponde ao nome pesquisado.
- [x] **Excluir Contato:** Limpa os dados da memória.
- [x] **Sair:** Finaliza a execução do programa em loop.

---

## 🧠 Conceitos de Programação Trabalhados

Nesta primeira versão, são consolidados os conceitos fundamentais da linguagem Java:

* **Tipos de Dados & Variáveis:** Declaração e manipulação de `String`, `int` e `boolean`.
* **Entrada de Dados:** Leitura interativa do terminal via classe `java.util.Scanner`.
* **Fluxo de Controle:** 
  * Estruturas condicionais (`if-else`).
  * Seleção múltipla com `switch-case` para o menu interativo.
  * Estrutura de repetição `while` mantendo a aplicação ativa.
* **Manipulação de Strings:** Uso de métodos utilitários como `.equalsIgnoreCase()` e `.isEmpty()`.

---

## 🚀 Roadmap de Evolução do Projeto

O projeto evoluirá através das seguintes fases pedagógicas:

| Versão | Mecanismo de Armazenamento | Conceitos Aprendidos | Limitação / Evolução |
| :---: | :--- | :--- | :--- |
| **`v0.0.0`** *(Atual)* | Variáveis Simples (`String`) | `Scanner`, `if-else`, `switch-case`, `while` | Armazena apenas 1 contato por vez. |
| **`v0.1.0`** | Arrays (Vetores) | Índices, tamanho fixo, laços `for` / `foreach` | Armazena múltiplos contatos, porém com capacidade estática. |
| **`v0.2.0`** | `List` + `ArrayList` | Coleções dinâmicas, métodos `add()`, `get()`, `remove()`, `size()` | Armazenamento dinâmico sem limite pré-definido. |
| **`v0.3.0`** | `List` + `ArrayList` (Avançado) | Atualização de dados com `set()`, refatoração | Conclusão das quatro operações do **CRUD**. |

---

## 💻 Como Executar

### Pré-requisitos
* Java Development Kit (JDK) 11 ou superior instalado.
* Git para clonar o repositório (opcional).

### Passo a Passo

1. **Clone o repositório** (ou faça o download do código-fonte):
   ```bash
   git clone [https://github.com/seu-usuario/agenda-contatos.git](https://github.com/seu-usuario/agenda-contatos.git)
   cd agenda-contatos