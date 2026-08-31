# 📇 Agenda de Contatos - *Projeto Didático em Java*

![Java Version](https://img.shields.io/badge/Java-14%2B-orange?style=flat-square&logo=openjdk)
![Course](https://img.shields.io/badge/Disciplina-POO-blue?style=flat-square)
![Institution](https://img.shields.io/badge/IFCE-Campus%20Maranguape-green?style=flat-square)
![Current Version](https://img.shields.io/badge/Vers%C3%A3o-v0.2.0-informational?style=flat-square)

## 📌 Sobre o Repositório

Este repositório faz parte do projeto **Agenda de Contatos**, desenvolvido como material didático e prático para a disciplina de **Programação Orientada a Objetos (POO)** do **4º semestre** do *Instituto Federal de Educação, Ciência e Tecnologia do Ceará (IFCE) — Campus Maranguape*.

O objetivo central é construir uma aplicação Java de forma **incremental e evolutiva**. Através dessa abordagem, o estudante acompanha na prática o surgimento de novos problemas de software e compreende a real necessidade de aplicar novas estruturas de dados, boas práticas e paradigmas da programação.

---

## 🎯 Versão Atual: `v0.2.0`

### Finalidade Didática
A versão **`v0.2.0`** introduz a transição de arrays de tamanho fixo para **coleções dinâmicas** com `List` e `ArrayList`. 

Nesta etapa, elimina-se a necessidade de definir uma capacidade máxima prévia para a agenda, permitindo o armazenamento flexível de contatos conforme a demanda. Além disso, a versão descontinua controles manuais que se tornaram obsoletos — como variáveis contadoras de elementos e algoritmos manuais de deslocamento de memória na exclusão.

---

## 🛠️ Funcionalidades Implementadas

- [x] **Adicionar Contato:** Insere um novo registro de forma dinâmica (sem limite rígido de capacidade).
- [x] **Listar Todos os Contatos:** Percorre a lista exibindo todos os contatos cadastrados.
- [x] **Procurar Contato:** Realiza busca linear por nome percorrendo a coleção.
- [x] **Excluir Contato:** Remove o contato por índice e delega a reorganização dos elementos à própria lista.
- [x] **Sair:** Finaliza o programa.

---

## 🧠 Conceitos de Programação Trabalhados

Nesta versão, os alunos entram em contato com a API de Coleções do Java (*Java Collections Framework*):

* **Interface e Implementação:** Uso da interface `java.util.List` com a implementação `java.util.ArrayList`.
* **Gerenciamento Dinâmico de Memória:** Alocação de dados com crescimento e encolhimento automático.
* **Manipulação de Coleções:**
  * `.add()` — Adiciona um elemento ao final da lista.
  * `.get(index)` — Recupera o elemento em uma posição específica.
  * `.remove(index)` — Exclui o elemento e reorganiza os índices automaticamente.
  * `.size()` — Retorna o número total de elementos armazenados.
* **Análise Comparativa:** Avaliação prática das diferenças entre Arrays estáticos e `ArrayList`.

---

## 🔄 Comparativo: `v0.1.0` (Array) ➡️ `v0.2.0` (ArrayList)

| Operação / Recurso | Array (`v0.1.0`) | ArrayList (`v0.2.0`) |
| :--- | :--- | :--- |
| **Instanciação** | `new String[capacidade]` | `new ArrayList<>()` |
| **Capacidade** | Estática / Fixa | Dinâmica |
| **Inserção** | `nomes[cont] = nome` | `nomes.add(nome)` |
| **Acesso** | `nomes[i]` | `nomes.get(i)` |
| **Contagem** | Variável manual (`quantidade`) | `nomes.size()` |
| **Exclusão** | Deslocamento manual + ajuste final | `nomes.remove(i)` *(Automático)* |
| **Validação de Limite** | Necessária (`quantidade == capacidade`) | Desnecessária |

---

## 💡 Motivação para a Próxima Versão (`v0.3.0`)

A versão `v0.2.0` já contempla três das quatro operações fundamentais de um **CRUD**: *Create* (adicionar), *Read* (listar/buscar) e *Delete* (excluir). A operação de **Update (atualizar/editar)** é o elo que falta para completar o ciclo basilar.

> 🔍 **Reflexão para o futuro:** Atualmente, informações de um mesmo contato (como nome e telefone) continuam divididas em listas paralelas independentes. Esta limitação servirá como ponto de partida para a introdução da **Orientação a Objetos (Criação de Classes e Objetos)** nas etapas posteriores.

---

## 🚀 Roadmap de Evolução do Projeto

| Versão | Mecanismo de Armazenamento | Conceitos Aprendidos | Limitação / Evolução |
| :---: | :--- | :--- | :--- |
| **`v0.0.0`** | Variáveis Simples (`String`) | `Scanner`, `if-else`, `switch-case`, `while` | Armazena apenas 1 contato por vez. |
| **`v0.1.0`** | Arrays (`String[]`) | Índices, tamanho fixo, controle por contador, laço `for` | Permite múltiplos contatos, porém com capacidade estática. |
| **`v0.2.0`** *(Atual)* | `List` + `ArrayList` | Coleções dinâmicas, métodos `add()`, `get()`, `remove()`, `size()` | Armazenamento dinâmico sem limite estático. |
| **`v0.3.0`** | `List` + `ArrayList` (Avançado) | Atualização de dados com `set()`, refatoração | Conclusão das quatro operações do **CRUD**. |

---

## 💻 Como Executar

### Pré-requisitos
* **Java Development Kit (JDK) 14 ou superior** instalado (devido ao suporte à sintaxe moderna do `switch`).
* Git para clonar o repositório (opcional).

### Passo a Passo

1. **Clone o repositório** (ou navegue até a pasta da versão):
   ```bash
   git clone [https://github.com/seu-usuario/agenda-contatos.git](https://github.com/seu-usuario/agenda-contatos.git)
   cd agenda-contatos