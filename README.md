# Agenda de Contatos - v1.0.0

## Sobre o Repositório

Este repositório faz parte do projeto **Agenda de Contatos**, desenvolvido como material didático para a disciplina de **Programação Orientada a Objetos (POO)** do **4º semestre** do **Instituto Federal de Educação, Ciência e Tecnologia do Ceará - Campus Maranguape**.

O objetivo principal é construir um projeto em Java desde a base, de forma incremental, permitindo acompanhar a evolução da aplicação e compreender na prática a necessidade de novas estruturas, técnicas e paradigmas de programação.

## Versão Atual: v1.0.0

### Finalidade
A versão **v1.0.0** representa a primeira grande evolução arquitetural do projeto. Após dominar as operações de CRUD sobre coleções dinâmicas (`ArrayList`), esta versão introduz a **modularização do código** por meio de **métodos estáticos**. Todo o código que antes estava concentrado dentro do `main()` foi reorganizado em métodos especializados, cada um responsável por uma única funcionalidade da agenda.

Essa mudança prepara o terreno para a transição definitiva para a **Programação Orientada a Objetos**, onde os métodos deixarão de ser estáticos e migrarão para uma classe `Contato` própria.

### Funcionalidades
- **Adicionar contato** — cadastra nome, celular e e-mail
- **Listar contatos** — exibe todos os contatos cadastrados
- **Procurar contato** — busca por nome (ignora maiúsculas/minúsculas)
- **Alterar contato** — atualiza os dados de um contato existente
- **Excluir contato** — remove um contato da agenda
- **Sair** — encerra o programa

### Conceitos Trabalhados
- **Modularização** com métodos estáticos (`static`)
- **Separação de responsabilidades** — cada método executa uma tarefa específica
- **Passagem de parâmetros** (`Scanner`, `List<String>`)
- **Retorno de valores** (`int`, `boolean`)
- Reutilização de código (métodos reutilizáveis)
- Organização e legibilidade do código
- Manutenção do CRUD completo sobre `ArrayList`

## Evolução do Projeto

### O que mudou da V.0.3.0 para a v1.0.0?

| Aspecto | V.0.3.0 | v1.0.0 |
|:---|:---|:---|
| **Arquitetura** | Todo o código dentro do `main()` | Código dividido em métodos especializados |
| **Organização** | `switch` com blocos de código inline | `switch` chama métodos por nome |
| **Reutilização** | Código repetido ou acoplado | Métodos reutilizáveis e independentes |
| **Legibilidade** | Código extenso no `main()` | `main()` enxuto e descritivo |
| **Manutenção** | Alterações afetam o `main()` | Alterações isoladas em métodos específicos |
| **Paradigma** | Estruturado/procedural | Procedural modularizado |

### Métodos Introduzidos

| Método | Responsabilidade | Retorno |
|:---|:---|:---|
| `mostraInicializacao()` | Exibe o cabeçalho de boas-vindas | `void` |
| `mostraMenu()` | Exibe as opções do menu | `void` |
| `selecionaOpcao(Scanner)` | Lê e retorna a opção escolhida | `int` |
| `adicionar(...)` | Cadastra um novo contato nas listas | `void` |
| `listar(...)` | Exibe todos os contatos cadastrados | `void` |
| `pesquisar(...)` | Busca e exibe um contato pelo nome | `void` |
| `atualizar(...)` | Altera os dados de um contato existente | `void` |
| `excluir(...)` | Remove um contato das listas | `void` |
| `sair()` | Exibe mensagem de despedida e retorna `false` | `boolean` |

### Motivação para Próximas Versões
A v1.0.0 ainda utiliza **métodos estáticos** e mantém os dados de um contato separados em três `ArrayList`s distintos. A próxima evolução natural será a criação de uma **classe `Contato`**, que agrupará nome, celular e e-mail em um único objeto. Isso eliminará a necessidade de três listas paralelas e permitirá aplicar os pilares da POO:

- **Encapsulamento** — atributos privados com getters e setters
- **Construtores** — inicialização padronizada de objetos
- **Coleção de objetos** — `List<Contato>` em vez de três `List<String>`
- **Métodos de instância** — substituindo métodos estáticos

| Versão | Armazenamento / Arquitetura | O que o aluno aprende | Limitação/Evolução |
|:---|:---|:---|:---|
| V.0.0.0 | Variáveis simples | String, Scanner, if-else, switch-case, repetição | Apenas 1 contato |
| V.0.1.0 | Arrays | Vetores, índices, tamanho fixo e `for` | Capacidade fixa |
| V.0.2.0 | List + ArrayList | Coleções dinâmicas: `add()`, `get()`, `remove()`, `size()` | Sem capacidade fixa |
| V.0.3.0 | List + ArrayList | `set()` e CRUD completo | Código todo no `main()` |
| **v1.0.0** | **List + ArrayList + Métodos estáticos** | **Modularização, separação de responsabilidades, passagem de parâmetros** | **Métodos estáticos; dados ainda em 3 listas paralelas** |
| v1.1.0 (futura) | Classe `Contato` + encapsulamento | Orientação a Objetos: classe, atributos, métodos, construtor | — |

## Como Executar

1. Certifique-se de ter o **JDK 14+** instalado (devido ao uso do switch com `->`).
2. Compile o arquivo:
   ```bash
   javac br/edu/principal/Principal.java
   ```
3. Execute o programa:
   ```bash
   java br.edu.principal.Principal
   ```

---
**Professor:** Dr. Róger Moura Sarmento  
**Instituição:** IFCE - Campus Maranguape  
**Disciplina:** Programação Orientada a Objetos (POO) — 4º Semestre
