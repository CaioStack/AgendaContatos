# 📇 Agenda de Contatos - *Projeto Didático em Java*

![Java Version](https://img.shields.io/badge/Java-14%2B-orange?style=flat-square&logo=openjdk)
![Course](https://img.shields.io/badge/Disciplina-POO-blue?style=flat-square)
![Institution](https://img.shields.io/badge/IFCE-Campus%20Maranguape-green?style=flat-square)
![Current Version](https://img.shields.io/badge/Vers%C3%A3o-v0.3.0-informational?style=flat-square)

## 📌 Sobre o Repositório

Este repositório faz parte do projeto **Agenda de Contatos**, desenvolvido como material didático e prático para a disciplina de **Programação Orientada a Objetos (POO)** do **4º semestre** do *Instituto Federal de Educação, Ciência e Tecnologia do Ceará (IFCE) — Campus Maranguape*.

O objetivo central é construir uma aplicação Java de forma **incremental e evolutiva**. Através dessa abordagem, o estudante acompanha na prática o surgimento de novos problemas de software e compreende a real necessidade de aplicar novas estruturas de dados, boas práticas e paradigmas da programação.

---

## 🎯 Versão Atual: `v0.3.0`

### Finalidade Didática
A versão **`v0.3.0`** consolida o ciclo de operações fundamentais sobre coleções dinâmicas ao fechar o modelo **CRUD** (*Create, Read, Update, Delete*). 

Ela introduz a funcionalidade de **Alterar Contato**, utilizando o método `.set()` para atualizar os dados de um registro pré-existente sem alterar sua posição na lista. Embora seja um avanço pontual, ele é conceitualmente estratégico para apresentar formalmente a manipulação completa de coleções em memória.

---

## 🛠️ Funcionalidades Implementadas

- [x] **Adicionar Contato (`CREATE`):** Insere um novo contato no final das listas.
- [x] **Listar Todos os Contatos (`READ`):** Exibe todos os registros salvos na memória.
- [x] **Procurar Contato (`READ`):** Realiza a busca de um contato por nome.
- [x] **Alterar Contato (`UPDATE`) ⭐ *Novidade*:** Localiza um contato por nome e substitui suas informações via método `.set()`.
- [x] **Excluir Contato (`DELETE`):** Remove o contato desejado mantendo a consistência dos índices.
- [x] **Sair:** Finaliza o programa.

---

## 🧠 Conceitos de Programação Trabalhados

Nesta versão, encerra-se o bloco fundamental de estudos sobre a estrutura `ArrayList`:

* **Substituição por Índice:** Diferença conceitual e prática entre `.add()` (inserção de novos elementos) e `.set()` (atualização de elementos existentes).
* **Mapeamento Posicional:** Busca de elementos mantendo a referência de seu índice para alterações cirúrgicas nas listas paralelas (`nomes`, `celulares`, `emails`).
* **Tratamento de Exceções Lógicas:** Validação e feedback visual para cenários de "Contato não encontrado".
* **Consolidação do Modelo CRUD:** Mapeamento direto das operações de software com métodos do *Java Collections Framework*.

---

## 🔄 Visão do CRUD com `ArrayList`

Com a introdução do método `.set()`, a sequência de aprendizado da estrutura `ArrayList` é finalizada:

```plain
V.0.2.0 (Fundamentos da Coleção)
├── add()    ➡️  CREATE (Adicionar)
├── get()    ➡️  READ (Consultar)
├── remove() ➡️  DELETE (Excluir)
└── size()   ➡️  Capacidade Dinâmica

V.0.3.0 (Ciclo Completo)
└── set()    ➡️  UPDATE (Alterar) ⭐