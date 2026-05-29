# AppAgenda-Java

## Visão Geral
O **AppAgenda-Java** é uma aplicação desktop desenvolvida em Java com foco no gerenciamento de contatos e reuniões. O projeto foi estruturado seguindo os princípios de arquitetura limpa, implementando uma divisão modular que garante a separação de responsabilidades, alta manutenibilidade e escalabilidade do código.

---

## Funcionalidades Principais
* **Gerenciamento de Contatos:** Controle do ciclo de vida dos contatos, incluindo informações pessoais e vinculação de endereços.
* **Organização de Reuniões:** Agendamento e gerenciamento de reuniões com persistência de informações dedicadas.
* **Padrão Data Access Object (DAO):** Camada de acesso a dados abstrata, isolando as operações de persistência da lógica de negócio.
* **Arquitetura MVC:** Separação rígida entre a lógica de negócio, os modelos de dados e a interface de interação com o usuário.

---

## Tecnologias e Conceitos Utilizados
* **Linguagem:** Java
* **Paradigma:** Programação Orientada a Objetos (POO)
* **Arquitetura:** Model-View-Controller (MVC) e Padrão DAO
* **Ambiente de Desenvolvimento:** IntelliJ IDEA / VS Code

---

## Estrutura do Projeto
Distribuição dos pacotes seguindo as camadas definidas pela arquitetura do sistema:

```text
AppAgenda-Java/
└── src/
    ├── controller/      # Lógica de negócio e orquestração das entidades
    │   ├── Contato.java
    │   ├── Endereco.java
    │   ├── InfoReuniao.java
    │   ├── Lista.java
    │   └── Reuniao.java
    ├── model/           # Camada de acesso a dados (Padrão DAO)
    │   ├── ContatoDAO.java
    │   ├── DAO.java
    │   ├── EnderecoDAO.java
    │   ├── InfoReuniaoDAO.java
    │   ├── ListaDAO.java
    │   └── ReuniaoDAO.java
    └── view/            # Interação com o usuário e ponto de entrada do sistema
        ├── Lista.java
        └── Main.java

```

> **Nota:** Os arquivos compilados (.class) são gerados automaticamente pela IDE no diretório de saída durante o build e foram incluídos no arquivo .gitignore para manter o repositório limpo.

---

## Divisão Arquitetural

### Controller

Contém as regras de negócio centrais e atua como intermediário entre os modelos de dados e a camada de apresentação.

### Model (DAO)

Responsável pela estruturação dos dados e pela lógica de persistência. O uso do padrão DAO (Data Access Object) isola a lógica de negócio de comandos diretos de manipulação de dados, garantindo um código desacoplado.

### View

Camada responsável por renderizar as informações e gerenciar a execução da interface com o usuário, tendo como ponto de partida a classe principal Main.java.

---

## Como Executar o Projeto

1. **Clonar o repositório:**
```bash
git clone [https://github.com/maduaperes/AppAgenda-Java.git](https://github.com/maduaperes/AppAgenda-Java.git)

```


2. **Abrir o projeto:**
Importe a pasta raiz em sua IDE de preferência (IntelliJ IDEA ou VS Code com o pacote Java Extension Pack instalado).
3. **Executar a aplicação:**
Navegue até o arquivo `src/view/Main.java` e execute o método `main`.

---

## Objetivo Acadêmico

Este projeto foi desenvolvido com propósitos educacionais e de portfólio para consolidar conceitos de:

* Padrões de arquitetura de software.
* Princípio de Responsabilidade Única (SRP).
* Desacoplamento de acesso a dados em aplicações Java.
