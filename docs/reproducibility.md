# Guia de reprodução

## Pré-requisitos

- Java e Maven compatíveis com o `pom.xml` do pacote original.
- Conta AWS com permissões mínimas para os serviços declarados na infraestrutura.
- Terraform para provisionamento, quando a reprodução incluir a infraestrutura completa.
- Acesso a um modelo compatível pelo Amazon Bedrock ou implementação equivalente das interfaces de cliente.

## Procedimento

1. Confira o SHA-256 do ZIP original.
2. Extraia o pacote sem alterar os arquivos de origem.
3. Revise arquivos de infraestrutura antes de aplicar Terraform e substitua valores específicos do ambiente.
4. Prepare um projeto Java autorizado em formato ZIP.
5. Registre commit ou hash do código de entrada.
6. Registre modelo, região, temperatura, limites, prompt, idioma e `maxTargets`.
7. Execute o pipeline.
8. Preserve `manifest.json`, `javadoc_report.json`, logs, código resultante e hash de cada saída.
9. Confirme que o diff contém apenas JavaDocs.
10. Selecione a amostra conforme o protocolo e entregue alterações em Merge Request contextualizada.
11. Conduza revisão individual antes do grupo focal.
12. Armazene codebook, citações codificadas e trilha das decisões analíticas.

## Critérios mínimos de sucesso

- inventário produzido sem perda de alvos elegíveis;
- zero alteração executável fora do escopo documental;
- métricas e parâmetros completos;
- rastreabilidade entre alvo, JavaDoc, validação e decisão do revisor;
- consentimento e proteção dos dados qualitativos.

