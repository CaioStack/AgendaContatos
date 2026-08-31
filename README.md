# 📇 Agenda de Contatos - *Projeto Didático em Java*

![Java Version](https://img.shields.io/badge/Java-11%2B-orange?style=flat-square&logo=openjdk)
![Course](https://img.shields.io/badge/Disciplina-POO-blue?style=flat-square)
![Institution](https://img.shields.io/badge/IFCE-Campus%20Maranguape-green?style=flat-square)
![Current Version](https://img.shields.io/badge/Vers%C3%A3o-v0.1.0-informational?style=flat-square)

## 📌 Sobre o Repositório

Este repositório faz parte do projeto **Agenda de Contatos**, desenvolvido como material didático e prático para a disciplina de **Programação Orientada a Objetos (POO)** do **4º semestre** do *Instituto Federal de Educação, Ciência e Tecnologia do Ceará (IFCE) — Campus Maranguape*.

O objetivo central é construir uma aplicação Java de forma **incremental e evolutiva**. Através dessa abordagem, o estudante acompanha na prática o surgimento de novos problemas de software e compreende a real necessidade de aplicar novas estruturas de dados, boas práticas e paradigmas da programação.

---

## 🎯 Versão Atual: `v0.1.0`

### Finalidade Didática
A versão **`v0.1.0`** representa a primeira grande evolução do projeto, introduzindo a capacidade de armazenar **múltiplos contatos simultaneamente** através do uso de **Arrays (vetores)** de tamanho estático.

Esta etapa explora o conceito de índices, o controle manual da quantidade de elementos cadastrados e a necessidade de reorganização da memória em operações de exclusão, evidenciando as limitações do uso de arrays de capacidade fixa em sistemas dinâmicos.

---

## 🛠️ Funcionalidades Implementadas

- [x] **Adicionar Contato:** Insere um novo contato no vetor (com validação de agenda cheia).
- [x] **Listar Todos os Contatos:** Percorre o array e exibe todos os contatos cadastrados.
- [x] **Procurar Contato:** Realiza busca linear por nome em todas as posições preenchidas.
- [x] **Excluir Contato:** Remove o contato desejado e realiza o deslocamento manual (*shift*) dos elementos à direita para não deixar lacunas no vetor.
- [x] **Sair:** Finaliza o programa.

---

## 🧠 Conceitos de Programação Trabalhados

Nesta versão, aprofundam-se os conceitos de estruturas de dados lineares e controle de memória estática:

* **Arrays Unidimensionais:** Declaração, alocação e manipulação de vetores (`String[]`).
* **Acesso por Índice:** Leitura e escrita de dados em posições específicas (`array[i]`).
* **Controle de Capacidade Limite:** Verificação utilizando a propriedade `.length` e uma variável contadora (`quantidade`).
* **Estruturas de Repetição:** Uso do laço `for` para percorrer, buscar e reorganizar o vetor.
* **Algoritmo de Remoção em Vetores:** Deslocamento manual de elementos subsequentes para preencher a posição excluída.

---

## 🔄 Comparativo: `v0.0.0` ➡️ `v0.1.0`

| Aspecto | Versão `v0.0.0` | Versão `v0.1.0` |
| :--- | :--- | :--- |
| **Armazenamento** | Variáveis simples (`String`) | Arrays de Strings (`String[]`) |
| **Capacidade** | Apenas 1 contato | Vários contatos (limite estático definido) |
| **Inclusão** | Sobrescreve a variável (`nome = ...`) | Atribuição por índice (`nomes[quantidade] = ...`) |
| **Listagem** | Impressão direta da variável | Percorre o vetor com laço `for` |
| **Busca** | Comparação direta simples | Percorre o vetor comparando posição a posição |
| **Exclusão** | Reseta/limpa as variáveis | Desloca os elementos à esquerda e decrementa contador |
| **Controle de Estado** | Nenhum | Variável `quantidade` monitora o total de registros |

---

## 💡 Motivação para a Próxima Versão (`v0.2.0`)

Apesar de permitir múltiplos registros, o uso de arrays impõe uma **capacidade pré-definida e rígida**. Se instanciarmos um vetor com tamanho 100, alocamos memória desnecessária para poucos contatos e impedimos o cadastro do 101º. Essa rigidez motivará a introdução do framework de coleções do Java (`List` e `ArrayList`) na próxima versão.

---

## 🚀 Roadmap de Evolução do Projeto

| Versão | Mecanismo de Armazenamento | Conceitos Aprendidos | Limitação / Evolução |
| :---: | :--- | :--- | :--- |
| **`v0.0.0`** | Variáveis Simples (`String`) | `Scanner`, `if-else`, `switch-case`, `while` | Armazena apenas 1 contato por vez. |
| **`v0.1.0`** *(Atual)* | Arrays (`String[]`) | Índices, tamanho fixo, controle por contador, laço `for` | Permite múltiplos contatos, porém com capacidade fixa. |
| **`v0.2.0`** | `List` + `ArrayList` | Coleções dinâmicas, métodos `add()`, `get()`, `remove()`, `size()` | Armazenamento dinâmico sem limite rígido pré-definido. |
| **`v0.3.0`** | `List` + `ArrayList` (Avançado) | Atualização de dados com `set()`, refatoração | Conclusão das quatro operações do **CRUD**. |

---

## 💻 Como Executar

### Pré-requisitos
* Java Development Kit (JDK) 11 ou superior instalado.
* Git para clonar o repositório (opcional).

### Passo a Passo

1. **Clone o repositório** (ou navegue até a pasta da versão):
   ```bash
   git clone [https://github.com/seu-usuario/agenda-contatos.git](https://github.com/seu-usuario/agenda-contatos.git)
   cd agenda-contatos