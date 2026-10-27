# 📰 FantasyClient - Últimas Atualizações

## Versão 1.0.16 - 26/10/2026

### ✨ Novidades
- **Análise de hardware**: o cliente detecta placa de vídeo, memória de vídeo e RAM ao abrir, e o **Performance Mode** já vem no nível certo para o seu PC
- **Tela de login**: aviso com o motivo e botão **Apply recommended** quando o seu PC é mais fraco que o modo escolhido
- **Vulkan**: placas NVIDIA/AMD recentes (4 GB+ de vídeo) recebem a sugestão de trocar do DirectX 11 para o Vulkan, com reinício do cliente
- **Graphics Engine**: cada motor gráfico agora tem um tooltip explicando para que ele é melhor

### 🔧 Correções
- **Placas antigas / pouca memória de vídeo** (ex.: GTX 750 Ti): o jogo fechava com "Unable to create hardware buffer". O cache de textura do mapa agora se adapta à placa, e se o driver reiniciar o cliente abre em modo seguro na próxima vez

## Versão 1.0.15 - 26/10/2026

### ✨ Novidades
- **Assistant**: janela maior (mais larga e mais alta). As listas de Timers, Shooter, Amulets, Rings, Healing e Group usam toda a largura, e os editores ganharam caixas de nome maiores e campos alinhados

### 🔧 Correções
- **Cyclopedia e Market**: 54 itens que não apareciam agora aparecem, incluindo todas as armas de Monk (nova categoria **Fist Weapons**) e itens sem categoria (Unsorted / Others)
- **Cyclopedia**: Offence/Defence sem erro, percentual de level correto, inspeção de item equipado e troca de título funcionando, mensagens de erro da House corretas, Magical Archive sem tudo bloqueado
- Atalho **Show/hide bestiary tracker** abre o tracker de verdade

## Versão 1.0.14 - 25/10/2026

### ✨ Novidades
- **Assistant - Scripts**: botão **Edit** abre o script selecionado no editor integrado e recarrega se estiver rodando
- **Monk**: o Harmony (0 a 5) aparece em cinco marcadores abaixo da barra de mana
- **Opções**: "Mark target visually" e "Effects Limits" agora funcionam
- Textos de HUD dos scripts em negrito com contorno preto, bem mais fáceis de ler

### 🔧 Correções
- **Bless**: o brilho do inventário e o botão de bless só aparecem com 5+ blessings confirmadas pelo servidor
- **Opções > HUD**: desligar HUD, nome, vida e mana agora esconde de verdade; ícones de NPC e marcas de outras criaturas também
- **Game Window**: "Show Messages" e "Show Textual Effects" escondem textos e números de dano/cura

## Versão 1.0.13 - 23/10/2026

### ✨ Novidades
- **Assistant - Scripts (beta)**: rode scripts Lua feitos para o ZeroBot (inclusive GozzimHUD) e crie scripts pelo botão **New script**
- **Cave Bot**: `wait()` nos waypoints Action e novos waypoints Ladder, Teleport, Machete e "Go to label"

### 🔧 Correções
- Assistant mais leve: cura, shooter, ataque, timers e cave bot dividem um único ciclo
- Cave Bot: o waypoint Stand espera o ponto estar alcançável; walk delay e lure passam a valer ao dar play
- A aba Scripts voltou a carregar os scripts

## Versão 1.0.12 - 22/10/2026

### ✨ Novidades
- **Opções > Misc**: nova opção **Interface Font** para escolher a fonte da interface
- **Minimapa**: a rota do cave bot ficou azul claro, com linha mais grossa

### 🔧 Correções
- Report de bugs envia tipo, texto e posição corretos
- Modal windows do servidor: tamanho, ícones, imagens e botões longos corrigidos
- Assistant: "Increase dust capacity" e "Convert dust to sliver" voltaram a funcionar
- Podium: janela "Customise Podium" corrigida

## Versão 1.0.11 - 20/10/2026

### ✨ Novidades
- **Assistant**: clique direito numa regra abre Duplicar, Mover para o topo/fim, Ativar/Desativar e Excluir; Shift + seta leva a regra ao topo ou ao fim
- **Presets**: exportar/importar por arquivo e "Resetar para o inicial"
- **Cave Bot**: a rota aparece no minimapa, com o waypoint atual destacado
- Modal windows do servidor mostram cores, quebras de linha e imagens

### 🔧 Correções
- O botão de subir regra voltou a aparecer no Shooter e nos Timers, e a lista não volta mais ao início ao editar
- O Shooter respeita a prioridade: a regra de cima é usada primeiro
- **Minimapa**: a área explorada não é mais perdida ao fechar o cliente
- Podium e Livestream (cast) corrigidos
- Menos lag com vários clientes abertos

## Versão 1.0.9 e 1.0.10 - 19/10/2026

### 🔧 Correções
- Assets do jogo atualizados: novos sprites e aparências (itens, criaturas e outfits)

## Versão 1.0.8 - 16/10/2026

### ✨ Novidades
- **Opções > Misc**: botões **Export Session Log** e **Open Config Folder**, para enviar o log ao suporte
- **Smart follow**: novas opções **Follow distance** e **Style** (Normal, Behind, Front, Left, Right, Wave); acompanha quem usa escada, corda e buraco e abre portas do caminho
- **Assistant - Support**: a lista agora tem barra de rolagem

### 🔧 Correções
- Corrigido o bug em que monstros apareciam clonados e sem nome depois de certas magias em área (como a Divine Grenade)
- Utito Tempo San (Sharpshooter) aparecia sem imagem na barra de ação do Paladin
- O Smart follow contorna monstros, summons e paredes
- Menos lag com o auto equip de ring/necklace e com o auto exercise

## Versão 1.0.7 - 06/10/2026

### ✨ Novidades
- **Assistant - Loot seller**: nova opção em Support > General que usa o **Loot Pouch Seller** automaticamente (a cada ~30 segundos) enquanto você o carrega, vendendo a sua Loot Pouch sem precisar clicar

### 🔧 Correções
- **Store Inbox**: o pontinho branco agora aparece só nos deco kits, e não mais em todos os itens
- **Chat**: Enter com o chat desligado liga o chat e já deixa o campo de texto pronto para digitar, sem precisar clicar nele
- Muito mais FPS em hunts pesadas (ex.: Inferniarch): andares de baixo já escondidos pelo chão não são mais desenhados
- Menos travadas ao lootear: abrir e atualizar backpacks e a loot pouch não congela mais o jogo

## Versão 1.0.6 - 05/10/2026

### 🔧 Correções
- Menos queda de FPS em áreas com muita coisa na tela, como hunts com muitos monstros e itens
- Menos queda de FPS ao vender muitos itens no NPC (ex.: loot da loot pouch)

## Versão 1.0.5 - 04/10/2026

### ✨ Novidades
- **Minimapa - Ping**: clique direito no minimapa ou no mapa e escolha **Ping...** para marcar um local para a party ou a guild (Perigo, A caminho, Ajuda, Aqui)
- **Minimapa**: membros da party e da guild aparecem no minimapa com a cor da vocação
- **Títulos**: God, GM e Tutor aparecem com título colorido sobre o nome, e os NPCs mostram o que fazem (Merchant, Banker, Boat Captain...)
- **Assistant - Pull ranged**: nova página que usa Chivalrous Challenge, Divine Dazzle ou Balanced Brawl para puxar monstros de longa distância
- **Assistant - Smart follow**: novo atalho que segue o alvo por escadas, buracos e fire fields, e vai até onde ele foi visto por último

### 🔧 Correções
- **Skills**: ao acabar o boost de XP da loja, a taxa voltava a mostrar o valor com boost (225% em vez de 175%)
- Janelas de diálogo do servidor (ex.: Maestria): tags `<b>` soltas removidas
- Painéis laterais travados não ficam mais com borda vermelha
- Menos queda de FPS em lutas com muitos monstros

## Versão 1.0.4 - 01/10/2026

### ✨ Novidades
- **Assistant - Shooter**: novo preview da área da spell/runa, desenhado tile por tile (piso, seu personagem e o alvo, virados para o sul)
- **Janelas de diálogo** (Spell Mastery Upgrader, Forge): visual do Tibia original e altura ajustável arrastando a borda de baixo

### 🔧 Correções
- **Atualização**: o pacote agora leva o executável junto. Na versão 1.0.3 o launcher apagava o FantasyClient.exe ao atualizar
- **Assistant**: ao trocar de regra, o campo da spell/item agora mostra a da regra selecionada, e o **Apply** não troca mais a spell/item sozinho (Healing, Shooter, Timers e Equipment)
- **Assistant**: área corrigida em várias spells (Fire Wave, Scorch, Energy Wave, Energy Beam, Hell's Core, Rage of the Skies, Divine Caldera, Front Sweep, Ice Wave, Terra Wave e outras)
- Janelas de diálogo com imagem: símbolos "/>" soltos removidos

## Versão 1.0.2 - 29/09/2026

### ✨ Novidades
- **Assistant - Mana Shield**: nova opção **Force use when monsters >=** na spell e na Magic Shield Potion. Usa o escudo quando houver a quantidade de monstros escolhida na tela, independente do HP
- **Assistant - Mana Shield**: **Ignore when feared** e **Hold until monsters <=** na remoção do escudo (exana vita)

### 🔧 Correções
- utamo vita e exana vita não são mais enviados várias vezes seguidas
- Renew do escudo dispara abaixo do percentual escolhido
- Página Mana Shield do Assistant agora tem barra de rolagem

## Versão 1.0.1 - 28/09/2026

### ✨ Novidades
- **HD Textures**: nova opção em Options > Graphics que amplia os sprites do mapa em 2x com filtro xBRZ
- **Bloco principal fixo**: Vida/Mana, Minimapa, Inventário e Botões de controle agrupados no topo do painel lateral, reordenáveis
- **Battle List**: clique direito abre o mesmo menu do mapa (atacar, seguir, party, inspecionar, reportar)
- **Cyclopedia (Mapa)**: novo botão para centralizar o mapa no seu personagem
- Barras horizontais do topo redimensionáveis, com altura salva por personagem

### 🔧 Correções
- Cyclopedia (Mapa): "Show All" não trava mais o cliente e a cruz de posição não some ao arrastar o mapa
- Mapa: pisos removidos pelo servidor não reaparecem mais do cache local
- Battle List: mostra só as criaturas na sua tela, filtros restaurados corretamente ao logar
- Assistant: Enhanced Ultimate Healing Rune e poções Enhanced não trocam mais para a versão comum ao aplicar
- Minimapa: tooltip, "Delete mark" e shift+clique voltaram a funcionar nas marcações

**Dúvidas? Chame no Discord!**
