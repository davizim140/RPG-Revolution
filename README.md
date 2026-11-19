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
- Despertares raros (3% por classe) ao escolher uma classe pela primeira vez: Assassino/Monarca das Sombras, Guerreiro/Colosso, Mago/Arquimago e Arqueiro/Olho Celestial, cada um com passiva e habilidade exclusiva. O Monarca invoca três soldados temporários por 45 segundos e pode extrair até cinco sombras permanentes, que evoluem individualmente até o nível 10. O Monarca pode alternar posturas agressiva, defensiva ou passiva com /posturasombras e reunir todos os soldados com /reunirsombras.
- Armas e armaduras exclusivas por classe, com bônus de conjunto.
- Espada do Aprendiz e Couraça do Guardião aprimoráveis até +3.
- Loja, receitas, itens nomeados e raridades visuais.
- Missão inicial, linha de história e contrato diário de caça.
- Grupos de jogadores com convites, liderança e compartilhamento de XP/moedas por abates próximos.
- Regiões configuráveis por mundo, com bloqueio de teleporte entre mundos para personagens abaixo do nível mínimo.
- Masmorra individual básica e expedição avançada de três etapas (duas ondas e chefe), com limpeza ao cancelar ou desconectar.
- Chefe mundial de três fases, com servos, participação e recompensas.
- Mercado entre jogadores com anúncios em custódia, compra e cancelamento.
- Progressão de guildas por caça, níveis e depósito automático no banco.
- Guerras de guildas por desafio/aceite, placar PvP e prêmio ao vencedor.
- Estatísticas PvP individuais, recompensas por vitória e marcos de 10/50 eliminações.
- Guildas com convite, hierarquia de líder/oficial/membro, transferência de liderança, chat e banco.
- Territórios de guilda: reivindicação de áreas 33x33 por 500 moedas do banco, limite de três por guilda e proteção contra construção/interação de não membros, explosões, pistões posicionados dentro da área e blocos movidos por pistões que alcançam a área ou sua margem imediata; fogo iniciado ou propagado dentro dela e fluxo de água/lava na área e na margem externa imediata. Durante guerras ativas, abates PvP dentro do território permitem captura: cinco pontos transferem a área e concedem 250 moedas ao banco atacante; abates defensivos reduzem o progresso.
- Captura territorial integrada às guerras de guilda, com consulta por /guildterritorioguerra (ou /gtg).
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
- /classe, /habilidades, /habilidade, /especializar, /despertar, /sombra, /invocar, /sombras, /exercito, /libertar, /posturasombras, /reunirsombras, /furia, /arcano, /precisao
- /saldo, /pagar
- /missoes, /resgatar, /recompensadiaria, /contrato
- /npc, /rpgnpc criar, /rpgnpc limpar, /missaoaceitar, /minhasmissoes, /missaoentregar
- /rpgloja, /comprar, /mercado [listar|vender|comprar|cancelar], /rpgcraft, /fabricar
- /fabricarclasse, /fabricararmadura, /equipamento, /aprimorar
- /grupo, /grupocriar, /grupoconvidar, /grupoaceitar, /gruposair, /grupochutar
- /masmorra [cancelar], /expedicao [cancelar], /chefemundial (admin)
- /guilda, /guildacriar, /guildaconvidar, /guildaaceitar, /guildasair, /guildainfo
- /guildatransferir, /guildaexpulsar, /guildchat, /guildabanco, /guildasaldo, /guildacargo, /guildacargos, /guildterritorio, /guildterritorioguerra, /guildanivel, /guildaguerra, /pvpstatus
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
- /masmorra continua sendo o encontro individual simples. /expedicao adiciona duas ondas e um chefe vanilla, mas ainda não cria arena instanciada nem salas construídas automaticamente.
- Grupos compartilham recompensas com integrantes online no mesmo mundo e a até 16 blocos do jogador que derrotou a criatura.
- Cargos de guilda têm líder, oficial e membro. Oficiais podem convidar e expulsar membros comuns; somente o líder pode promover/rebaixar oficiais, expulsar oficiais, transferir liderança e sacar do banco. Territórios podem ser reivindicados e abandonados pelo líder. Durante uma guerra ativa, cinco abates válidos de membros defensores dentro do território transferem a área para a guilda atacante e concedem 250 moedas ao banco; abates defensivos reduzem o progresso. A captura exige espaço no limite de três territórios. A proteção contra explosões remove os blocos protegidos da lista de destruição, sem impedir dano a entidades. Pistões são bloqueados quando estão posicionados dentro do território; eventos de extensão/retração também verificam os blocos movidos e uma margem de um bloco. A geometria completa de mecanismos externos ainda precisa de validação em Paper real. Os eventos de início e propagação de fogo são cancelados dentro do território. Fluxos de água/lava são cancelados quando a origem está dentro da área ou na margem de um bloco ao redor; isso evita a entrada imediata pela borda, mas não é uma barreira física para líquidos que já tenham atravessado antes da atualização. Mecanismos externos ainda não estão protegidos. Ainda não há impostos nem arenas isoladas.
- Cada classe tem 3% de chance de despertar no momento da primeira escolha; não há novo sorteio para personagens que já escolheram classe. Os despertares são permanentes. O Monarca pode invocar três soldados temporários com /invocar e consultar com /sombras. Ao derrotar monstros diretamente, há 15% de chance de extrair uma sombra permanente, com limite de cinco; /exercito lista as sombras, /sombranivel <1-5> consulta o nível e XP, e /libertar <1-5> libera um espaço. Cada sombra permanente ganha XP ao derrotar monstros e evolui a cada cinco XP por nível, até o nível 10. /posturasombras agressiva|defensiva|passiva controla a seleção automática de alvos: agressiva reage a ataques do Monarca e contra ele; defensiva só protege o Monarca; passiva não escolhe alvos automaticamente. /reunirsombras teleporta os soldados vivos para perto do Monarca. As sombras permanentes são representadas por esqueletos Wither e podem ser destruídas por inimigos. O rank dos soldados temporários evolui com o nível do Monarca: C (1+), B (10+), A (25+) e S (50+), aumentando seus efeitos de combate.
- O mercado mantém itens anunciados em custódia nas variáveis do Skript; não possui taxa, interface gráfica ou histórico de transações.
- O chefe mundial e as expedições usam criaturas vanilla e dependem de espaço livre no local onde são iniciados.
- Guerras de guilda usam um placar global e não isolam PvP por região; a administração deve combinar regras de arena e duração. As recompensas PvP ainda precisam de proteção contra combinação de mortes entre contas.
- A HUD usa a action bar e pode sobrescrever mensagens de action bar enviadas por outros plugins. Os eventos mundiais são iniciados manualmente.

## Validação
O GitHub Actions verifica estrutura, ausência de marcadores de placeholder e empacota ZIP. Isso não comprova sintaxe Skript nem execução em Paper 26.3. Teste /sk reload all e todos os sistemas em servidor de homologação antes de produção.
