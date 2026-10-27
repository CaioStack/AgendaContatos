# 📒 Agenda de Contatos

> **Projeto prático desenvolvido no IFCE – Campus Maranguape**  
> **Disciplina:** Programação Orientada a Objetos (POO)  
> **Aluno:** Caio | **Professor:** Prof. Roger

![Java](https://img.shields.io/badge/Java-17%2B-orange?style=flat-square&logo=openjdk)
![Instituição](https://img.shields.io/badge/IFCE-Campus%20Maranguape-green?style=flat-square)
![Status](https://img.shields.io/badge/Versão%20Atual-v3.3.0%20(Encapsulamento)-blue?style=flat-square)

---

## 📌 Sobre o Projeto

Sistema de gerenciamento de contatos em Java construído de forma **incremental**: cada versão parte da anterior e acrescenta um conceito novo, evoluindo de variáveis simples até encapsulamento, passando por coleções dinâmicas, modularização em classes dedicadas e persistência em arquivos.

Cada pasta `vX.Y.Z` deste repositório é uma versão completa e executável, acompanhada de seu próprio `README.md` individual, permitindo acompanhar visualmente a evolução do código a cada etapa do aprendizado.

---

## ✨ Funcionalidades (v3.3.0)

| Funcionalidade | O que faz | Onde fica |
| :--- | :--- | :--- |
| ➕ **Adicionar** | Cadastra um contato com nome, celular e e-mail | `Agenda.adicionar()` |
| 📋 **Listar** | Mostra todos os contatos cadastrados | `Agenda.listar()` |
| 🔍 **Pesquisar** | Busca contatos por atributos | `Agenda.pesquisar()` |
| ✏️ **Atualizar** | Altera os dados de um contato existente | `Agenda.atualizar()` |
| 🗑️ **Excluir** | Remove um contato da coleção | `Agenda.excluir()` |
| 💾 **Persistência** | Carrega e salva automaticamente em `contatos.txt` | `Persistencia.carregarContatos()` e `Persistencia.salvarContatos()` |

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
| **v3.3.0** ✅ | **Encapsulamento (Atual)** | `private`, construtor parametrizado, `this`, getters e setters |

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
├── v3.3.0/               # Versão atual: encapsulamento (private, construtor, get/set)
└── README.md
```

---

## 🏗️ Estrutura da Versão Atual (v3.3.0)

### Organização dos Arquivos

```text
v3.3.0/
├── README.md
└── src/
    └── br/
        └── edu/
            └── principal/
                ├── Agenda.java
                ├── Contato.java
                ├── Persistencia.java
                ├── Principal.java
                └── Uteis.java
```

> **Nota:** O arquivo `contatos.txt` é gerado automaticamente pela aplicação ao ser encerrada, no diretório de execução.

### Arquitetura das Classes

Tudo fica no pacote `br.edu.principal`, operando sobre uma única coleção `List<Contato>`:

```text
Principal  (controla o loop do menu e mantém a List<Contato>)
   │
   ├── Uteis          → menus e leitura de opções
   ├── Agenda         → adicionar() · listar() · pesquisar() · atualizar() · excluir()
   └── Persistencia   → carregarContatos() · salvarContatos()

Contato  → entidade usada por todas as classes acima
```

### Divisão de Responsabilidades

| Classe | Responsabilidade |
| :--- | :--- |
| `Contato` | Entidade com atributos privados, construtor parametrizado, getters e setters |
| `Agenda` | Operações de CRUD sobre a `List<Contato>` |
| `Persistencia` | Leitura e escrita do arquivo `contatos.txt` via `java.io` |
| `Uteis` | Exibição de menus e métodos auxiliares de interface gráfica/terminal |
| `Principal` | Ponto de entrada da aplicação (`main`) e controle do laço do menu |

---

## 🚀 Como Executar (v3.3.0)

1. **Acesse a pasta da versão atual:**
   ```bash
   cd v3.3.0
   ```

2. **Compile as classes do pacote:**
   ```bash
   javac -d bin src/br/edu/principal/*.java
   ```

3. **Execute a aplicação:**
   ```bash
   java -cp bin br.edu.principal.Principal
   ```