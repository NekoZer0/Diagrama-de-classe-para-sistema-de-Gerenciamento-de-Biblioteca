
# Sistema de Gerenciamento de Biblioteca

Este repositório contém um modelo UML representando um **Sistema de Gerenciamento de Biblioteca**, projetado para administrar o cadastro, empréstimo e devolução de livros, bem como a gestão de usuários e membros associados.

## 📋 Descrição Geral

O sistema permite:
- **Gestão de Bibliotecas**: Cadastro, consulta, atualização e exclusão de bibliotecas.
- **Gestão de Usuários e Membros**: Controle de acesso e associação dos membros à biblioteca.
- **Gestão de Livros**: Cadastro, exclusão, atualização e controle da disponibilidade dos livros.
- **Transações**: Registro de empréstimos e devoluções de livros.

## 🗂️ Estrutura do Modelo

### **Entidades Principais**
1. **Biblioteca**
   - Armazena informações sobre bibliotecas, como nome, contato e e-mail.
   - Métodos:
     - `criar()`: Cadastra uma nova biblioteca.
     - `consultar(id)`: Retorna informações de uma biblioteca específica.
     - `eliminarBiblioteca(id)`: Remove uma biblioteca do sistema.
     - `actualizar(id)`: Atualiza os dados de uma biblioteca.

2. **Usuário**
   - Representa os administradores ou operadores do sistema.
   - Métodos:
     - `entrar(email, senha)`: Autentica o usuário.
     - `sair()`: Finaliza a sessão do usuário.
     - `criarMembro(usuario)`: Registra um novo membro.
     - `eliminarMembro(id)`: Remove um membro do sistema.
     - `consultarMembro(id)`: Exibe informações de um membro.

3. **Membro**
   - Representa as pessoas associadas à biblioteca.
   - Métodos:
     - `emprestarLivro(livro, membro)`: Realiza o empréstimo de um livro.
     - `devolverLivro(livro)`: Registra a devolução de um livro.
     - `entrar(email, senha)`: Autentica o membro no sistema.
     - `consultarEmprestados()`: Lista os livros emprestados por este membro.

4. **Livro**
   - Contém detalhes dos livros disponíveis na biblioteca.
   - Métodos:
     - `cadastrar(livro)`: Registra um novo livro.
     - `apagar(id)`: Remove um livro do sistema.
     - `actualizar(id)`: Atualiza informações de um livro.

5. **Transação**
   - Registra as movimentações de empréstimos e devoluções.
   - Atributos:
     - `data_emissao`: Data em que o livro foi emprestado.
     - `data_devolucao`: Data prevista para devolução.
     - `status`: Indica se o livro foi devolvido ou está emprestado.

## 🔗 Relacionamentos

- Uma **Biblioteca** pode conter múltiplos **Livros**, sendo que cada livro pertence a uma única biblioteca.
- Um **Usuário** pode gerenciar vários **Membros**.
- Um **Membro** pode realizar empréstimos de livros, sendo que cada empréstimo é registrado como uma **Transação**.

## 🛠️ Ferramenta Utilizada

O modelo foi desenvolvido utilizando uma ferramenta de modelagem UML. Este diagrama representa um sistema orientado a objetos, ideal para implementação em linguagens de programação como Java ou Python.

## 📂 Estrutura do Repositório

- `README.md`: Documentação do sistema.
- Arquivo UML e/ou diagrama de classes incluído neste repositório.

## 📄 Licença

Este projeto está licenciado sob a [MIT License](LICENSE). Consulte o arquivo de licença para mais detalhes.
