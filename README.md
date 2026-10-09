# Redocumentação de sistemas legados Java

Este repositório reúne o material necessário para compreender e reproduzir a pesquisa sobre geração e avaliação empírica de JavaDocs por modelos de linguagem em um sistema Java real.

## Escopo

O núcleo empírico da dissertação é a qualidade, utilidade, confiabilidade e adoção de JavaDocs gerados automaticamente. Documentação de API, arquitetura e testes manuais pertence ao projeto tecnológico mais amplo, mas não constitui o objeto principal da avaliação descrita aqui.

## Estrutura

- `dissertation/`: versão revisada da dissertação e controle das recomendações da banca.
- `pipeline/original-tool/`: ZIP original da ferramenta, preservado sem alteração.
- `methodology/`: protocolo do Estudo 01, planejamento do Estudo 02 e matriz de rastreabilidade.
- `docs/`: arquitetura, fluxo do pipeline e guia de reprodução.
- `artifacts/`: métricas agregadas e esquema dos artefatos produzidos.
- `data/`: política de disponibilidade e restrições dos dados institucionais.

## Resultado verificável da execução reproduzida

O inventário contém 1.478 alvos públicos: 521 classes, 866 métodos, 84 construtores e 7 enumerações. Apenas 9 alvos possuíam JavaDoc antes da intervenção. A execução registrada adicionou 1.466 JavaDocs, ignorou 9 alvos e rejeitou 3 respostas na validação.

## Início rápido

1. Verifique o hash do ZIP em `pipeline/original-tool/SHA256SUMS.txt`.
2. Extraia a ferramenta em diretório isolado.
3. Consulte `docs/reproducibility.md` para dependências, variáveis e sequência de execução.
4. Registre versão do código, modelo, parâmetros, prompt, idioma e política de seleção.
5. Preserve `manifest.json`, `javadoc_report.json`, logs e diff da execução.
6. Aplique o protocolo em `methodology/study-01-protocol.md` ou o desenho comparativo em `methodology/study-02-plan.md`.

## Ética e confidencialidade

O código-fonte do SARSB, transcrições integrais e artefatos institucionais não são publicados neste repositório. A reprodução técnica pode usar outro projeto Java; a replicação contextual no SARSB depende de autorização da instituição responsável.

