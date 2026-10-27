# QA Cruzado

Plugin local para apoiar testes cruzados em equipes de desenvolvimento. Contém duas skills:

- **code-review**: revisa PR/MR ou diff e apresenta comentários concisos, fundamentados e priorizados.
- **manual-testing**: gera uma bateria interativa em HTML com resultado, observações e impressão para PDF.

## Uso

Disponibilize esta pasta como plugin local no ambiente Codex que suporta manifestos `.codex-plugin/plugin.json`. O método de instalação depende da configuração do ambiente; este pacote não se registra automaticamente. As skills também podem ser copiadas individualmente para o diretório de skills do Codex. Exemplos de pedido:

- “Use code-review to review this PR.”
- “Use manual-testing to create a manual test suite for this MR.”

Abra o HTML gerado em um navegador, registre os resultados e use **Exportar PDF** para imprimir e escolher **Salvar como PDF**. Os resultados são locais ao navegador e ao perfil, não sincronizados nem embutidos no HTML compartilhado. O armazenamento em arquivos locais depende do navegador; o PDF registra os estados visíveis no momento da impressão.

Os passos seguem princípios de linguagem simples inspirados em [asd-ste100-skill](https://github.com/danyuchn/asd-ste100-skill), sem alegação de conformidade com o padrão para textos em português.

## Ideias para evolução

1. **Triagem de risco e regressão:** escolher áreas e cenários de maior impacto a partir do diff.
2. **Reprodução e relato de defeitos:** transformar evidências em um relato conciso com passos, resultado e ambiente.
3. **Revisão de critérios de aceite:** identificar ambiguidades e exemplos ausentes antes da implementação.
4. **Investigação de testes instáveis:** distinguir falhas intermitentes de regressões, com evidências.
5. **Resumo de liberação:** consolidar mudanças, validações, pendências e riscos conhecidos.
