# RPG Revolution

RPG de mundo aberto para Minecraft Java **26.3**, com lógica de jogo em Skript puro.

## Stack
- Minecraft Java 26.3 como versão-base pretendida.
- Paper 26.3 como servidor recomendado.
- Skript em versão explicitamente compatível com a versão-base.
- ViaVersion para compatibilidade de clientes, dentro da matriz suportada pelo ViaVersion.
- Nenhum addon de Skript.

ViaVersion não altera a versão-base do servidor nem garante compatibilidade universal.

## Sistemas incluídos nesta fundação
- Criação automática de personagem.
- Perfil, níveis e XP.
- XP e moedas por derrotar criaturas.
- Dois pontos de atributo por nível.
- Força, defesa, agilidade e inteligência.
- Bônus de dano de força.
- Economia e transferências entre jogadores.
- Missão inicial de caça.
- Quatro classes permanentes: Guerreiro, Mago, Assassino e Arqueiro.
- Uma habilidade ativa inicial por classe, com custo de mana e recarga.
- Regeneração automática de mana.
- Especializações desbloqueadas no nível 20:
  - Guerreiro: Guardião ou Berserker.
  - Mago: Elementalista ou Arcanista.
  - Assassino: Sombra ou Duelista.
  - Arqueiro: Francoatirador ou Caçador.

## Instalação
1. Faça backup do servidor.
2. Instale Paper 26.3 e uma versão do Skript compatível com ela.
3. Instale ViaVersion se quiser aceitar clientes de outras versões.
4. Copie `server/plugins/Skript/scripts/` para `plugins/Skript/scripts/` no servidor.
5. Execute `/sk reload all` e confira o console.
6. Não use em produção até validar o carregamento e os eventos no servidor.

Permissão administrativa: `rpg.admin`.

## Comandos
- `/rpgajuda`
- `/perfil`
- `/atributos`
- `/upar <forca|defesa|agilidade|inteligencia>`
- `/classe` e `/classe <guerreiro|mago|assassino|arqueiro>`
- `/habilidades` e `/habilidade`
- `/especializar` e `/especializar <especializacao>` (nível 20+)
- `/saldo`
- `/pagar <jogador> <valor>`
- `/missoes`
- `/resgatar`
- `/rpgxp <jogador> <quantidade>` (admin)
- `/rpgmoedas <jogador> <saldo>` (admin)

## Validação
O workflow verifica estrutura, presença dos arquivos e empacota a distribuição. Isso não substitui teste de carregamento e jogabilidade em Paper 26.3. A compatibilidade final depende das versões publicadas do Paper, Skript e ViaVersion disponíveis no momento da instalação. Habilidades e balanceamento ainda precisam ser testados em servidor.
