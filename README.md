# Mainquest

## Visão Geral

**Mainquest** é um jogo de RPG baseado em turnos, desenvolvido principalmente em PHP e JavaScript. O objetivo do jogo é uma gameplay simples, permitindo que os jogadores criem e gerenciem seus personagens.

## Funcionalidades

- **Criação e Login de Personagens:** Os usuários podem registrar e fazer login em seus personagens.
- **Escolha de Classe:** Os jogadores podem escolher livremente a classe de seu personagem.
- **Implementação de Status de Personagens:** Cada personagem possui atributos e estatísticas que afetam a jogabilidade.

## Estrutura

### Páginas Principais

1. **login.php**
   - Esta é a página principal de login do sistema.
   - Os usuários podem enviar suas credenciais através de um formulário para acessar a pagina de jogo (mainquest.php).
   - Também há um botão que redireciona os usuários para a página de registro (register.php).

2. **register.php**
   - Esta página contém um formulário com três campos:
     - **Nome do Personagem:** O nome do heroi do jogador.
     - **Senha:** Uma senha específica para o personagem.
     - **Classe do Personagem:** A classe escolhida para o personagem (ex: Mago, Guerreiro, Arqueiro).
   - Após o envio bem-sucedido do formulário, um "herói" será criado no banco de dados MongoDB (chamado "accounts").
   - As informações armazenadas no banco de dados são parcialmente determinadas pela classe selecionada.
   - Após o registro, os usuários são redirecionados de volta para **login.php** para logar com seu novo personagem.

3. **mainquest.php**
   - Esta página contém a funcionalidade central do jogo.
   - Após um login bem-sucedido, o jogador é redirecionado para esta página.
   - O jogo inicia uma série de encontros de combate com base nas informações do personagem armazenadas na sessão.

## Estrutura do Banco de Dados

- **Banco de Dados:** `accounts`
- **Coleção:** `login`
  - Armazena informações do usuário, incluindo:
    - Nome de usuário
    - Senha (hash)
    - Classe (Mago, Guerreiro, Arqueiro, etc.)
    - Nível
    - Vida (PV)
    - Vida maxima (PVmax)
    - Armadura
    - Tamanho do inventario

## Como Jogar

1. **Registro:**
   - Navegue até a página **Registro**.
   - Preencha o formulário com o nome do personagem, senha e classe.
   - Envie o formulário para criar seu personagem.

2. **Login:**
   - Acesse a página **Login**.
   - Insira o nome e a senha do seu personagem.
   - Clique no botão de login para entrar no jogo.
