# Documento de Arquitetura de Software - Petbem

Este documento detalha a estrutura técnica e as decisões arquiteturais do sistema PetHealth, projetado para a gestão de prontuários em abrigos de animais.

## 1. Descrição da Arquitetura
O PetHealth utiliza uma arquitetura **Client-Server (Cliente-Servidor)** baseada em **Camadas**. Essa escolha permite a separação clara entre a interface do usuário (Frontend), a lógica de negócios (Backend) e a persistência de dados (Banco de Dados).

O sistema é **Multiplataforma**, garantindo que voluntários em campo acessem via dispositivos móveis enquanto a administração utiliza a versão Web para relatórios complexos.

## 2. Padrões Arquiteturais Utilizados
* **RESTful API:** Para a comunicação entre o cliente e o servidor via protocolo HTTP, utilizando JSON como formato de dados.
* **MVC (Model-View-Controller):** Para organizar a lógica interna do servidor, facilitando a manutenção e escalabilidade.
* **Singleton:** Aplicado na conexão com o banco de dados para otimizar o uso de recursos do servidor.

## 3. Componentes do Sistema
O ecossistema do projeto é dividido em quatro componentes principais:

* **Frontend Web (React):** Interface administrativa para gestão de cadastros e visualização de dashboards de saúde.
* **Frontend Mobile (React Native):** Aplicativo otimizado para o registro rápido de logs de comportamento e medicação à beira do leito/baia.
* **Backend API (Node.js/Express):** Processa as regras de negócio, autenticação e a geração de arquivos para exportação.
* **Serviço de Relatórios:** Módulo responsável por converter as tabelas de histórico e comportamento em arquivos **PDF/CSV** para compartilhamento externo.
* **Banco de Dados (PostgreSQL):** Base relacional que garante a integridade referencial entre animais, tutores e prontuários.

## 4. Diagrama de Arquitetura
Abaixo, a representação visual do fluxo de dados:

```mermaid
graph TD
    A[Usuário Mobile/Web] -->|HTTPS/JSON| B[API Gateway]
    B --> C[Camada de Autenticação]
    C --> D[Lógica de Negócio / Controllers]
    D --> E[Serviço de Exportação PDF]
    D --> F[Persistência de Dados]
    F --> G[(Banco de Dados PostgreSQL)]
