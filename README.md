# Sistema de Gestão de Projetos e Equipes
Projeto acadêmico desenvolvido para a atividade A3 da disciplina 
*Programação de Soluções Computacionais* da *Universidade São Judas*.
---
## Sobre o projeto
Este sistema foi desenvolvido em *Java* com foco nos conceitos de 
*Programação Orientada a Objetos (POO)*, organização em camadas 
inspirada no padrão *MVC* e aplicação de boas práticas de 
desenvolvimento de software.
A proposta do projeto é auxiliar no controle de *projetos*, 
*equipes, **usuários* e *tarefas*, permitindo uma gestão mais 
organizada das atividades e do andamento dos projetos dentro de 
uma organização.
---
## Funcionalidades
- Cadastro de usuários com definição de perfis de acesso:
  - Administrador
  - Gerente
  - Colaborador
- Cadastro de equipes
- Vinculação de membros às equipes
- Cadastro de projetos com definição de gerente responsável
- Alocação de equipes em projetos
- Cadastro de tarefas por projeto com responsável definido
- Atualização de status de projetos:
  - Planejado | Em Andamento | Concluído | Cancelado
- Atualização de status de tarefas:
  - Pendente | Em Andamento | Concluída | Bloqueada
- Geração de relatório de acompanhamento do projeto
- Validação de dados e tratamento de exceções customizadas
- Carregamento automático de dados de exemplo para demonstração
---
## Tecnologias utilizadas
- Java (JDK 17+)
- Programação Orientada a Objetos (POO)
- Arquitetura inspirada no padrão MVC
- Java Collections — persistência em memória via ArrayList
- Java Stream API — filtros, buscas e processamento de listas
- Java Time API — manipulação de datas com LocalDate
- SQL — modelo de banco de dados incluído no projeto
---
## Estrutura do projeto
src/
 └── br/com/a3/gestaoprojetos/
     ├── controller/
     ├── exception/
     ├── model/
     ├── repository/
     ├── util/
     ├── view/
     └── Main.java
database/
     ├── schema.sql
     └── sample_data.sql
---
## Descrição de cada camada
| Pacote       | Responsabilidade                                                        |
|--------------|-------------------------------------------------------------------------|
| model        | Classes de domínio: User, Team, Project, TaskItem e enums              |
| controller   | Regras de negócio e controle das operações de cada módulo              |
| repository   | Armazenamento e recuperação dos dados em memória                       |
| view         | Interação com o usuário via menu no console                            |
| exception    | Exceções customizadas: BusinessException, NotFoundException, Validation |
| util         | Utilitário de validações: campos obrigatórios, CPF e e-mail            |
---
## Como executar
### Compilar
javac -d out $(find src -name "*.java")
### Executar
java -cp out br.com.a3.gestaoprojetos.Main
---
## Como testar o sistema
*Teste rápido com dados automáticos:*
| Opção | O que faz                                          |
|-------|----------------------------------------------------|
| 11    | Carrega usuários, equipe, projeto e tarefas de exemplo |
| 2     | Lista todos os usuários cadastrados                |
| 10    | Gera relatório do projeto (informe o ID: 1)        |
| 9     | Atualiza status de uma tarefa                      |
| 8     | Atualiza status do projeto                         |
*Teste manual completo:*
1  → Cadastrar usuário
3  → Cadastrar equipe
4  → Adicionar membro na equipe
5  → Cadastrar projeto
6  → Alocar equipe no projeto
7  → Cadastrar tarefa
10 → Gerar relatório
*Formatos importantes:*
- Datas: AAAA-MM-DD (exemplo: 2026-06-05)
- Perfil: 1 Administrador | 2 Gerente | 3 Colaborador
- Status do projeto: 1 Planejado | 2 Em andamento | 3 Concluído | 4 Cancelado
- Status da tarefa: 1 Pendente | 2 Em andamento | 3 Concluída | 4 Bloqueada
---
## Banco de dados
A pasta database contém:
- schema.sql — estrutura das tabelas para integração futura
- sample_data.sql — dados de exemplo para popular o banco
---
## Observações
- Este projeto foi desenvolvido como um MVP acadêmico
- A execução atual ocorre em modo console
- A estrutura foi organizada para facilitar melhorias futuras,
  como integração com banco de dados e interface gráfica
- Os dados cadastrados ficam na memória e são perdidos ao encerrar
---
## Autores
Desenvolvido pela equipe como atividade A3 da disciplina  
*Programação de Soluções Computacionais*  
*Universidade São Judas*
- Bruno de Abreu Balan
- Sabrina Lima de Souza  
- Mirella Prando Medeiro