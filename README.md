# Projeto: Sistema de Gerenciamento de Biblioteca

## Descrição
Você vai desenvolver um sistema de gerenciamento de uma pequena biblioteca que opera apenas em um terminal. O sistema permitirá que o usuário gerencie livros, clientes, e empréstimos de livros.

## Requisitos do Sistema
1. *Encapsulamento*: Todas as classes devem ter seus atributos privados e expor métodos públicos para acesso e modificação (getters e setters).
2. *Herança*: Crie uma hierarquia de classes que permita a reutilização de código comum.
3. *Classe Abstrata*: Defina uma classe abstrata que sirva de base para outros tipos de objetos.
4. *Sobrecarga de Métodos*: Use sobrecarga para criar métodos que aceitem diferentes tipos de parâmetros ou uma quantidade variável deles.
5. *Métodos Abstratos*: Inclua métodos abstratos que devem ser implementados por classes concretas derivadas.
6. *Interfaces*: Defina uma ou mais interfaces que descrevam comportamentos comuns que podem ser implementados por várias classes.

## Classes Sugeridas

### ItemBiblioteca (Classe Abstrata)
- *Atributos*:
  - String titulo
  - String autor
  - int anoPublicacao
- *Métodos*:
  - abstract void exibirDetalhes(): Método abstrato para exibir detalhes do item.
- Esta classe será a base para diferentes tipos de itens na biblioteca (livros, revistas, etc.).

### Livro (Herda de ItemBiblioteca)
- *Atributos*:
  - String ISBN
  - String genero
- *Métodos*:
  - void exibirDetalhes(): Implementa o método abstrato para exibir detalhes específicos do livro.

### Revista (Herda de ItemBiblioteca)
- *Atributos*:
  - int numeroEdicao
- *Métodos*:
  - void exibirDetalhes(): Implementa o método abstrato para exibir detalhes específicos da revista.

### Cliente
- *Atributos*:
  - String nome
  - String cpf
  - List<ItemBiblioteca> itensEmprestados
- *Métodos*:
  - void emprestarItem(ItemBiblioteca item): Adiciona um item à lista de itens emprestados.
  - void devolverItem(ItemBiblioteca item): Remove um item da lista de itens emprestados.

### Emprestimo
- *Atributos*:
  - Cliente cliente
  - ItemBiblioteca item
  - String dataEmprestimo
  - String dataDevolucao
- *Métodos*:
  - void registrarEmprestimo(): Registra o empréstimo.
  - void registrarDevolucao(): Registra a devolução.

### SistemaBiblioteca (Classe Principal)
- *Métodos*:
  - void menuPrincipal(): Exibe o menu principal e permite ao usuário escolher entre diferentes operações como adicionar livros, emprestar itens, etc.

### Exibivel (Interface)
- *Métodos*:
  - void exibir(): Método que será implementado por classes que têm a responsabilidade de exibir algo na tela.

### Catalogo
- *Atributos*:
  - List<ItemBiblioteca> itensDisponiveis
- *Métodos*:
  - void adicionarItem(ItemBiblioteca item): Adiciona um novo item ao catálogo.
  - void listarItens(): Lista todos os itens disponíveis no catálogo.

## Funcionalidades
- O sistema deve permitir ao usuário:
  - Adicionar novos livros e revistas ao catálogo.
  - Listar todos os itens disponíveis.
  - Registrar empréstimos e devoluções.
  - Exibir os detalhes dos itens no catálogo.

## Desafio
Implemente esse sistema utilizando as melhores práticas de programação orientada a objetos, garantindo que todos os conceitos (encapsulamento, herança, etc.) sejam aplicados de forma adequada.
