# Plugins pessoais

Marketplace pessoal de plugins para ajudar em rotinas de desenvolvimento. Cada plugin mantém uma única cópia de suas skills, com manifestos para Codex/ChatGPT, Claude Code e Cursor.

## Plugins

| Plugin | Skills | Descrição |
| --- | --- | --- |
| [QA Assistant](qa-assistant/README.md) | `code-review`, `manual-testing` | Revisão de código e testes manuais para equipes sem QA dedicado. |

## Codex e ChatGPT desktop

No Codex, adicione o marketplace pelo terminal:

```sh
codex plugin marketplace add joaobreno/plugins
```

No ChatGPT desktop ou Codex, abra o diretório de plugins, selecione **João Breno Plugins** e instale **QA Assistant**. Reinicie o aplicativo se o catálogo não aparecer e inicie uma nova conversa após a instalação. A disponibilidade depende do aplicativo, plano e políticas do workspace. Este catálogo não publica o plugin automaticamente no diretório público da OpenAI. [Documentação](https://developers.openai.com/plugins/build/plugins).

## Claude Code

No terminal:

```sh
claude plugin marketplace add joaobreno/plugins
claude plugin install qa-assistant@joaobreno-plugins
```

Inicie uma sessão e use `/qa-assistant:code-review` ou `/qa-assistant:manual-testing`. [Documentação](https://code.claude.com/docs/en/plugin-marketplaces).

## Cursor

Em um workspace de equipe compatível, um administrador pode importar `https://github.com/joaobreno/plugins` em **Dashboard → Plugins & MCPs → Team Marketplaces → Add Marketplace → Import from Repo**, revisar o plugin e disponibilizá-lo. O manifesto `.cursor-plugin/marketplace.json` descreve o catálogo; ele não o publica automaticamente no marketplace público do Cursor. A publicação pública exige submissão e revisão. [Documentação](https://cursor.com/docs/plugins).

Como alternativa pessoal, copie os diretórios em `qa-assistant/skills/` para `~/.cursor/skills/` e inicie uma nova sessão. Veja [Agent Skills no Cursor](https://cursor.com/docs/context/skills).

## Organização

Os catálogos estão em `.agents/plugins/marketplace.json`, `.claude-plugin/marketplace.json` e `.cursor-plugin/marketplace.json`. Cada diretório de plugin contém seus manifestos, `skills/` e documentação. Ao adicionar um plugin, inclua-o nos catálogos desejados e consulte a documentação de cada plataforma.
