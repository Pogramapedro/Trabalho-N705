**NOTA:**
// Estou fazendo o trabalho sozinho pois sempre tenho dificuldade em achar um grupo

# Petbem: Sistema Multiplataforma de Gestão e Prontuário Animal

## 1. Visão Geral do Projeto
Este projeto consiste no planejamento de uma solução multiplataforma voltada para a gestão de saúde e histórico médico de animais em abrigos e ONGs de proteção. O foco principal é garantir a continuidade dos tratamentos e a transparência das informações de cada animal resgatado.

### Problema e Justificativa (ODS 11)
Muitos abrigos em Fortaleza enfrentam dificuldades na organização de prontuários, utilizando fichas de papel que se perdem ou se deterioram. O **Petbem** atende ao **ODS 11 (Cidades e Comunidades Sustentáveis)** ao promover o controle sanitário eficiente e o bem-estar animal, contribuindo para uma saúde pública urbana mais resiliente e organizada

### Objetivos do Sistema
* **Centralizar** o histórico médico (doenças, vacinas e medicações) de cada animal.
* **Facilitar** o acompanhamento da evolução clínica por meio de uma linha do tempo.
* **Otimizar** a rotina de voluntários com alertas de medicação e status de saúde visual.



## 2. Prática Extensionista (Evidências)


**Organização Selecionada:** Lar da tia Myrlla(@LARDATIAMYRLLA)**Contexto:** Realizamos o levantamento de dados através do perfil oficial da instituição, analisando a rotina de resgates, as principais patologias relatadas e as dinâmicas de adoção.

### Evidências Coletadas
> Abaixo, detalhamos o contato e a análise da demanda real da organização parceira.

* **Análise de Fluxo:** Trata-se de um abrigo que tem alto fluxo de animais sendo resgatados e faz, frequentemente eventos de adoção. o app seria capaz de ajudar tanto o abrigo no gerenciamento dos animais, quanto aos atuais donos, apos terem acesso a uma planilha exportada do app.
* **Registros Visuais:** As fotos dos prontuários atuais e dos animais em tratamento (conforme prints do perfil) estão armazenadas na pasta `docs/extension/`.



## 3. Arquitetura e Tecnologias Propostas
O sistema foi projetado sob uma arquitetura de microsserviços para garantir escalabilidade e suporte multiplataforma (Web e Mobile)

* **Frontend:** React (Web) e React Native (Mobile).
* **Backend:** Node.js com arquitetura RESTful.
* **Banco de Dados:** PostgreSQL (Relacional) para garantir a integridade dos históricos médicos.
* **Infraestrutura:** Docker para padronização do ambiente de desenvolvimento.

---

## 4. Cronograma de Desenvolvimento (Etapa 2 - N708)
Planejamento para a implementação prática do sistema na próxima etapa do curso:

| Semana | Atividade Principal |
| :--- | :--- |
| **01-02** | Configuração do ambiente e Modelagem do Banco de Dados |
| **03-05** | Desenvolvimento do Backend e integração com APIs de saúde |
| **06-08** | Desenvolvimento da interface Mobile e Web |
| **09-10** | Testes de usabilidade e homologação com a ONG parceira |

---

## 5. Equipe e Papéis
Lista de integrantes devidamente cadastrados no AVA(Nesse caso, eu)

* **PEDRO THIAGO BORGES GOMES - 2326187:** Líder de Projeto e Desenvolvedor.

* **Link do Repositório:** https://github.com/Pogramapedro/Trabalho-N705
