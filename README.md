# manual-2-anos-ia

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Manual da IA](guia/assets/banner.jpg)](https://inematds.github.io/manual-2-anos-ia/guia/)

**ðŸ‡§ðŸ‡· [PortuguÃªs](README.md) Â· ðŸ‡ºðŸ‡¸ [English](README.en.md) Â· ðŸ‡ªðŸ‡¸ [EspaÃ±ol](README.es.md)**

## O que Ã©

Este Ã© um manual curto para quem sente ansiedade com as notÃ­cias de inteligÃªncia artificial. Ele organiza o assunto em 4 passos: entender o que aconteceu, saber quem estÃ¡ falando e por quÃª, medir o que muda no seu trabalho e agir em doses pequenas. Vem com 5 ferramentas simples, que rodam no seu computador sem internet, e com o passo a passo de como montar um manual parecido para a sua famÃ­lia, equipe ou escola. Para ler, basta abrir a pÃ¡gina; para as ferramentas, basta ter Python 3.

## ðŸ“– Guia de uso

Guia completo (landing + passo a passo): **https://inematds.github.io/manual-2-anos-ia/guia/**

## ðŸŽ¬ VÃ­deos

- **Completo (16:9, â‰ˆ6 min):** https://www.youtube.com/watch?v=DnkFeQDB8AI
- **Curto (9:16, 41 s):** https://www.youtube.com/watch?v=XFDDBRPuvwE

## O mÃ©todo: 4 passos (vocÃª nÃ£o controla o mar, sÃ³ o leme)

| Passo | Pergunta | Ferramenta |
|---|---|---|
| 1. [Entender os ventos](manual/01-entender-os-ventos.md) | O que aconteceu? | `campo.py` |
| 2. [Ver atravÃ©s da nÃ©voa](manual/02-ver-atraves-da-nevoa.md) | Quem fala, e por quÃª? (3 campos + governo, A Janela) | `janela.py`, `campo.py` |
| 3. [Achar o farol](manual/03-achar-o-farol.md) | O que muda no MEU trabalho? (modelo TLC) | `tlc.py` |
| 4. [Remar atÃ© a praia](manual/04-remar-ate-a-praia.md) | O que eu faÃ§o agora? | `tarefa_dia.py`, `contribuicao.py` |

VersÃ£o de uma pÃ¡gina para imprimir: **[manual/MANUAL.md](manual/MANUAL.md)**.
Como montar o seu prÃ³prio manual (processo + ferramentas): **[COMO-CRIAR-O-MANUAL.md](COMO-CRIAR-O-MANUAL.md)**.

## Estrutura

```
manual/                  o manual (1 arquivo por passo + MANUAL.md de uma pÃ¡gina)
ferramentas/             5 ferramentas em Python 3, sem dependÃªncia, sem internet
  janela.py              A Janela: anotar manchetes e ler no horÃ¡rio fixo
  campo.py               cartÃ£o de leitura de notÃ­cia (campo, incentivo, fato Ã— suposiÃ§Ã£o)
  tlc.py                 modelo TLC: ConfianÃ§a, Aprender, Contato
  tarefa_dia.py          uma tarefa por dia com IA + sequÃªncia
  contribuicao.py        sua contribuiÃ§Ã£o + plano de 4 semanas
  tests/                 16 testes (python3 -m unittest)
COMO-CRIAR-O-MANUAL.md   como transformar um tema em manual + vÃ­deos + ferramentas
guia/                    landing + guia (PT, en/, es/) no GitHub Pages
```

## O processo, do inÃ­cio ao fim

ðŸ§  sessÃ£o com o Nei Â· âš™ï¸ script Â· ðŸ¤– agente

| # | Passo | Comando | Quem |
|---|---|---|---|
| 1 | Escolher o tema e a referÃªncia; decidir o que o manual resolve | conversa | ðŸ§  |
| 2 | Baixar e transcrever a referÃªncia | `python baixar_v1.py --url <URL>` Â· `python transcrever_v1.py --in <video>` (inemavox) | âš™ï¸ |
| 3 | Extrair os passos, a metÃ¡fora e os exemplos; checar fatos com fonte | agente lendo a transcriÃ§Ã£o + busca na web | ðŸ¤– |
| 4 | Escrever o manual em `manual/` | ediÃ§Ã£o em Markdown | ðŸ¤– + ðŸ§  revisa |
| 5 | Escrever as ferramentas e os testes | `python3 -m unittest` | ðŸ¤– |
| 6 | Capa e banners (PT/EN/ES) | `gerar-capa.cjs` + `gerar-banner.sh --estilo live\|grade --lang pt\|en\|es` (Codex image_gen) e `cor_neutra.py corrigir` | ðŸ¤– |
| 7 | Guia PT em `guia/index.html` | skill `projetos-landing-guia` | ðŸ¤– |
| 8 | Traduzir guia e README para EN/ES | `inema-traduz` (tradutor central) | âš™ï¸ |
| 9 | Revisor independente | agente novo com a lista fixa | ðŸ¤– |
| 10 | Publicar o repo e o Pages | `git push` (Pages via GitHub Actions) | âš™ï¸ |
| 11 | Portal inema.club + inemabuscas + PRO | skill `atualiza-portal` | ðŸ¤– |
| 12 | VÃ­deos explicativos 16:9 e 9:16 do mesmo tema | explicavideos + estÃºdio HeyGen (outra sessÃ£o) | ðŸ¤– + ðŸ§  aprova |

## Rodar as ferramentas

```bash
git clone https://github.com/inematds/manual-2-anos-ia && cd manual-2-anos-ia
python3 -m unittest                     # 16 testes, deve dar OK
cd ferramentas
python3 janela.py add "manchete" --campo seguranca
python3 janela.py listar
python3 tlc.py "Minha tarefa" --confianca s --aprende n --contato n
python3 campo.py                        # modo interativo
python3 tarefa_dia.py feito "pedi para a IA resumir um e-mail"
python3 contribuicao.py plano 1 --para "meus pais"
```

Os dados ficam em `~/.manual-ia/` (mude com `MANUAL_IA_DADOS=/outra/pasta` ou `--arquivo`).

## Complemento

Kit prÃ¡tico (14 dias, IA offline, seguranÃ§a de contas, avaliar seu trabalho com IA):
**[sobreviver-ia](https://inematds.github.io/sobreviver-ia/guia/)**.

---

ConteÃºdo aberto e gratuito do **[INEMA.CLUB](https://inema.club)** Â· LicenÃ§a MIT.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>