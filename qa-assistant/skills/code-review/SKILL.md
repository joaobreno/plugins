---
name: code-review
description: Use when reviewing a PR, MR, branch, or diff to find actionable defects and suggest concise code review comments.
---

# Revisão de código

Revise mudanças com foco em defeitos que afetem comportamento, segurança, dados, compatibilidade ou operação. Responda em português, salvo pedido diferente.

1. Identifique o PR/MR e a revisão analisada. Leia a descrição, requisitos disponíveis, diff e contexto necessário dos arquivos e dos chamadores. Use as integrações disponíveis; para um branch local, determine a base antes de comparar. Não suponha que a descrição comprova o comportamento.
2. Investigue os caminhos alterados, casos de erro e testes relevantes. Verifique cada suspeita no código e, quando útil, execute uma reprodução segura. Se faltar acesso ou contexto, declare a limitação; não invente achados.
3. Reporte apenas problemas concretos introduzidos pela alteração, ou diretamente agravados por ela. Para cada um, apresente prioridade, arquivo e linha, cenário que o desencadeia, consequência e correção sugerida quando útil. Faça comentários curtos, respeitosos e objetivos. Evite preferências de estilo e hipóteses não verificadas. Não repita achados.
4. Ordene por impacto: P0 bloqueia o uso ou causa dano amplo; P1 é grave e deve ser corrigido logo; P2 afeta um cenário relevante; P3 é um problema menor e concreto. Não atribua prioridade sem evidência.
5. Se não houver achados, diga isso claramente e informe limitações e riscos não verificados. Resuma os testes efetivamente executados. Uma revisão sem achados não é garantia de ausência de defeitos.

Use comentários inline quando o ambiente permitir e o usuário solicitar publicação. Não publique, aprove ou altere o PR/MR sem pedido explícito. Caso contrário, entregue os comentários na conversa, com referências navegáveis quando disponíveis.

Exemplo de comentário: **[P1] Preservar a transação ao falhar** — Se o segundo `save` falhar, o primeiro já terá sido gravado. Execute as duas gravações na mesma transação para evitar dados inconsistentes.
