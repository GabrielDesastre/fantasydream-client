# 📁 Launcher Content Files

Esta pasta contém os arquivos de conteúdo que são exibidos no launcher.

## 🎯 Como Funciona

O launcher busca automaticamente estes arquivos do GitHub e exibe o conteúdo nas respectivas seções. Isso permite atualizar o conteúdo sem precisar recompilar o launcher!

## 📝 Arquivos Necessários

Crie um arquivo para cada seção do launcher:

- `patch_news.md` - Patch Notes / Atualizações
- `auto_loot.md` - Sistema de Auto Loot
- `proficiency.md` - Sistema de Proficiência
- `task_system.md` - Sistema de Tarefas
- `battle_pass.md` - Battle Pass
- `master_forge.md` - Master Forge
- `eventos.md` - Eventos
- `destaques.md` - Destaques

## 📍 Onde Colocar

Você pode colocar os arquivos em dois lugares no seu repositório GitHub:

1. **Pasta `launcher_content/`** (recomendado)
   ```
   seu-repositorio/
   ├── launcher_content/
   │   ├── patch_news.md
   │   ├── auto_loot.md
   │   └── ...
   ```

2. **Raiz do repositório** (alternativa)
   ```
   seu-repositorio/
   ├── patch_news.md
   ├── auto_loot.md
   └── ...
   ```

## ✍️ Formato dos Arquivos

### Markdown (.md) - Recomendado

```markdown
# Título Principal

## Subtítulo

- Item de lista 1
- Item de lista 2

**Texto em negrito** será convertido para MAIÚSCULAS

### Seção

Texto normal aqui...
```

### Texto Simples (.txt)

```
Título Principal

• Item 1
• Item 2

Texto normal...
```

## 🔄 Conversão Automática

O launcher converte automaticamente:
- `##` → Remove (títulos)
- `**texto**` → TEXTO (negrito para maiúsculas)
- `- item` → `• item` (listas)
- `* item` → `• item` (listas)

## 🚀 Vantagens

✅ Atualizar conteúdo sem recompilar o launcher
✅ Editar diretamente no GitHub
✅ Histórico de mudanças (Git)
✅ Fácil colaboração
✅ Fallback automático para conteúdo local

## 📌 Exemplo de Uso

1. Crie o arquivo `patch_news.md` no GitHub
2. Faça commit
3. O launcher baixa automaticamente na próxima vez que o usuário abrir
4. Se o GitHub estiver indisponível, usa o conteúdo local padrão

## 🔧 Configuração

O launcher está configurado para buscar do repositório:
- **Owner**: GabrielDesastre
- **Repo**: fantasydream-client
- **Branch**: main

Para mudar, edite `github_downloader.py`:
```python
self.repo_owner = "seu-usuario"
self.repo_name = "seu-repositorio"
```
