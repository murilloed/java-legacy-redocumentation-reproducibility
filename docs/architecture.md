# Arquitetura e processo

## Papéis lógicos

1. O agente de inventário executa o JavaParser e cria `manifest.json`.
2. O agente de priorização seleciona alvos por camada, complexidade, trivialidade e relevância.
3. O agente de geração monta o contexto e solicita o JavaDoc ao modelo.
4. O agente de validação verifica formato, aderência ao alvo e escopo da mudança.
5. O agente de integração insere comentários aceitos e registra métricas.

O termo agente identifica um componente especializado com entrada, saída e responsabilidade delimitadas. Nem todos os agentes precisam utilizar um modelo de linguagem.

## Fluxo de ponta a ponta

`ZIP do projeto -> S3 -> CodeBuild -> JavaParser -> manifesto -> seleção -> contexto -> Bedrock -> validação -> inserção -> relatórios -> ZIP de saída -> amostra -> Merge Request -> revisão humana`

S3, CodeBuild, Lambda, SQS, DynamoDB e EventBridge realizam armazenamento e orquestração. Não são variáveis empíricas da avaliação.

## Controle de integridade

Uma execução refinada deve comparar a AST antes e depois da inserção e bloquear qualquer diff que altere imports, assinaturas, anotações executáveis ou corpos de métodos. Somente comentários JavaDoc podem ser aceitos automaticamente para revisão.

