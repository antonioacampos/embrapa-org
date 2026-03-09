**Ata de Reunião — Projeto**

**Data:** 05/03/2026  
**Responsáveis:** Estela, Gustavo e Antonio  

***

## 1. Resumo

O time avançou na estruturação da engenharia e no mapeamento dos requisitos do sistema de cálculos integrados. As melhorias focaram em evitar inconsistências em cenários com vários talhões e garantir a rastreabilidade das regras de negócio de **LER (Land Equivalent Ratio)** e **margem bruta**.  

Também foi revisado o modelo de governança de dados, separando a entidade **Propriedade** das **CATIs**.

***

## 2. Atividades Realizadas e Entregas

### 2.1 Engenharia de Testes e Mapeamento

- **Mapeamento de Regras de Cálculo**  
  Consolidação das lógicas de conversão de dados de entrada, estoques de madeira e margem bruta, garantindo o fluxo correto entre a coleta de dados e o banco central.

- **Tratamento de Exceções e Dados Nulos**  
  Implementação de regras para lidar com dados vazios e evitar erros de divisão por zero, aplicando a **“média condicional (Média C)”** em talhões inativos.

- **Testes em Funcionalidades Offline (PWA)**  
  Definição do escopo offline, que será focado na coleta inicial de dados e exibição de gráficos de **Percepção** e **Bem-estar**, deixando os cálculos mais pesados apenas para o modo online.

***

### 2.2 Governança, Acessos e Dados

- **Modelagem de Dados**  
  Reorganização do banco para que **Propriedade** seja uma entidade independente. Agora, produtores e técnicos podem estar vinculados à mesma propriedade sem depender de vínculo direto com a **CATI**.

- **Padronização Nacional**  
  Remoção da obrigatoriedade de vínculo com a **CATI**, possibilitando a adoção do sistema por outras instituições no país.

- **Controle de Acesso**  
  Definição de perfis de acesso: os usuários veem apenas os **relatórios processados**, enquanto os dados brutos ficam restritos aos administradores.

***

## 3. Bloqueios e Riscos

- **Modelo de Entrega do Software (PWA)**  
  Ainda há indefinição sobre o modelo de entrega via navegador, o que pode impactar a estratégia de armazenamento offline.  
  **Responsável:** Equipe de Desenvolvimento.

- **Adaptação a Novos Perfis de Cultivo**  
  É necessário ajustar as regras do sistema para novos tipos de cultivo, como **agroflorestas com cacau e banana**, sem afetar as regras atuais de lavoura e floresta.  
  **Responsável:** Estela e Marcela.

***

## 4. Próximos Passos

- Finalizar e aprovar a **planilha mestre de regras de negócio**, com as especificações de obrigatoriedade, para validação pela equipe de testes.  
- Criar e validar o **protótipo dos relatórios gráficos de percepção offline**, que será a primeira entrega voltada ao uso em campo.  
- Formalizar os **requisitos de infraestrutura e hospedagem do sistema**, seguindo as definições contratuais (web e mobile), para liberar as próximas etapas da arquitetura.
- Adicionar legendas na aba de **Percepção** para explicar **quais componentes a propriedade deve ter** para a pergunta ser exibida no sistema. 

***
