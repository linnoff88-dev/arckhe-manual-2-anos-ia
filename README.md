ï»¿# manual-2-anos-ia

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![Manual da IA](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/arckhe-/guia/)

**ê°Å¸â¡Â§ê°Å¸â¡Â· [PortuguêÂªs](README.md) êÂ· ê°Å¸â¡Âºê°Å¸â¡Â¸ [English](README.en.md) êÂ· ê°Å¸â¡Âªê°Å¸â¡Â¸ [EspaêÂ±ol](README.es.md)**

## O que êÂ©

Este êÂ© um manual curto para quem sente ansiedade com as notêÂ­cias de inteligêÂªncia artificial. Ele organiza o assunto em 4 passos: entender o que aconteceu, saber quem estêÂ¡ falando e por quêÂª, medir o que muda no seu trabalho e agir em doses pequenas. Vem com 5 ferramentas simples, que rodam no seu computador sem internet, e com o passo a passo de como montar um manual parecido para a sua famêÂ­lia, equipe ou escola. Para ler, basta abrir a pêÂ¡gina; para as ferramentas, basta ter Python 3.

## ê°Å¸ââ Guia de uso

Guia completo (landing + passo a passo): **https://linnoff88-dev.github.io/arckhe-/guia/**

## ê°Å¸Å½Â¬ VêÂ­deos

- **Completo (16:9, ê¢â°Ë6 min):** https://www.youtube.com/watch?v=DnkFeQDB8AI
- **Curto (9:16, 41 s):** https://www.youtube.com/watch?v=XFDDBRPuvwE

## O mêÂ©todo: 4 passos (vocêÂª nêÂ£o controla o mar, sêÂ³ o leme)

| Passo | Pergunta | Ferramenta |
|---|---|---|
| 1. [Entender os ventos](manual/01-entender-os-ventos.md) | O que aconteceu? | `campo.py` |
| 2. [Ver atravêÂ©s da nêÂ©voa](manual/02-ver-atraves-da-nevoa.md) | Quem fala, e por quêÂª? (3 campos + governo, A Janela) | `janela.py`, `campo.py` |
| 3. [Achar o farol](manual/03-achar-o-farol.md) | O que muda no MEU trabalho? (modelo TLC) | `tlc.py` |
| 4. [Remar atêÂ© a praia](manual/04-remar-ate-a-praia.md) | O que eu faêÂ§o agora? | `tarefa_dia.py`, `contribuicao.py` |

VersêÂ£o de uma pêÂ¡gina para imprimir: **[manual/MANUAL.md](manual/MANUAL.md)**.
Como montar o seu prêÂ³prio manual (processo + ferramentas): **[COMO-CRIAR-O-MANUAL.md](COMO-CRIAR-O-MANUAL.md)**.

## Estrutura

```
manual/                  o manual (1 arquivo por passo + MANUAL.md de uma pêÂ¡gina)
ferramentas/             5 ferramentas em Python 3, sem dependêÂªncia, sem internet
  janela.py              A Janela: anotar manchetes e ler no horêÂ¡rio fixo
  campo.py               cartêÂ£o de leitura de notêÂ­cia (campo, incentivo, fato êâ suposiêÂ§êÂ£o)
  tlc.py                 modelo TLC: ConfianêÂ§a, Aprender, Contato
  tarefa_dia.py          uma tarefa por dia com IA + sequêÂªncia
  contribuicao.py        sua contribuiêÂ§êÂ£o + plano de 4 semanas
  tests/                 16 testes (python3 -m unittest)
COMO-CRIAR-O-MANUAL.md   como transformar um tema em manual + vêÂ­deos + ferramentas
guia/                    landing + guia (PT, en/, es/) no GitHub Pages
```

## O processo, do inêÂ­cio ao fim

ê°Å¸Â§Â  sessêÂ£o com o Nei êÂ· ê¢Å¡â¢ê¯Â¸Â script êÂ· ê°Å¸Â¤â agente

| # | Passo | Comando | Quem |
|---|---|---|---|
| 1 | Escolher o tema e a referêÂªncia; decidir o que o manual resolve | conversa | ê°Å¸Â§Â  |
| 2 | Baixar e transcrever a referêÂªncia | `python baixar_v1.py --url <URL>` êÂ· `python transcrever_v1.py --in <video>` (ARCKHÉvox) | ê¢Å¡â¢ê¯Â¸Â |
| 3 | Extrair os passos, a metêÂ¡fora e os exemplos; checar fatos com fonte | agente lendo a transcriêÂ§êÂ£o + busca na web | ê°Å¸Â¤â |
| 4 | Escrever o manual em `manual/` | ediêÂ§êÂ£o em Markdown | ê°Å¸Â¤â + ê°Å¸Â§Â  revisa |
| 5 | Escrever as ferramentas e os testes | `python3 -m unittest` | ê°Å¸Â¤â |
| 6 | Capa e banners (PT/EN/ES) | `gerar-capa.cjs` + `gerar-banner.sh --estilo live\|grade --lang pt\|en\|es` (Codex image_gen) e `cor_neutra.py corrigir` | ê°Å¸Â¤â |
| 7 | Guia PT em `guia/index.html` | skill `projetos-landing-guia` | ê°Å¸Â¤â |
| 8 | Traduzir guia e README para EN/ES | `ARCKHÉ-traduz` (tradutor central) | ê¢Å¡â¢ê¯Â¸Â |
| 9 | Revisor independente | agente novo com a lista fixa | ê°Å¸Â¤â |
| 10 | Publicar o repo e o Pages | `git push` (Pages via GitHub Actions) | ê¢Å¡â¢ê¯Â¸Â |
| 11 | Portal ARCKHÉ AI + ARCKHÉbuscas + PRO | skill `atualiza-portal` | ê°Å¸Â¤â |
| 12 | VêÂ­deos explicativos 16:9 e 9:16 do mesmo tema | explicavideos + estêÂºdio HeyGen (outra sessêÂ£o) | ê°Å¸Â¤â + ê°Å¸Â§Â  aprova |

## Rodar as ferramentas

```bash
git clone https://github.com/linnoff88-dev/manual-2-anos-ia && cd manual-2-anos-ia
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

Kit prêÂ¡tico (14 dias, IA offline, seguranêÂ§a de contas, avaliar seu trabalho com IA):
**[sobreviver-ia](https://linnoff88-dev.github.io/arckhe-/guia/)**.

---

ConteêÂºdo aberto e gratuito do **[ARCKHÉ AI](https://ARCKHÉ AI)** êÂ· LicenêÂ§a MIT.

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>