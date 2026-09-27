# Como escrever os Patch Notes do launcher

O painel **Patch News** do launcher (à direita do carrossel) lê arquivos `.md`
deste repositório. Não precisa gerar release nem recompilar o launcher:
é só editar/commitar aqui.

## 1. Onde ficam os arquivos

- Na **raiz** do repositório (ex.: `patchnews.md`, `battlepass.md`)
- ou na pasta `launcher_content/` (tem prioridade sobre a raiz, se existir).

## 2. Quais arquivos aparecem

Definido pelo campo `textshow` do config. Cada nome vira uma "página" do painel,
que gira sozinha a cada **6 segundos** (pausa com o mouse em cima; bolinhas embaixo trocam a página).

```json
"textshow": "patchnews,battlepass"
```

- Separe por vírgula, na ordem em que devem aparecer.
- Sem extensão, o launcher assume `.md` (`patchnews` → `patchnews.md`).
- Extensões aceitas: `.md`, `.txt`, `.html`.

> ⚠️ **Existem DOIS configs**: `launcher_config.json` (cliente CipSoft) e
> `launcher_config_ftc.json` (FantasyClient/OTC). O launcher lê o do cliente
> que o jogador escolheu. **Ao adicionar/remover uma página, altere o `textshow` nos dois.**
> O mesmo vale para `imgsshow` (carrossel) e `background_image`.

## 3. Formatação suportada

O launcher tem um conversor de Markdown **simples**. Só isto funciona:

| Escreva | Resultado |
|---|---|
| `# Título` | título grande (dourado) |
| `## Subtítulo` | subtítulo (laranja) |
| `### Seção` | seção (dourado, menor) |
| `**texto**` | negrito (branco) |
| `- item` | lista com marcador |
| `---` (linha sozinha) | linha separadora |

**NÃO funciona** (aparece como texto cru): `*itálico*`, `[link](url)`, listas numeradas `1.`,
listas com `*` ou `+`, tabelas, imagens `![]()`, blocos de código.

Para o que o Markdown não cobre, use **HTML direto** no arquivo:

```html
<i>itálico</i>
<a href="https://fantasydream.online">link clicável</a>
<span style="color:#7CFC9A;">texto verde</span>
```

### Cuidados
- Use **`- `** (hífen + espaço) no início da linha para listas. `* item` não vira lista.
- **Não use `---` no meio de frases**: qualquer `---` vira linha separadora.
- Emojis funcionam normalmente (📰 🏆 ⚔️).
- O painel é pequeno (~580×320 px) e rola com o mouse. Prefira textos curtos,
  com as novidades mais importantes no topo.

## 4. Modelo recomendado

Copie e adapte para `patchnews.md`:

```markdown
# 📰 Atualização 1.0.40

## 26/09/2026

### ✨ Novidades
- **Nome do sistema**: descrição curta do que mudou
- Novo evento **Nome do Evento** até 10/10

### 🔧 Correções
- Corrigido bug em ...
- Melhorias de performance

### ⚖️ Balanceamento
- Magia **X**: dano aumentado em 10%

---

**Dúvidas? Chame no Discord!**
```

Regras de estilo:
- Um `#` só, com a versão no topo.
- Data em `##`, seções em `###`.
- Mantenha no máximo as **2 últimas atualizações** no arquivo; apague as antigas.

## 5. Publicar e conferir

1. Edite o `.md` e faça commit/push na branch `main`.
2. O GitHub pode levar **até ~5 minutos** para servir a versão nova (cache do CDN).
3. O launcher carrega as notícias **ao abrir**. Feche e abra o launcher para ver.

### Checklist antes do push
- [ ] Arquivo está na raiz (ou em `launcher_content/`)
- [ ] Nome está no `textshow` de **ambos** os configs
- [ ] Listas usam `- `
- [ ] Nenhum `---` no meio do texto
- [ ] Se editou algum `launcher_config*.json`, o JSON é válido
  (uma vírgula faltando quebra o painel, o carrossel e os links de uma vez;
  valide em https://jsonlint.com)

## 6. Descrição da atualização (notificação do Windows)

O campo `description` de cada config aparece na **notificação do Windows**
quando sai uma versão nova do cliente. Escreva uma frase curta:

```json
"description": "Novo sistema de forja e correções no Battle Pass"
```
