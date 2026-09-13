# 🛠️ Registro de Engenharia de Prompts e "Cicatrizes" (Troubleshooting)

Este documento registra o processo experimental de interação com o **NotebookLM**, utilizando como base de conhecimento os arquivos do **Guia PMBOK® 6ª Edição** e **Guia PMBOK® 7ª Edição**. 

O objetivo é evidenciar o raciocínio crítico por trás da formulação das perguntas, documentando os gargalos encontrados (respostas vagas, alucinações de contexto ou omissões) e as estratégias adotadas para refinar os prompts até obter respostas técnicas precisas.

Caso 1: O Status dos Processos e ITTOs no PMBOK 7
Contexto da Consulta
Investigar se a transição para a 7ª edição tornou os 49 processos e as ferramentas/técnicas (ITTOs) da 6ª edição oficialmente obsoletos perante o PMI.

Tentativa 1 (Prompt Ingênuo)
"O que aconteceu com os 49 processos do PMBOK 6 na 7ª edição? Eles foram excluídos e não valem mais?"

Comportamento da IA / Resposta Obtida: O modelo respondeu de forma binária, indicando que a 7ª edição substituiu a estrutura de processos por 12 princípios e 8 domínios de desempenho, sugerindo erroneamente que os processos haviam sido descontinuados pelo PMI.

Diagnóstico da Falha ("Cicatriz"): A pergunta continha viés indutivo e não delimitou fontes normativas institucionais. O modelo simplificou a mudança sem contextualizar a convivência dos dois modelos.

Prompt Refinado:

"Com base exclusivamente nas seções 'Prefácio' e 'Resumo das Mudanças' do Guia PMBOK 7ª edição, responda: A 7ª edição invalida ou cancela a abordagem baseada em processos da 6ª edição? Estruture a resposta em: (1) Posicionamento oficial do PMI sobre a abordagem de processos; (2) O papel da plataforma digital PMIstandards+; (3) Como o conceito de Tailoring conecta os dois paradigmas."

Resultado Obtido: A IA extraiu a citação literal do Prefácio da 7ª edição demonstrando que "nada nesta edição nega o alinhamento com a abordagem baseada em processos de edições anteriores", explicando a migração do acervo prático para o PMIstandards+ e a necessidade de adaptação (tailoring).

Caso 2: De-Para entre Áreas de Conhecimento e Domínios de Desempenho
Contexto da Consulta
Mapear a equivalência técnica entre a gestão de prazos/tempo na 6ª edição e a nova estrutura sistêmica da 7ª edição.

Tentativa 1 (Prompt Ingênuo)
"Como ficou a gestão do tempo na 7ª edição em comparação com a 6ª?"

Comportamento da IA / Resposta Obtida: O modelo gerou um texto genérico sobre produtividade e cumprimento de prazos, ignorando que na 6ª edição o termo formal já havia mudado para "Gerenciamento do Cronograma" e não mapeou o domínio correspondente no PMBOK 7.

Diagnóstico da Falha ("Cicatriz"): Linguagem coloquial no prompt levou a alucinações de senso comum em vez de respostas ancoradas na taxonomia formal dos guias.

Prompt Refinado:

"Atuando como um especialista em certificação PMP, construa uma matriz comparativa entre a Área de Conhecimento 'Gerenciamento do Cronograma' (PMBOK 6) e o 'Domínio de Desempenho do Planejamento' (PMBOK 7). A resposta deve ser uma tabela contendo: (1) Foco principal de cada edição; (2) Métricas de controle utilizadas; (3) Ferramentas mantidas em comum (ex.: CPM, Gráfico de Gantt, EAP)."

Resultado Obtido: O NotebookLM gerou uma tabela técnica precisa, diferenciando o controle rígido de linhas de base (6ª ed.) do planejamento orientado a cadências de entrega (preditiva, iterativa ou híbrida na 7ª ed.), mantendo as ferramentas clássicas de cronograma como métodos válidos.

Caso 3: Tratamento de Risco vs. Domínio da Incerteza
Contexto da Consulta
Compreender a ampliação conceitual da gestão de riscos para o domínio de incerteza no gerenciamento moderno de projetos.

Tentativa 1 (Prompt Ingênuo)
"Qual a diferença entre risco no PMBOK 6 e no PMBOK 7?"

Comportamento da IA / Resposta Obtida: A resposta apenas repetiu a definição clássica de risco (evento incerto com impacto positivo ou negativo) e listou os processos da 6ª edição, ignorando as nuances teóricas inseridas na 7ª edição.

Diagnóstico da Falha ("Cicatriz"): Faltou instrução explícita de contraste conceitual, fazendo o modelo recorrer ao texto quantitativamente maior da base (PMBOK 6).

Prompt Refinado:

"Compare o 'Gerenciamento dos Riscos' (PMBOK 6) com o 'Domínio de Desempenho da Incerteza' (PMBOK 7). Detalhe: (1) Por que o escopo foi expandido de 'risco' para 'incerteza'; (2) Como os conceitos de ambiguidade, complexidade e volatilidade são abordados na 7ª edição; (3) Quais estratégias de respostas a ameaças e oportunidades permanecem idênticas em ambas as edições."

Resultado Obtido: Resposta estruturada demonstrando que a incerteza engloba fatores não probabilísticos (como ambiguidade de requisitos e complexidade sistêmica), enquanto confirmou a permanência das estratégias clássicas de resposta (evitar, transferir, mitigar, aceitar, explorar, compartilhar e melhorar).
