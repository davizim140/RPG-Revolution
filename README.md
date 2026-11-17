# RPG Revolution

RPG de mundo aberto para Minecraft Java **26.3**, com lógica de jogo em Skript puro.

## Stack
- Minecraft Java 26.3 como versão-base pretendida.
- Paper 26.3 como servidor recomendado.
- Skript em versão explicitamente compatível com a versão-base.
- ViaVersion para compatibilidade de clientes, dentro da matriz suportada pelo ViaVersion.
- Nenhum addon de Skript.

ViaVersion é um plugin separado: não altera a versão-base do servidor nem garante compatibilidade universal.

## Sistemas incluídos
- Personagens, níveis, XP, atributos, economia e missão inicial.
- Quatro classes, mana, habilidades e especializações.
- Regiões informativas por mundo.
- Loja de equipamentos básicos.
- Receitas próprias para espada incomum, couraça épica e arco épico.
- Bônus de dano da espada especial e redução de dano da couraça especial.
- Aprimoramento de espada e couraça até +3, consumindo diamantes e moedas.
- Chefe de masmorra repetível.
- Guildas com criação e convites.
- Recompensa diária.
- Três personagens de história por diálogos via comandos.
- Linha de missões: recolher 8 troncos de carvalho e derrotar 5 zumbis, com progresso salvo e recompensas.

## Instalação
1. Faça backup do servidor.
2. Instale Paper 26.3 e uma versão do Skript compatível com ela.
3. Instale ViaVersion se quiser aceitar clientes de outras versões.
4. Copie a pasta server/plugins/Skript/scripts/ para plugins/Skript/scripts/ no servidor.
5. Execute /sk reload all e confira o console.
6. Teste em um servidor separado antes de usar em produção.

## Comandos principais
- /rpgajuda, /perfil, /atributos, /upar <forca|defesa|agilidade|inteligencia>
- /classe, /habilidades, /habilidade, /especializar
- /saldo, /pagar <jogador> <valor>
- /missoes, /resgatar, /recompensadiaria
- /npc <guia|ferreiro|explorador>
- /missaoaceitar <madeira|zumbis>, /minhasmissoes, /missaoentregar
- /rpgloja, /comprar <espada|armadura|arco|comida>
- /rpgcraft, /fabricar <espada|armadura|arco>
- /equipamento, /aprimorar (segure a espada ou couraça especial)
- /masmorra
- /guilda, /guildacriar <nome>, /guildaconvidar <jogador>, /guildaaceitar, /guildainfo, /guildasair
- /regiao, /rpgmundos, /rpgregiao definir <nome> <nivel-minimo>
- /rpgxp <jogador> <quantidade> e /rpgmoedas <jogador> <saldo>

Permissão administrativa: rpg.admin.

## Limites conhecidos
- A identificação dos equipamentos especiais usa o nome do item; renomeá-los em bigorna pode afetar o reconhecimento. Ainda não há identificador persistente próprio nem atributos NBT/PDC.
- O bônus especial de combate é aplicado à espada fabricada; o arco mantém dano vanilla.
- Os NPCs são personagens de diálogo acionados por comando, não entidades com skin ou interação física.
- Regiões exibem nível recomendado, mas ainda não bloqueiam entrada por nível.
- Loja entrega itens vanilla nomeados; não há atributos extras.
- O chefe é um zumbi vanilla com vida aumentada; não há arena instanciada nem mecânicas especiais.
- Guildas ainda não têm transferência de liderança, chat próprio, banco ou guerras.
- HUD customizada, eventos mundiais e grupos de dungeon ainda não estão implementados.

## Validação
O GitHub Actions verifica a estrutura, procura marcadores de placeholder e empacota a distribuição. Isso **não valida a sintaxe do Skript nem substitui o teste real** de carregamento e jogabilidade em Paper 26.3. Antes de produção, teste /sk reload all e os comandos em um servidor de homologação.
