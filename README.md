# Sistema de Gestão de Projetos e Equipes

Projeto acadêmico desenvolvido para a atividade A3 da disciplina 
**Programação de Soluções Computacionais** da **Universidade São Judas**.

## Sobre o projeto

Este sistema foi desenvolvido em **Java** com foco nos conceitos de **Programação Orientada a Objetos (POO)**, organização em camadas inspirada no padrão **MVC** e aplicação de boas práticas de desenvolvimento.

A proposta do projeto é auxiliar no controle de **projetos**, **equipes**, **usuários** e **tarefas**, permitindo uma gestão mais organizada das atividades e do andamento dos projetos.

## Funcionalidades

- Cadastro de usuários
- Definição de perfis de acesso:
  - Administrador
  - Gerente
  - Colaborador
- Cadastro de equipes
- Vinculação de membros às equipes
- Cadastro de projetos
- Definição de gerente responsável
- Alocação de equipes em projetos
- Cadastro de tarefas por projeto
- Atualização de status de projetos e tarefas
- Relatório simples de acompanhamento
- Validação de dados e tratamento de exceções

## Tecnologias utilizadas

- Java
- Programação Orientada a Objetos
- Estrutura inspirada no padrão MVC
- SQL (modelo de banco incluído no projeto)

## Estrutura do projeto

```text
src/
 └── br/com/a3/gestaoprojetos/
     ├── controller/
     ├── exception/
     ├── model/
     ├── repository/
     ├── util/
     ├── view/
     └── Main.java
```

## Estrutura principal

- `model`: classes de domínio do sistema
- `controller`: regras e controle das operações
- `repository`: armazenamento em memória
- `view`: interação via menu no console
- `exception`: exceções personalizadas
- `util`: validações auxiliares

## Como executar

No terminal, dentro da pasta do projeto:

### Executar
```bash
java -cp out br.com.a3.gestaoprojetos.Main
```

### Como testar o sistema

*Teste rápido com dados automáticos:*
| Opção | O que faz                                          |
|-------|----------------------------------------------------|
| 11    | Carrega usuários, equipe, projeto e tarefas de exemplo |
| 2     | Lista todos os usuários cadastrados                |
| 10    | Gera relatório do projeto (informe o ID: 1)        |
| 9     | Atualiza status de uma tarefa                      |
| 8     | Atualiza status do projeto                         |

*Teste manual completo:*
- 1  → Cadastrar usuário
- 3  → Cadastrar equipe
- 4  → Adicionar membro na equipe
- 5  → Cadastrar projeto
- 6  → Alocar equipe no projeto
- 7  → Cadastrar tarefa
- 10 → Gerar relatório

*Formatos importantes:*

- Datas: AAAA-MM-DD (exemplo: 2026-06-05)
- Perfil: 1 Administrador | 2 Gerente | 3 Colaborador
- Status do projeto: 1 Planejado | 2 Em andamento | 3 Concluído | 4 Cancelado
- Status da tarefa: 1 Pendente | 2 Em andamento | 3 Concluída | 4 Bloqueada

## Banco de dados

A pasta `database` contém os arquivos:

- `schema.sql`
- `sample_data.sql`

Esses arquivos representam a base inicial para futura integração com banco de dados relacional.

## Observações

- Este projeto foi desenvolvido como um **MVP acadêmico**.
- A execução atual ocorre em **modo console**.
- A estrutura foi organizada para facilitar futuras melhorias, como integração real com banco de dados e interface gráfica.

## Autores

Desenvolvido pela equipe como atividade A3 da disciplina  
*Programação de Soluções Computacionais*  
*Universidade São Judas*
- Bruno de Abreu Balan
- Sabrina Lima de Souza  
- Mirella Prando Medeiro
