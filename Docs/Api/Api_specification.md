# Especificação da API - Petbem

Esta API segue o padrão RESTful, utilizando JSON para o intercâmbio de dados e JWT (JSON Web Token) para autenticação.

## 1. Endpoints de Animais
| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| GET | `/animais` | Lista todos os animais do abrigo. |
| POST | `/animais` | Cadastra um novo animal resgatado. |
| GET | `/animais/{id}` | Retorna os detalhes e prontuário de um animal específico. |

## 2. Endpoints de Saúde (Prontuário)
| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| POST | `/animais/{id}/logs` | Adiciona uma atualização (log) no histórico de melhora. |
| GET | `/animais/{id}/tratamentos` | Lista os medicamentos e dosagens atuais do animal. |

## 3. Exemplo de Requisição (Cadastro de Animal)
**POST** `/animais`
```json
{
  "nome": "Belinha",
  "especie": "Cachorro",
  "data_ingresso": "2026-03-25",
  "status_saude": "Em tratamento"
}
```

## 4. Endpoints de Exportação e Relatórios
| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| GET | `/animais/{id}/exportar` | Gera e baixa o PDF com a tabela completa de histórico e comportamento. |

### Exemplo de Resposta (Exportação)
**Status:** 200 OK
**Content-Type:** application/pdf
*(O sistema retorna o arquivo binário pronto para download)*.
