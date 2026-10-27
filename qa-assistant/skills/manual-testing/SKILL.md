---
name: manual-testing
description: Use when generating an actionable manual test battery for a change, PR, MR, feature, or bug fix as an interactive HTML artifact with PDF printing.
---

# Bateria de testes manuais

Gere um HTML autônomo a partir da alteração real e dos requisitos disponíveis. Responda em português, salvo pedido diferente.

1. Inspecione o PR/MR, diff, requisitos e comportamento relacionado. Identifique fluxos afetados, permissões, estados, dependências e riscos. Se não houver informação suficiente para afirmar um resultado, registre a dúvida ou pré-condição; não apresente suposições como fatos. Não execute ações destrutivas ou em produção sem autorização.
2. Priorize cenários que possam revelar regressões: caminho principal, validações e limites, erros, permissões e fluxos adjacentes quando relevantes. Evite casos redundantes e não invente dados, URLs ou credenciais. Registre ambiente, dados e preparação necessários; use valores de exemplo identificados como tais.
3. Cada caso deve ter um identificador único e estável, título, prioridade, pré-condições, passos numerados e resultados esperados verificáveis. Associe cada resultado ao passo ou ao caso claramente. Inclua cobertura das mudanças, riscos não cobertos e dúvidas pertinentes.
4. Escreva instruções em linguagem simples, inspirada nos princípios de [ASD-STE100 Skill](https://github.com/danyuchn/asd-ste100-skill): uma ação por passo, voz ativa, verbos concretos, termos consistentes e condições explícitas. Preserve o significado e a precisão. A referência trata de inglês; não afirme conformidade ASD-STE100 para português.
5. Copie `assets/bateria.html` para o destino solicitado ou para o diretório de trabalho com nome descritivo. Substitua os dados de exemplo no elemento `script` de id `dados-bateria` por JSON válido, mantendo o esquema do modelo. Escape `<` em valores JSON como `\u003c` para impedir fechamento acidental do script. Gere um `id` único por bateria, estável nas revisões destinadas a preservar marcações; altere-o para baterias independentes. Não inclua segredos no HTML.
6. Abra ou inspecione o resultado quando possível. Verifique conteúdo, navegação, alterações de status e notas, persistência após recarregar e layout de impressão. O botão PDF abre a impressão do navegador; o usuário deve escolher Salvar como PDF. Informe que os dados ficam no armazenamento local daquele navegador e perfil, sujeito às restrições de arquivos locais, e não são sincronizados. A impressão reflete os estados e notas atuais. Ao compartilhar, explique que o HTML sozinho não leva os registros locais; imprima em PDF para registrar os resultados.

Estados: Não iniciado, Aprovado, Reprovado, Bloqueado e Não aplicável. Um caso reprovado ou bloqueado deve ter espaço para observação. Não marque casos como executados sem evidência de execução humana ou de ferramenta.
