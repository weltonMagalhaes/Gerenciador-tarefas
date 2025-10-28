# 🧠 Gerenciador de Tarefas

Sistema de controle de tarefas com acompanhamento de tempo, voltado para uso pessoal e profissional.

---

## 🚀 Funcionalidades
- Cadastro de usuários
- Criação e acompanhamento de tarefas
- Controle de status (A Fazer, Em Progresso, Pausada, Concluída, Cancelada)
- Priorização por nível (Baixa, Média, Alta, Urgente)
- Contagem automática de tempo
- Histórico de alterações de status

---

## 🗄️ Banco de Dados
- O sistema utiliza **Oracle Database 21c XE**.  
- O script de criação das tabelas está em:

📂 `sql/sql.sql`

📋 Tabelas (resumo)

 | Tabela                | Finalidade                                                                      |
 | --------------------- | ------------------------------------------------------------------------------- |
 | **USUARIO**           | Armazena quem usa o sistema.                                                    |
 | **STATUS_TAREFA**     | Status (A Fazer, Em Progresso, Pausada, Concluída, Cancelada).                  |
 | **PRIORIDADE**        | Nível de urgência (Baixa, Média, Alta, Urgente).                                |
 | **TAREFA**            | Registro principal: título, descrição, prazo, status, prioridade, responsáveis. |
 | **APONTAMENTO_TEMPO** | Intervalos de trabalho (início/fim, minutos calculados).                        |
 | **CONTAGEM_ATIVA**    | Indica contagem de tempo aberta por (usuário, tarefa).                          |
 | **HISTORICO_STATUS**  | Auditoria das mudanças de status.                                               |


---

## 🛠️ Tecnologias
- Java 21
- Spring Boot
- Maven
- Oracle XE
- GitHub Actions (CI/CD)

---

## ⚙️ Build & Testes

Para compilar e testar:

```bash
mvn clean verify
