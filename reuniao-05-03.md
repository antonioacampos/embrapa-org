
**Data:** 05/03/2026
**Responsáveis:** Estela, Gustavo e Antonio

**1. RESUMO**
O time avançou na estruturação da engenharia  e no mapeamento de requisitos lógicos do sistema de cálculos integrados, mitigando riscos de inconsistência sistêmica em cenários com múltiplos talhões e buscando a rastreabilidade das regras de negócio de LER (Land Equivalent Ratio) e margens brutas. As definições de governança de dados foram reestruturadas, desvinculando propriedades de CATIs.

**2. ATIVIDADES REALIZADAS E ENTREGAS**
**2.1. Engenharia de Testes e Mapeamento**
*   **Mapeamento de Regras de Cálculo e Rastreabilidade:** Consolidação das lógicas de conversão de dados de entrada, estoques de madeira em pé e margem bruta, garantindo que os cálculos fluam corretamente da folha de dados para o banco de dados central.
*   **Tratamento de Exceções e Qualidade de Dados:** Implementação de lógicas de mitigação em cenários de dados nulos, validando a aplicação de "média condicional" (Média C) para evitar falhas sistêmicas (divisão por zero) em talhões inativos,.
*   **Quality Assurance em Funcionalidades Offline:** Análise técnica para delimitação do escopo offline (PWA), definindo que a aplicação focará na captura primária de dados e na exibição de gráficos de "Percepção" e "Bem-estar", isolando as lógicas pesadas para garantir a integridade do sistema em campo.

**2.2. Governança, Acessos e Dados**
*   **Modelagem e Governança de Entidades:** Reestruturação da arquitetura de banco de dados para tratar a "Propriedade" como entidade independente. Estabeleceu-se a permissão de múltiplos produtores e técnicos vinculados à mesma entidade, mitigando limitações do modelo de negócio anterior.
*   **Escalabilidade e Padronização Nacional:** Decisão executiva de remover a obrigatoriedade de vínculo dos técnicos com a CATI, promovendo a adequação do sistema para adoção nacional por outros institutos.
*   **Controle de Acessos:** Definição rigorosa de visibilidade, garantindo que usuários finais visualizem apenas os relatórios processados (deliverables), mantendo o banco de dados bruto sob restrição exclusiva aos administradores.

**3. BLOQUEIOS E RISCOS**

*   **Risco/Bloqueio:** Limitação e indefinição arquitetônica sobre o modelo de entrega do software (PWA via navegador), o que impacta diretamente a estratégia de armazenamento offline. | **Responsável:** Equipe de Desenvolvimento,,.
*   **Risco/Bloqueio:** Necessidade de adequação da lógica e rastreabilidade da multifuncionalidade para novos perfis de cultivo (ex.: "Agrofloresta" com cacau e banana), visando evitar falhas na padronização dos formulários sem impactar as regras vigentes de lavoura e floresta. | **Responsável:** Estela e Marcela.

**4. PRÓXIMOS PASSOS**

*   Aprovação e entrega final da planilha mestre de regras de negócio, contendo especificações visuais de obrigatoriedade, para homologação pela Engenharia de Testes.
*   Prototipação e validação da geração de relatórios gráficos de percepção em ambiente offline, configurando um deliverable inicial de alto impacto para os produtores em campo,.
*   Formalização técnica dos requisitos de infraestrutura e hospedagem do software baseada nas definições contratuais (web/mobile) para liberação das próximas etapas de arquitetura.