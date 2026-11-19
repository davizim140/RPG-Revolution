# RPG Revolution

RPG de mundo aberto para Minecraft Java 26.3, com sistemas implementados em Skript puro.

## Stack
- Minecraft Java 26.3 como versão-base pretendida.
- Paper 26.3 como servidor recomendado.
- Skript em versão explicitamente compatível com a versão-base.
- ViaVersion como plugin separado para clientes de outras versões, dentro da matriz suportada.
- Nenhum addon de Skript.

## Sistemas implementados
- Personagens, níveis, XP, atributos, economia e progressão.
- Quatro classes, habilidades, mana e especializações.
- Despertares raros (3% por classe) ao escolher uma classe pela primeira vez: Assassino/Monarca das Sombras, Guerreiro/Colosso, Mago/Arquimago e Arqueiro/Olho Celestial, cada um com passiva e habilidade exclusiva. O Monarca invoca três soldados temporários por 45 segundos e pode extrair até cinco sombras permanentes, que evoluem individualmente até o nível 10.
- Armas e armaduras exclusivas por classe, com bônus de conjunto.
- Espada do Aprendiz e Couraça do Guardião aprimoráveis até +3.
- Loja, receitas, itens nomeados e raridades visuais.
- Missão inicial, linha de história e contrato diário de caça.
- Grupos de jogadores com convites, liderança e compartilhamento de XP/moedas por abates próximos.
- Regiões configuráveis por mundo, com bloqueio de teleporte entre mundos para personagens abaixo do nível mínimo.
- Masmorra com chefe.
- Guildas com convite, transferência de liderança, expulsão, chat e banco.
- Recompensas diárias.
- Evento manual de invasão mundial: cinco invasores, participação registrada e recompensa coletiva.
- HUD leve na action bar com nível, XP, vida e mana; ativação individual por /rpghud on|off.

## Instalação
1. Faça backup do servidor.
2. Instale Paper 26.3 e uma versão do Skript compatível com ela.
3. Opcionalmente instale ViaVersion.
4. Copie server/plugins/Skript/scripts/ para plugins/Skript/scripts/.
5. Execute /sk reload all e examine o console.
6. Teste em servidor separado antes de produção.

## Comandos principais
- /rpgajuda, /perfil, /atributos, /upar
- /classe, /habilidades, /habilidade, /especializar, /despertar, /sombra, /invocar, /sombras, /exercito, /libertar, /furia, /arcano, /precisao
- /saldo, /pagar
- /missoes, /resgatar, /recompensadiaria, /contrato
- /npc, /rpgnpc criar, /rpgnpc limpar, /missaoaceitar, /minhasmissoes, /missaoentregar
- /rpgloja, /comprar, /rpgcraft, /fabricar
- /fabricarclasse, /fabricararmadura, /equipamento, /aprimorar
- /grupo, /grupocriar, /grupoconvidar, /grupoaceitar, /gruposair, /grupochutar
- /masmorra [cancelar]
- /guilda, /guildacriar, /guildaconvidar, /guildaaceitar, /guildasair, /guildainfo
- /guildatransferir, /guildaexpulsar, /guildchat, /guildabanco, /guildasaldo
- /regiao, /rpgmundos, /rpgregiao definir, /rpgregiao remover
- /rpghud [on|off]
- /invasao iniciar|encerrar (permissão rpg.admin)
- /rpgxp, /rpgmoedas

Permissão administrativa: rpg.admin.

## Limitações conhecidas
- Itens especiais são identificados pelo nome; bigorna ou renomeação pode afetar os bônus. Ainda não há identificador persistente NBT/PDC.
- Raridades são visuais, exceto bônus programados nos itens descritos.
- O bônus do Arco do Batedor precisa de validação em combate real com flechas.
- Armaduras de classe são identificadas pelo nome; conjunto Guerreiro reduz dano, Mago e Assassino aumentam dano corpo a corpo, Arqueiro recebe velocidade.
- NPCs físicos usam aldeões vanilla e abrem os diálogos existentes ao clicar; não têm skin personalizada.
- A proteção de regiões é aplicada a teletransportes entre mundos; movimentação/entrada por outros mecanismos precisa de validação no servidor real.
- A masmorra continua sendo um encontro individual simples com criatura vanilla; agora permite cancelamento e limpa o chefe ao desconectar. Não há arena instanciada ou mecânicas complexas.
- Grupos compartilham recompensas com integrantes online no mesmo mundo e a até 16 blocos do jogador que derrotou a criatura.
- Guildas ainda não têm guerras, cargos ou níveis.
- Cada classe tem 3% de chance de despertar no momento da primeira escolha; não há novo sorteio para personagens que já escolheram classe. Os despertares são permanentes. O Monarca pode invocar três soldados temporários com /invocar e consultar com /sombras. Ao derrotar monstros diretamente, há 15% de chance de extrair uma sombra permanente, com limite de cinco; /exercito lista as sombras, /sombranivel <1-5> consulta o nível e XP, e /libertar <1-5> libera um espaço. Cada sombra permanente ganha XP ao derrotar monstros e evolui a cada cinco XP por nível, até o nível 10. As sombras permanentes são representadas por esqueletos Wither e podem ser destruídas por inimigos. O rank dos soldados temporários evolui com o nível do Monarca: C (1+), B (10+), A (25+) e S (50+), aumentando seus efeitos de combate.
- A HUD usa a action bar e pode sobrescrever mensagens de action bar enviadas por outros plugins. Os eventos mundiais são iniciados manualmente.

## Validação
O GitHub Actions verifica estrutura, ausência de marcadores de placeholder e empacota ZIP. Isso não comprova sintaxe Skript nem execução em Paper 26.3. Teste /sk reload all e todos os sistemas em servidor de homologação antes de produção.
