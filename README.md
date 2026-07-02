# zettelkasten-luhmann

**[English below](#english)**

Skill de Claude que aplica a mentalidade de Niklas Luhmann ao seu Zettelkasten no Obsidian: notas como **teses contestáveis** (não tópicos), **arquivamento forçado** (você decide onde cada nota entra — a decisão é o exercício) e **conexões-surpresa** entre clusters diferentes.

Luhmann escreveu 70 livros não acumulando conteúdo, mas forçando cada nota nova a entrar numa conversa com as existentes. Esta skill reproduz as três práticas que tornavam isso possível — e devolve a decisão a você, sempre.

## O que ela faz

1. **Da ideia à tese** — se o título descreve ("Observabilidade no sistema X"), ela provoca até virar afirmação ("Sem telemetria, todo incidente vira arqueologia"). Teste: dá para discordar do título? Se não, ainda é tópico.
2. **Corpo como argumento** — nas suas palavras, atômico, incluindo a melhor objeção contra a própria tese.
3. **Arquivamento forçado** — analisa seu vault e apresenta 2-4 notas candidatas com a relação nomeada (**contradiz · completa · exemplifica · responde**). Você escolhe. Ela nunca arquiva sozinha.
4. **Conexão bidirecional** — a nota nova linka a escolhida, e a escolhida ganha o link reverso com a relação. Nenhuma nota nasce órfã.
5. **A surpresa** — fecha sugerindo um vizinho improvável de outro domínio do vault, porque o arquivo "precisa ser capaz de surpreender" (Luhmann).

Funciona em qualquer idioma (conversa no seu idioma; escreve as notas no idioma do vault) e inicializa um vault do zero — estrutura de pastas + templates com a mentalidade embutida (`--lang pt|en`).

## Instalação

**Claude Code:**

```
/plugin marketplace add daniloneto/zettelkasten-luhmann
/plugin install zettelkasten-luhmann@zettelkasten-luhmann
```

**Claude Desktop / Cowork:** baixe o arquivo [`zettelkasten-luhmann.skill`](./zettelkasten-luhmann.skill), arraste na conversa e clique em **Save skill**.

## Uso

Fale naturalmente — a skill dispara sozinha:

- *"quero anotar isso: reunião de estimativa sempre ancora no primeiro número dito"*
- *"processa minhas fleeting notes"*
- *"quero começar um zettelkasten do zero, monta a estrutura"*
- *"turn this into a note: code reviews anchor on the first comment"*

## Resultados

Testada em 6 cenários (criação de nota, processamento de fleeting, resistência a pedido de resumo, bootstrap do zero, uso sem estrutura, multilíngue): **100%** dos critérios com a skill vs **28-50%** sem ela. O caso mais revelador: peça "uma nota resumindo o capítulo X" e ela resiste — resumo não atrita; tese sim.

---

<a name="english"></a>

# English

A Claude skill that applies Niklas Luhmann's mindset to your Obsidian Zettelkasten: notes as **contestable claims** (not topics), **forced filing decisions** (you choose where each note enters — the decision is the exercise), and **surprise connections** across clusters.

Luhmann wrote 70 books not by hoarding content, but by forcing every new note into a conversation with the existing ones. This skill reproduces the three practices that made it possible — and always hands the decision back to you.

## What it does

1. **From idea to claim** — if the title describes ("Observability in system X"), it pushes until it asserts ("Without telemetry, every incident becomes archaeology"). Test: can you disagree with the title? If not, it's still a topic.
2. **Body as argument** — your own words, atomic, including the best objection against your own claim.
3. **Forced filing** — scans your vault and presents 2-4 candidate notes with named relations (**contradicts · completes · exemplifies · answers**). You choose. It never files on its own.
4. **Bidirectional linking** — the new note links the chosen one, which gets a reverse link with the relation. No note is born an orphan.
5. **The surprise** — closes by suggesting an unlikely neighbor from a different domain, because the archive "must be able to surprise you" (Luhmann).

Works in any language (converses in yours; writes notes in the vault's language) and can bootstrap a vault from scratch — folder structure + templates with the mindset built in (`--lang pt|en`).

## Install

**Claude Code:**

```
/plugin marketplace add YOUR-USERNAME/zettelkasten-luhmann
/plugin install zettelkasten-luhmann@zettelkasten-luhmann
```

**Claude Desktop / Cowork:** download [`zettelkasten-luhmann.skill`](./zettelkasten-luhmann.skill), drop it into a conversation and click **Save skill**.

## Usage

Just talk — the skill triggers on its own:

- *"turn this into a note: code reviews always anchor on the first comment"*
- *"process my fleeting notes"*
- *"I want to start a zettelkasten from scratch"*

## Results

Tested on 6 scenarios (note creation, fleeting processing, resisting summary requests, bootstrap from scratch, use without structure, multilingual): **100%** of criteria with the skill vs **28-50%** without. The most telling case: ask for "a note summarizing chapter X" and it resists — summaries don't create friction; claims do.

## License

MIT © 2026 Danilo Neto (daniloneto)
