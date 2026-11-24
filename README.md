# 📒 Agenda de Contatos

> **Projeto prático desenvolvido no IFCE – Campus Maranguape**  
> **Disciplina:** Programação Orientada a Objetos (POO)  
> **Aluno:** Caio | **Professor:** Prof. Roger

![Java](https://img.shields.io/badge/Java-17%2B-orange?style=flat-square&logo=openjdk)
![Instituição](https://img.shields.io/badge/IFCE-Campus%20Maranguape-green?style=flat-square)
![Status](https://img.shields.io/badge/Versão%20Atual-v5.1.0%20(MVC%20Completo%20View%20Loop)-blue?style=flat-square)

---

## 📌 Sobre o Projeto

Sistema de gerenciamento de contatos em Java construído de forma **incremental**: cada versão parte da anterior e acrescenta um conceito novo, evoluindo de variáveis simples até **MVC completo com View controlando o loop principal**, passando por coleções dinâmicas, modularização em classes dedicadas, persistência em arquivos, encapsulamento, organização em pacotes com DAO e separação Controller/View.

Cada pasta `vX.Y.Z` deste repositório é uma versão completa e executável, acompanhada de seu próprio `README.md` individual, permitindo acompanhar visualmente a evolução do código a cada etapa do aprendizado.

---

## ✨ Funcionalidades (v5.1.0)

| Funcionalidade | O que faz | Onde fica |
| :--- | :--- | :--- |
| ➕ **Adicionar** | Cadastra um contato com nome, celular e e-mail | `Agenda.adicionar()` |
| 📋 **Listar** | Mostra todos os contatos cadastrados | `Agenda.listar()` |
| 🔍 **Pesquisar** | Busca contatos por atributos | `Agenda.pesquisar()` |
| ✏️ **Atualizar** | Altera os dados de um contato existente | `Agenda.atualizar()` |
| 🗑️ **Excluir** | Remove um contato da coleção | `Agenda.excluir()` |
| 💾 **Persistência** | Carrega e salva automaticamente em `contatos.txt` | `ContatoDAO.carregarContatos()` e `ContatoDAO.salvarContatos()` |

---

## 📊 Evolução das Versões

| Versão | Abordagem | Principais Conceitos |
| :--- | :--- | :--- |
| **v0.0.0** | Variáveis simples | `Scanner`, `if/else`, `while`, 1 contato em memória |
| **v0.1.0** | Arrays | Vetores, índices, `for`, capacidade fixa |
| **v0.2.0** | List + ArrayList | Coleções dinâmicas: `add()`, `get()`, `remove()`, `size()` |
| **v0.3.0** | List + ArrayList | `set()` e CRUD completo |
| **v1.0.0** | Modularização procedural | Métodos estáticos, pacote `br.edu.principal` |
| **v1.1.0** | Separação de responsabilidades | Classes `Agenda`, `Uteis` e `Principal` |
| **v1.1.1** | Correção de bugs (patch) | Fluxo da opção Sair, buffer do `Scanner`, mensagens |
| **v2.1.0** | Persistência em arquivo TXT | Classe `Persistencia`, `java.io`, `contatos.txt` |
| **v3.0.0** | Classes e objetos | Entidade `Contato`, atributos, operador `new` |
| **v3.1.0** | Coleção de objetos | `List<Contato>`, `for-each`, Generics |
| **v3.2.0** | CRUD orientado a objetos | CRUD e persistência operando sobre `List<Contato>` |
| **v3.3.0** | Encapsulamento | `private`, construtor parametrizado, `this`, getters e setters |
| **v4.0.0** | DAO + Pacotes | `ContatoDAO`, pacotes `modelo/servico/dao/uteis`, imports, responsabilidade única |
| **v5.0.0** | MVC (Controller/View) | `AgendaController`, `AgendaView`, `ContatoDAO` instância, injeção de dependência, confirmação exclusão |
| **v5.1.0** ✅ | **MVC Completo (View Loop)** | View controla loop principal, `executar*()` delegam ao Controller, `Uteis` removido, `Principal` minimal |

---

## 📚 Histórico Detalhado de Versões

<details>
<summary><b>🔍 Clique para expandir o histórico detalhado de cada versão</b></summary>

### 🔹 Fase Procedural
* **v0.0.0 — Versão Inicial:** Armazenamento individual de um único contato utilizando variáveis locais e controle de fluxo simples.
* **v0.1.0 — Arrays:** Permite armazenar múltiplos contatos utilizando vetores (`String[]`) com capacidade fixa.
* **v0.2.0 — List e ArrayList:** Introdução a coleções dinâmicas da Java Collections Framework, eliminando a limitação de tamanho fixo.
* **v0.3.0 — Alteração de Contatos:** Inclusão de funcionalidade de pesquisa e alteração de registros com `set()`.
* **v1.0.0 — Modularização Procedural:** Organização do código em métodos estáticos dentro do pacote `br.edu.principal`.
* **v1.1.0 — Separação em Classes:** Distribuição de responsabilidades entre as classes `Agenda`, `Uteis` e `Principal`.
* **v1.1.1 — Patch de Correção:** Ajuste no buffer de leitura do `Scanner` e no fluxo de encerramento da opção Sair.

### 🔹 Fase de Persistência
* **v2.1.0 — Persistência em TXT:** Implementação da classe `Persistencia` utilizando o pacote `java.io` para salvar e carregar dados do arquivo `contatos.txt` no formato `nome;celular;email`.

### 🔹 Fase Orientada a Objetos
* **v3.0.0 — Introdução a Classes e Objetos:** Criação da classe `Contato` representando uma entidade com estado próprio.
* **v3.1.0 — Coleção de Objetos:** Uso de `List<Contato>` com Generics e percurso via `for-each`.
* **v3.2.0 — CRUD Orientado a Objetos:** Refatoração completa das operações de CRUD e persistência para operarem sobre instâncias da classe `Contato`.
* **v3.3.0 — Encapsulamento:** Proteção do estado interno da entidade `Contato` (`private`), construtor dedicado, controle de acesso via getters/setters e uso da palavra-chave `this`.

### 🔹 Fase Arquitetural
* **v4.0.0 — DAO e Organização em Pacotes:** Código organizado em pacotes Java (`modelo`, `servico`, `dao`, `uteis`, `principal`); introdução do padrão DAO com `ContatoDAO` substituindo `Persistencia`; métodos static com try-with-resources; separação de responsabilidades via imports.
* **v5.0.0 — MVC com Controller e View:** Separação completa da lógica de negócio (`AgendaController`) e interface (`AgendaView`); `ContatoDAO` passa a ser instância (não static) com caminho do arquivo configurável; injeção de dependência no `Principal`; confirmação antes de exclusão; métodos retornam `boolean` para indicar sucesso/falha.
* **v5.1.0 — MVC Completo com View Loop:** View assume o loop principal (`iniciar()`); métodos `executar*()` na View delegam ao Controller; `Uteis` removido (inicialização/sobre/encerramento movidos para View); `Principal` torna-se composition root minimal (apenas injeta dependências e chama `view.iniciar()`).

</details>

---

## 🗂️ Estrutura do Projeto

Uma pasta por versão, cada uma independente das outras:

```text
agenda_contatos/
├── v0.0.0/ ... v2.1.0/   # Evolução procedural, modularização e persistência TXT
├── v3.0.0/               # Introdução à classe Contato e objetos
├── v3.1.0/               # Testes e manipulação de List<Contato>
├── v3.2.0/               # CRUD e persistência orientados a objetos
├── v3.3.0/               # Encapsulamento (private, construtor, get/set)
├── v4.0.0/               # DAO + organização em pacotes
├── v5.0.0/               # MVC (Controller/View)
├── v5.1.0/               # Versão atual: MVC Completo (View Loop)
└── README.md
```

---

## 🏗️ Estrutura da Versão Atual (v5.1.0)

### Organização dos Arquivos

```text
v5.1.0/
├── README.md
└── src/
    └── br/
        └── edu/
            ├── principal/
            │   └── Principal.java
            ├── modelo/
            │   └── Contato.java
            ├── controle/
            │   └── AgendaController.java
            ├── visao/
            │   └── AgendaView.java
            └── dao/
                └── ContatoDAO.java
```

> **Nota:** O arquivo `contatos.txt` é gerado automaticamente pela aplicação ao ser encerrada, no diretório de execução.

### Arquitetura das Classes (MVC Completo)

```text
Principal  (composition root: cria dependências, injeta, chama view.iniciar())
   │
   ├── AgendaView (View)        → loop principal (iniciar), menus, executar*(), I/O terminal
   │     └── AgendaController   → regras de negócio: CRUD, coordena DAO
   │           └── ContatoDAO   → persistência arquivo (instância, caminho configurável)
   │
   └── Contato (Modelo)         → entidade usada por todas as camadas
```

### Divisão de Responsabilidades

| Classe | Pacote | Responsabilidade |
| :--- | :--- | :--- |
| `Contato` | `modelo` | Entidade com atributos privados, construtor parametrizado, getters e setters |
| `AgendaController` | `controle` | Regras de negócio: adicionar, listar, pesquisar, atualizar, excluir, salvar |
| `AgendaView` | `visao` | **Loop principal**, menus, leitura/escrita terminal, `executar*()` delegam ao Controller |
| `ContatoDAO` | `dao` | Persistência em arquivo (`contatos.txt`), instância com caminho configurável |
| `Principal` | `principal` | **Composition root minimal**: cria dependências, injeta no Controller/View, chama `view.iniciar()` |

---

## 🚀 Como Executar (v5.1.0)

1. **Compile as classes (da raiz do projeto):**
   ```bash
   javac -d bin src/br/edu/modelo/Contato.java src/br/edu/dao/ContatoDAO.java src/br/edu/controle/AgendaController.java src/br/edu/visao/AgendaView.java src/br/edu/principal/Principal.java
   ```

2. **Execute a aplicação:**
   ```bash
   java -cp bin br.edu.principal.Principal
   ```