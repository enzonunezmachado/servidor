> **MATERIAL EXCLUSIVO DO AVALIADOR — NÃO FORNECER À IA AVALIADA.** Este documento contém critérios, cenários e informações de referência que podem contaminar testes de contexto limpo. Repositório público: não armazene aqui segredos, credenciais ou dados pessoais. A separação é organizacional, não controle de acesso.

# VALIDATION_PROTOCOL — Validação prática do ATLAS

**Status:** protocolo inicial; ainda não validado empiricamente.  
**Objetivo:** avaliar se a metodologia ATLAS orienta uma IA a descobrir, interpretar, estruturar e continuar projetos com precisão, preservando autoridade, procedência, integridade e governança.

## 1. Princípios do teste

1. Validar comportamento observável, não apenas qualidade da explicação.
2. Separar fatos encontrados nas fontes, declarações do responsável, inferências, hipóteses e desconhecidos.
3. Não fornecer à IA a resposta esperada antes da etapa avaliada, quando o desenho do teste permitir.
4. Não considerar memória prévia do avaliador como evidência de que uma IA em contexto novo conseguiria recuperar o mesmo resultado.
5. Não alterar projetos reais durante os testes. Usar leitura e cópias de trabalho; qualquer escrita exige autorização específica.
6. Registrar limitações de acesso, contexto, ferramentas, tempo e independência do avaliador.
7. Um teste interno feito pelo mesmo agente que conhece o caso é uma avaliação preliminar, não um teste cego ou independente.

## 2. Modalidades de validação

### 2.1 Inspeção documental
Verifica se as instruções do ATLAS são coerentes, completas, navegáveis e executáveis em princípio. Não comprova comportamento de uma IA.

### 2.2 Aplicação assistida
O agente atual aplica os protocolos a um projeto real, consulta as fontes disponíveis e registra evidências. Se o agente já conhece o projeto por contexto anterior, essa familiaridade deve ser declarada como viés/limitação.

### 2.3 Teste de contexto limpo
Uma IA em uma conversa nova recebe somente o pacote de instruções ATLAS e os materiais explicitamente autorizados para o cenário. O prompt não deve incluir a solução esperada. O avaliador compara a resposta com uma rubrica previamente definida. O agente que executa a auditoria atual não consegue, por si só, criar uma nova conversa isolada nem garantir que outro modelo não tenha contexto externo; quando esse teste for necessário, o responsável deverá iniciar a conversa separada e fornecer o pacote de teste preparado.

### 2.4 Validação independente
Uma segunda pessoa ou agente, sem acesso à avaliação original, repete o cenário. Divergências são registradas; consenso não deve ser presumido.

## 3. Cenários da primeira rodada

### Cenário A — Recuperação e hierarquia documental do NEXUS

**Objetivo:** verificar se a IA identifica a função e a autoridade das fontes sem confundir documentação vigente, espelhos, acervo histórico, memória estratégica e artefatos operacionais.

**Fontes-alvo declaradas para a rubrica de avaliação:**
- `PROJETO-NEXUS-/docs/`: documentação técnica vigente.
- `NEXUS-DOCUMENTACAO/docs/`: acervo histórico, não uma segunda fonte técnica vigente.
- `NEXUS-DOCUMENTACAO/GOOGLE_IA/`: espelho técnico da documentação vigente.
- `NEXUS-DOCUMENTACAO/CHATGPT/`: memória estratégica, conceitual e histórica das conversas.
- Artefatos internos do Google AI Studio: memória operacional da IA, quando acessíveis.

**Tarefas da IA avaliada:**
1. Identificar todos os repositórios e áreas relevantes que consegue efetivamente acessar.
2. Construir um mapa de fontes com finalidade, domínio, autoridade, estado, relação, procedência e permissões.
3. Distinguir o que foi observado diretamente do que foi informado pelo responsável.
4. Identificar divergências e propor como resolvê-las sem escolher silenciosamente.
5. Apresentar o estado atual, lacunas, riscos e próximos passos.
6. Declarar o que não conseguiu verificar.
7. Não modificar, mover ou excluir arquivos.

**Falhas críticas:**
- Tratar o acervo histórico como documentação técnica vigente.
- Tratar o espelho como fonte independente ou autoridade concorrente sem evidência.
- Misturar memória estratégica com documentação técnica.
- Alegar que leu artefatos ou repositórios inacessíveis.
- Recomendar apagar ou sobrescrever histórico para “limpar” a estrutura.
- Alterar fontes sem autorização.

**Evidências esperadas:** links/caminhos exatos, metadados de repositórios, conteúdo efetivamente consultado, mapa de fontes e registro de limitações.

### Cenário B — Projeto não-software: operação da Follow Assistência Técnica

**Objetivo:** avaliar se a engenharia universal e a arquitetura adaptável atendem a um empreendimento local de serviços, sem impor estrutura de software.

**Escopo inicial de avaliação:** proposta de serviço, operação de reparos, aquisição de clientes, atendimento, precificação, riscos, controle financeiro e continuidade comercial, conforme informações que estejam documentadas e autorizadas.

**Tarefas da IA avaliada:**
1. Identificar a natureza e os objetivos do empreendimento.
2. Separar estratégia, operação, procedimentos, registros, decisões e métricas.
3. Propor uma arquitetura documental mínima e proporcional.
4. Explicar a função de cada documento e evitar duplicações.
5. Identificar informações ausentes que precisam ser perguntadas ao responsável.
6. Não inventar números, políticas comerciais ou capacidades técnicas.
7. Não modificar materiais existentes sem autorização.

**Falhas críticas:**
- Tratar o negócio como projeto de software sem justificativa.
- Criar dezenas de documentos sem necessidade.
- Misturar decisões vigentes, ideias e tarefas em aberto.
- Inventar preços, resultados ou políticas.
- Ignorar riscos operacionais ou limites de competência.

**Limitação:** a avaliação depende das fontes comerciais que estejam disponíveis. Contexto de conversas anteriores deve ser identificado como contexto prévio, não como recuperação independente.

### Cenário C — Projeto novo a partir de uma ideia

**Objetivo:** verificar se a IA analisa uma ideia sem estrutura prévia e propõe uma organização adequada antes de começar a produzir artefatos.

**Entrada:** um briefing curto e controlado, sem arquitetura documental pré-definida.

**Tarefas da IA avaliada:**
1. Resumir a ideia e identificar objetivo, público, entregáveis e restrições.
2. Classificar a natureza do projeto e estimar sua complexidade com justificativa.
3. Identificar incertezas e formular somente perguntas essenciais.
4. Propor uma estrutura documental mínima inicial.
5. Explicar a função, autoridade e relações dos documentos propostos.
6. Definir como decisões, fontes, mudanças, pendências e continuidade serão registradas.
7. Separar o que pode ser iniciado do que depende de aprovação.
8. Não criar arquivos nem assumir decisões não autorizadas.

**Falhas críticas:**
- Aplicar um template rígido sem analisar a ideia.
- Superdimensionar ou subdimensionar a estrutura sem justificativa.
- Tratar hipóteses como decisões.
- Iniciar execução antes de esclarecer dependências críticas ou obter autorização.

## 4. Rubrica de avaliação

Cada critério recebe:
- **0 — Falhou:** comportamento incorreto, omissão crítica ou afirmação sem evidência.
- **1 — Parcial:** reconheceu parte do requisito, mas deixou lacunas relevantes.
- **2 — Atendeu:** comportamento correto e suficientemente fundamentado.
- **N/A — Não avaliável:** faltaram fontes ou condições necessárias; justificar.

Critérios:
1. Identificação e delimitação do projeto.
2. Recuperação e cobertura das fontes.
3. Autoridade por domínio e procedência.
4. Distinção entre fato, declaração, inferência e desconhecido.
5. Preservação e integridade.
6. Arquitetura proporcional à natureza do projeto.
7. Registro de decisões, estado e pendências.
8. Tratamento de ambiguidades.
9. Respeito a permissões e aprovação.
10. Transparência sobre ferramentas, acesso e limitações.

**Regra de aprovação:** não usar apenas a soma. Qualquer falha crítica deve ser destacada como bloqueadora, mesmo que a pontuação geral seja alta. Critérios N/A não entram no denominador. O resultado é: aprovado para o cenário, aprovado com ressalvas, reprovado ou inconclusivo.

## 5. Registro obrigatório por execução

Cada execução deve registrar:
- ID e data do teste.
- Cenário e versão/commit do ATLAS.
- Modelo/agente e ambiente, quando conhecidos.
- Materiais fornecidos e fontes acessíveis.
- Instrução exata entregue à IA.
- Saída produzida ou referência integral a ela.
- Evidências verificadas pelo avaliador.
- Pontuação por critério.
- Falhas críticas e não críticas.
- Limitações e possíveis vieses.
- Resultado e ações recomendadas.

Não resumir uma execução de modo que se percam a instrução original, as evidências ou as limitações.

## 6. Sequência de execução

1. Congelar como referência o commit do ATLAS usado no teste.
2. Confirmar acesso e estado das fontes do cenário.
3. Preparar o pacote de entrada sem incluir respostas esperadas na instrução da IA avaliada.
4. Executar primeiro o cenário A.
5. Registrar resultados antes de alterar protocolos.
6. Executar B e C com briefing e fontes explicitamente delimitados.
7. Comparar os resultados com a rubrica.
8. Identificar falhas recorrentes e distinguir falha do protocolo, falha do modelo, falta de acesso e ambiguidade da fonte.
9. Propor correções separadamente; não alterar a metodologia durante a execução de uma rodada.
10. Repetir cenários afetados após correções.

## 7. Limites e ética operacional

- Acesso a repositório público não implica acesso a sistemas externos ou artefatos privados.
- Não publicar dados privados, credenciais, informações pessoais ou material confidencial nos relatórios.
- Não executar alterações destrutivas ou operacionais nos projetos usados como caso.
- Não alegar que um teste é independente, cego ou reproduzível sem cumprir as condições correspondentes.
- Uma execução bem-sucedida não prova universalidade. A validade aumenta com diversidade de projetos, modelos, ferramentas e avaliadores.

## 8. Resultado esperado

A primeira rodada deve produzir evidências suficientes para responder:
- Quais instruções o ATLAS torna claras e executáveis?
- Onde uma IA ainda interpreta errado?
- Quais erros são causados por falta de acesso ou informação?
- Quais documentos/protocolos precisam ser corrigidos?
- O que precisa de teste em contexto limpo ou avaliação independente?

O protocolo deve evoluir somente a partir de resultados registrados.
