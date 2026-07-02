# Contribuindo / Contributing

**[English below](#english)**

Obrigado pelo interesse! Este projeto aceita contribuições via pull request — todo PR passa pela revisão e aprovação do mantenedor antes do merge (regra de branch ativa na `main`).

## Como contribuir

1. Faça um fork e crie uma branch descritiva (`fix/deteccao-idioma`, `feat/template-review`).
2. Faça sua mudança. Os dois arquivos que importam:
   - `skills/zettelkasten-luhmann/SKILL.md` — as instruções da skill
   - `skills/zettelkasten-luhmann/scripts/init_vault.py` — o bootstrap do vault
3. **Teste antes de abrir o PR** (veja abaixo).
4. Abra o PR preenchendo o template. PRs pequenos e focados são revisados mais rápido.

## Como testar

A skill é instrução para o Claude, então o teste é comportamental. Rode estes cenários numa sessão do Claude (Code, Desktop ou Cowork) com a sua versão da skill instalada:

| Cenário | Prompt de exemplo | O que deve acontecer |
|---|---|---|
| Nota nova | "quero anotar isso: [ideia]" | Propõe títulos-tese; apresenta 2-4 candidatas com relação nomeada; **pergunta** onde arquivar; cria com link bidirecional; sugere vizinho improvável |
| Pegadinha do resumo | "faz uma nota resumindo o capítulo X de [livro]" | Resiste ao resumo e converte em tese/comentário próprio |
| Bootstrap | "quero começar um zettelkasten do zero" | Roda `init_vault.py`, não sobrescreve nada existente |
| Sem estrutura | pedir nota numa pasta sem vault | Detecta a ausência ANTES de criar qualquer arquivo e oferece inicialização |
| Idioma | prompt em outro idioma | Conversa no idioma do usuário; nota no idioma do vault |

Para o `init_vault.py`, também vale teste direto: rodar duas vezes no mesmo destino (a segunda não pode criar nem sobrescrever nada) e rodar com `--lang en`.

## Princípios do projeto (leia antes de propor mudanças grandes)

- **A decisão é do usuário.** Qualquer mudança que faça a skill arquivar, escolher título ou conectar automaticamente será recusada — o atrito da decisão é o produto.
- **Tese > tópico.** Mudanças que suavizem a provocação ("pode ser um resumo se o usuário insistir muito") vão contra o propósito.
- **SKILL.md enxuto.** Explique o porquê das instruções em vez de adicionar regras rígidas; se sua adição passar de ~15 linhas, considere um arquivo em `references/`.
- Novos idiomas no `init_vault.py` são bem-vindos (adicione o dicionário de templates + starter e a opção em `--lang`).

## Issues

Bugs, ideias e relatos de uso são bem-vindos nas issues — em português ou inglês.

---

<a name="english"></a>

# English

Thanks for your interest! Contributions come in via pull request — every PR requires maintainer review and approval before merging (branch rule active on `main`).

**How to contribute:** fork, create a descriptive branch, change one of the two files that matter (`skills/zettelkasten-luhmann/SKILL.md` or `scripts/init_vault.py`), test, open a PR using the template.

**How to test:** the skill is behavioral, so run the scenarios from the table above in a Claude session with your version installed — new note flow, the summary trap, bootstrap, missing-structure detection, and language handling. For `init_vault.py`, also run it twice against the same target (second run must create/overwrite nothing) and with `--lang en`.

**Project principles:** the user makes the decision (changes that auto-file, auto-title or auto-connect will be declined — the friction is the product); claim beats topic; keep SKILL.md lean and explain the why. New languages in `init_vault.py` are welcome.
