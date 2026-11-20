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
- Espada do Aprendiz e Couraça do Guardião aprimoráveis até +3. Três armas lendárias forjáveis (Lâmina Solar, Machado do Colosso e Arco da Tempestade) evoluem por abates até maestria 5, possuem habilidades ativas próprias e podem receber até três níveis de evolução permanente por jogador.
- Loja, receitas, itens nomeados e raridades visuais.
- Missão inicial, linha de história e contrato diário de caça.
- Grupos de jogadores com convites, liderança e compartilhamento de XP/moedas por abates próximos.
- Regiões configuráveis por mundo, com bloqueio de teleporte entre mundos para personagens abaixo do nível mínimo.
- Masmorra individual básica, expedição avançada em três dificuldades (Normal 10+, Heroica 20+, Pesadelo 35+) e expedições cooperativas integradas aos grupos e raids de chefes com dificuldade e recompensa proporcional ao dano contribuído. A Arena das Ruínas (/arenadungeon) adiciona três salas de combate com sentinelas, aranhas armadilhadas e o chefe Guardião Arcano, tesouros intermediários e recompensa final; o encontro usa a área atual sem alterar blocos do mundo.
- Chefe mundial de três fases, com servos, participação e recompensas. Chefes lendários invocáveis: Guardião Primordial, Lich Eterno e Draco Celestial, cada um com 400/300/350 de vida, duas transições de fase, reforços e relíquia exclusiva. Arenas cooperativas de raid em três etapas configuráveis, com ondas de inimigos, Titã final e baús de recompensa por sala.
- Mercado entre jogadores com anúncios em custódia, compra e cancelamento.
- Progressão de guildas por caça, níveis e depósito automático no banco.
- Guerras de guildas por desafio/aceite, placar PvP e prêmio ao vencedor.
- Estatísticas PvP individuais, recompensas por vitória e marcos de 10/50 eliminações.
- Guildas com convite, hierarquia de líder/oficial/membro, transferência de liderança, chat e banco.
- Territórios de guilda: reivindicação de áreas 33x33 por 500 moedas do banco, limite de três por guilda e proteção contra construção/interação de não membros, explosões, pistões posicionados dentro da área e blocos movidos por pistões que alcançam a área; fogo iniciado ou propagado dentro dela e fluxo de água/lava na área e na margem externa imediata, além de bloqueio de dispensers/droppers instalados dentro do território, cancelamento de transferências automáticas de itens por funis quando a origem ou o destino está dentro da área e bloqueio da coleta de itens do chão por funis e carrinhos com funil no território e proteção de inventários de entidades, incluindo carrinhos com baú, ao serem abertos, além de bloqueio de dano e destruição de veículos com inventário e proteção dos itens dropados contra coleta por jogadores de outras guildas e contra dano ambiental de fogo, lava e explosões e contra movimento de saída pela fronteira e transporte por portais. Durante guerras ativas, abates PvP dentro do território permitem captura: cinco pontos transferem a área e concedem 250 moedas ao banco atacante; abates defensivos reduzem o progresso.
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
- /rpgitenslimpar [CONFIRMAR] (admin): limpeza manual de todos os itens dropados no território atual; exige confirmação e remove também itens legítimos.

- /rpgajuda, /perfil, /atributos, /upar
- /classe, /habilidades, /habilidade, /especializar, /despertar, /sombra, /invocar, /sombras, /exercito, /libertar, /posturasombras, /reunirsombras, /furia, /arcano, /precisao
- /saldo, /pagar
- /missoes, /resgatar, /recompensadiaria, /contrato
- /npc, /rpgnpc criar, /rpgnpc limpar, /missaoaceitar, /minhasmissoes, /missaoentregar
- /rpgloja, /comprar, /mercado [listar|vender|comprar|cancelar], /rpgcraft, /fabricar
- /fabricarclasse, /fabricararmadura, /evoluirarmadura, /evolucaoarmadura, /guardialendaria, /equipamento, /aprimorar, /forjarlendaria <espada|machado|arco>, /poderarma, /maestriaarma, /melhorararma <espada|machado|arco>, /evolucaoarma
- /grupo, /grupocriar, /grupoconvidar, /grupoaceitar, /gruposair, /grupochutar
- /masmorra [cancelar], /expedicao [normal|heroica|pesadelo|cancelar], /expedicaogrupo [normal|heroica|pesadelo|cancelar], /arenadungeon iniciar|status|cancelar, /chefemundial (admin), /invocarchefe guardiao|lich|draco, /chefeslendarios encerrar (admin), /raidchefe normal|heroica|pesadelo|status|cancelar, /raidarena configurar 1|2|3 (admin) ou normal|heroica|pesadelo|status|cancelar, /raidbau abrir|status
- /guilda, /guildacriar, /guildaconvidar, /guildaaceitar, /guildasair, /guildainfo
- /guildatransferir, /guildaexpulsar, /guildchat, /guildabanco, /guildasaldo, /guildacargo, /guildacargos, /guildterritorio, /guildterritorioguerra, /guildanivel, /guildaguerra, /pvpstatus
- /regiao, /rpgmundos, /rpgregiao definir, /rpgregiao remover
- /rpghud [on|off]
- /invasao iniciar|encerrar (permissão rpg.admin)
- /rpgxp, /rpgmoedas

Permissão administrativa: rpg.admin.

## Limitações conhecidas
- As raids de chefe usam o grupo existente, exigem pelo menos dois membros online no mesmo mundo e a até 24 blocos, e têm níveis mínimos 10/20/35. O Colosso da Raid recebe 250/500/800 de vida; recompensas-base de 500/1.000/1.800 moedas, 300/600/1.000 XP e 2/4/7 diamantes são distribuídas proporcionalmente ao dano registrado, com um sorteio de item de chefe para cada participante que causou dano. O placar é consultado por /raidchefe status. Encontro usa um ravager vanilla; ainda requer teste em Paper real.
- Chefes lendários permitem apenas um encontro global por vez. Invocação custa 8 diamantes, 1 estrela do Nether e 1.000 moedas; participantes registrados recebem 750 moedas, 500 XP e uma relíquia específica ao vencer. Os encontros usam mobs vanilla e ainda precisam de validação de sintaxe, balanceamento e runtime em Paper real.
- Itens especiais são identificados pelo nome; bigorna ou renomeação pode afetar os bônus. Ainda não há identificador persistente NBT/PDC.
- Raridades são visuais, exceto bônus programados nos itens descritos.
- O bônus do Arco do Batedor precisa de validação em combate real com flechas.
- Armaduras de classe são identificadas pelo nome; conjunto Guerreiro reduz dano, Mago e Assassino aumentam dano corpo a corpo, Arqueiro recebe velocidade.
- NPCs físicos usam aldeões vanilla e abrem os diálogos existentes ao clicar; não têm skin personalizada.
- A proteção de regiões é aplicada a teletransportes entre mundos; movimentação/entrada por outros mecanismos precisa de validação no servidor real.
- /masmorra continua sendo o encontro individual simples. /expedicao adiciona duas ondas e um chefe vanilla, mas ainda não cria arena instanciada nem salas construídas automaticamente.
- Grupos compartilham recompensas de abates com integrantes online no mesmo mundo e a até 16 blocos do jogador que derrotou a criatura. /expedicaogrupo inicia uma expedição cooperativa pelo líder: exige pelo menos dois integrantes online, no mesmo mundo e a até 24 blocos; todos precisam cumprir o nível mínimo da dificuldade. Cada participante registrado que permanecer online recebe a recompensa integral individual. O líder pode cancelar com /expedicaogrupo cancelar; se desconectar, a expedição é encerrada e os inimigos são removidos.
- Cargos de guilda têm líder, oficial e membro. Oficiais podem convidar e expulsar membros comuns; somente o líder pode promover/rebaixar oficiais, expulsar oficiais, transferir liderança e sacar do banco. Territórios podem ser reivindicados e abandonados pelo líder. Durante uma guerra ativa, cinco abates válidos de membros defensores dentro do território transferem a área para a guilda atacante e concedem 250 moedas ao banco; abates defensivos reduzem o progresso. A captura exige espaço no limite de três territórios. A proteção contra explosões remove os blocos protegidos da lista de destruição, sem impedir dano a entidades. Pistões são bloqueados quando estão posicionados dentro do território; eventos de extensão/retração também verificam os blocos movidos. A geometria completa de mecanismos externos ainda precisa de validação em Paper real. Os eventos de início e propagação de fogo são cancelados dentro do território. Fluxos de água/lava são cancelados quando a origem está dentro da área ou na margem de um bloco ao redor; isso evita a entrada imediata pela borda, mas não é uma barreira física para líquidos que já tenham atravessado antes da atualização. Dispensers e droppers localizados dentro do território têm sua ativação bloqueada, inclusive os pertencentes à própria guilda, pois o evento não identifica com segurança o proprietário do mecanismo. Dispensers externos que disparam para dentro ainda não são bloqueados. Veículos que possuem inventário têm dano e destruição bloqueados dentro da área; veículos sem inventário não são cobertos por essa regra. Jogadores de fora da guilda não conseguem recolher itens dropados dentro do território; membros da guilda proprietária podem. Itens dropados também são protegidos contra dano de fogo, queimadura, lava e explosões na área, e não podem ser empurrados para fora da fronteira do território nem transportados por portais do Nether/End para fora da área. Pilhas de itens de dentro e de fora de territórios não podem se fundir na fronteira, evitando que a pilha resultante atravesse a proteção. Itens dropados na área também não desaparecem pelo temporizador natural enquanto permanecerem dentro do território; isso pode acumular entidades e exige limpeza administrativa periódica. Ainda não há impostos nem arenas isoladas.
- Cada classe tem 3% de chance de despertar no momento da primeira escolha; não há novo sorteio para personagens que já escolheram classe. Os despertares são permanentes. O Monarca pode invocar três soldados temporários com /invocar e consultar com /sombras. Ao derrotar monstros diretamente, há 15% de chance de extrair uma sombra permanente, com limite de cinco; /exercito lista as sombras, /sombranivel <1-5> consulta o nível e XP, e /libertar <1-5> libera um espaço. Cada sombra permanente ganha XP ao derrotar monstros e evolui a cada cinco XP por nível, até o nível 10. /posturasombras agressiva|defensiva|passiva controla a seleção automática de alvos: agressiva reage a ataques do Monarca e contra ele; defensiva só protege o Monarca; passiva não escolhe alvos automaticamente. /reunirsombras teleporta os soldados vivos para perto do Monarca. As sombras permanentes são representadas por esqueletos Wither e podem ser destruídas por inimigos. O rank dos soldados temporários evolui com o nível do Monarca: C (1+), B (10+), A (25+) e S (50+), aumentando seus efeitos de combate.
- O mercado mantém itens anunciados em custódia nas variáveis do Skript; não possui taxa, interface gráfica ou histórico de transações.
- O chefe mundial e as expedições usam criaturas vanilla e dependem de espaço livre no local onde são iniciados.
- Guerras de guilda usam um placar global e não isolam PvP por região; a administração deve combinar regras de arena e duração. As recompensas PvP ainda precisam de proteção contra combinação de mortes entre contas.
- A HUD usa a action bar e pode sobrescrever mensagens de action bar enviadas por outros plugins. Os eventos mundiais são iniciados manualmente.

## Validação
O GitHub Actions verifica estrutura, ausência de marcadores de placeholder e empacota ZIP. Isso não comprova sintaxe Skript nem execução em Paper 26.3. Teste /sk reload all e todos os sistemas em servidor de homologação antes de produção.


### Auditoria de limpeza de territórios (0.43.0)
- Cada execução confirmada de `/rpgitenslimpar CONFIRMAR` registra data/hora, administrador (nome e UUID), mundo, território, posição e quantidade de entidades removidas.
- Administradores podem consultar o histórico persistente com `/rpgitenslog`.
- O histórico fica salvo nas variáveis persistentes do Skript; não é um arquivo externo e não possui rotação automática nesta versão.


### Proteção de plantações e terreno agrícola (0.44.0)
- Entidades não podem alterar blocos dentro de territórios reivindicados; isso bloqueia pisoteio de farmland e alterações de blocos feitas por mobs.
- O evento de ovelhas comerem grama também é cancelado dentro dos territórios.
- Jogadores de fora continuam impedidos de quebrar/colocar blocos pelas proteções gerais; membros da guilda proprietária podem colher normalmente.
- A proteção de alterações por entidades também afeta comportamentos como Endermen pegando/colocando blocos e blocos móveis; valide no Paper antes de ativar em produção.


### Estatísticas de fazenda (0.45.0)
- O servidor contabiliza colheitas maduras de trigo, cenoura, batata, beterraba e verruga do Nether dentro de territórios da própria guilda.
- `/guildcolheita` mostra o total individual e o total acumulado da guilda.
- O sistema é estatístico: não altera drops, não concede XP/moedas e não conta colheitas fora dos territórios da guilda.


### Progressão de agricultura (0.46.0)
- Cada colheita madura válida concede 5 XP de agricultura.
- A experiência necessária para o próximo nível é 100 × nível atual.
- Cada nível concede 50 moedas; níveis múltiplos de 5 concedem mais 100 moedas e desbloqueiam títulos: Agricultor Experiente (5), Cultivador Veterano (10) e Mestre da Colheita (15).
- O comando /guildcolheita agora mostra nível e XP individuais, além das estatísticas da guilda.
- A progressão é individual e persistente; somente colheitas em territórios da própria guilda contam.


### Pecuária de guilda (0.47.0)
- Alimentar vacas, ovelhas, cabras, coguvacas, porcos, galinhas e coelhos com seus alimentos adequados em território próprio registra alimentação e concede 2 XP de pecuária, com limite de uma contagem por animal a cada 30 segundos.
- Reprodução de animais dentro do território próprio concede 20 XP ao jogador que realizou a reprodução e atualiza os totais pessoais e da guilda.
- A progressão é individual: cada nível concede 25 moedas; níveis múltiplos de 5 concedem mais 75 moedas e desbloqueiam títulos nos níveis 5, 10 e 15.
- O comando /guildpecuaria mostra nível, XP, título, alimentações e reproduções.

### Montarias evolutivas (0.48.0)
- Cavalos domados pelo jogador ganham 5 XP a cada 8 blocos percorridos com seu dono montado.
- A cada nível, a velocidade e a força de salto aumentam gradualmente, respeitando limites configurados; os atributos-base individuais do cavalo são preservados.
- Cavalos nascidos por reprodução dentro do território da própria guilda têm 5% de chance de se tornarem Corcéis Raros, com bônus de vida, velocidade e salto.
- O comando /montaria mostra nível, XP, distância registrada e raridade da montaria atual.
- A evolução é vinculada ao UUID do cavalo e persiste após reinícios.

### Acessórios de pets (0.50.0)
- Cada espécie possui um acessório compatível: Coleira de Caça (lobo), Amuleto Vital (gato) ou Pena Celeste (papagaio).
- Cada acessório custa 300 moedas, é desbloqueado permanentemente e concede um bônus passivo enquanto o companheiro está invocado.
- /petacessorio loja|comprar|equipar|remover|status administra o equipamento.

### Pets companheiros (0.49.0)

- Cada jogador pode adotar um companheiro: lobo (combate), gato (regeneração e visão noturna) ou papagaio (mobilidade).
- A adoção tem 5% de chance de raridade Rara; pets raros fortalecem suas habilidades e recebem resistência adicional.
- /pet chamar, /pet guardar, /pet status e /pet habilidade controlam o companheiro.
- Lobos recebem como alvo monstros atacados pelo dono e ganham XP por abates; gatos e papagaios podem receber XP quando o dono derrota monstros enquanto estão invocados.
- Evolução até o nível 10; no nível 5, o lobo recebe mais força e as habilidades de gato e papagaio melhoram; no nível 10, o lobo recebe velocidade adicional.
- O pet é recolhido quando o dono desconecta. Espécie, raridade, nível e XP permanecem salvos.
- O sistema usa entidades vanilla e Skript, sem addons. A validação em Paper real ainda é necessária.


### Árvore de talentos dos pets (0.51.0)
- Pets ganham 1 ponto de talento a cada dois níveis após o nível 1; os pontos são persistentes e calculados pelo nível e talentos gastos.
- /pettrilha mostra a árvore da espécie e os pontos disponíveis; /pettalento <nome> desbloqueia um talento compatível com lobo, gato ou papagaio.
- Lobo: Mordida (força para o pet), Guardião (resistência ao dono) e Rastreador (velocidade ao dono).
- Gato: Ronronar (regeneração), Reflexo (velocidade) e Vigia (visão noturna).
- Papagaio: Corrente (velocidade), Plumagem (resistência) e Observador (visão noturna).
- Cada talento custa um ponto e só pode ser desbloqueado uma vez. Efeitos são aplicados enquanto o pet está invocado.
- A implementação requer validação de sintaxe e runtime em servidor Paper real.


### Combate montado (0.52.0)
- Abates de monstros enquanto o jogador monta seu próprio cavalo concedem 10 XP à montaria.
- Ataques montados contra monstros recebem bônus de dano escalonado pelo nível da montaria, limitado a +3.
- A habilidade Investida é desbloqueada no nível 5: concede velocidade e força ao cavaleiro e velocidade e resistência ao cavalo por 8 segundos, com recarga de 60 segundos.
- /montariacombate status mostra nível e abates montados; /montariacombate habilidade ativa a Investida.
- O combate montado não aplica bônus de dano contra outros jogadores.
- Requer teste de sintaxe e execução em servidor Paper real.


### Drops exclusivos de chefes (0.53.0)
- Concluir a expedição e derrotar o Devorador das Ruínas concede um equipamento exclusivo aleatório, além das recompensas normais.
- Cada participante registrado do Titã da Fenda recebe dois sorteios de equipamento exclusivo.
- Lâmina do Devorador: espada de diamante com +3 de dano contra criaturas.
- Couraça das Ruínas: peitoral de diamante que reduz 3 de dano recebido.
- Arco do Titã: arco lendário que causa +4 de dano com flechas contra criaturas.
- Os equipamentos são identificados por nome; renomear em bigorna pode afetar a identificação. PvP não recebe os bônus.
- Teste de sintaxe e runtime em Paper real ainda necessário.


### Dificuldades de expedição (0.54.0)
- /expedicao normal: nível 10+, inimigos com atributos base, 600 moedas, 400 XP, 3 diamantes e 1 sorteio de equipamento de chefe.
- /expedicao heroica: nível 20+, 1,5x de vida nos inimigos, 900 moedas, 600 XP, 4 diamantes e 2 sorteios.
- /expedicao pesadelo: nível 35+, 2x de vida nos inimigos, 1.200 moedas, 800 XP, 6 diamantes e 3 sorteios.
- A dificuldade escolhida permanece vinculada à expedição e determina os atributos das ondas e do chefe final.
- Necessário testar sintaxe e execução em Paper real; o workflow valida estrutura e empacotamento, não runtime.


### Expedições cooperativas (0.55.0)
- /expedicaogrupo normal|heroica|pesadelo inicia uma expedição usando os integrantes online do grupo do líder, no mesmo mundo e a até 24 blocos.
- São necessários pelo menos dois participantes; todos devem cumprir o nível mínimo da dificuldade (10, 20 ou 35).
- O grupo enfrenta as três ondas da expedição. Cada participante registrado que estiver online na conclusão recebe moedas, XP, diamantes e sorteios individuais conforme a dificuldade.
- /expedicaogrupo cancelar encerra a sessão; a desconexão do líder também encerra e remove os inimigos.
- O fluxo é separado da expedição solo. Requer teste de sintaxe e execução em servidor Paper real.


### Arena das Ruínas (0.56.0)
- /arenadungeon iniciar exige nível 15; /arenadungeon status consulta a sala atual e /arenadungeon cancelar encerra o encontro.
- Sala 1: três Sentinelas das Ruínas; recompensa intermediária de 75 moedas e uma maçã dourada.
- Sala 2: quatro Aranhas Armadilhadas; recompensa intermediária de 125 moedas e duas maçãs douradas.
- Sala 3: chefe Guardião Arcano (evocador fortalecido); recompensa final de 300 moedas, 250 XP, três diamantes, uma maçã dourada encantada e um equipamento de chefe.
- O encontro é encerrado e seus inimigos removidos ao cancelar ou desconectar. Esta versão não constrói blocos nem altera terreno; as salas são etapas de combate no local de início. Requer validação em Paper real.


### Armas lendárias (0.57.0)
- /forjarlendaria espada|machado|arco forja uma arma de netherita ou arco por 1 barra de netherita, 8 diamantes e 1.500 moedas; cada tipo pode ser forjado uma vez por jogador.
- Lâmina Solar: Fúria Solar (Força II e Resistência ao Fogo por tempo curto).
- Machado do Colosso: Vigor do Colosso (Resistência II e Força I).
- Arco da Tempestade: Passo da Tempestade (Velocidade III e Salto II); o bônus de dano é aplicado ao impacto da flecha.
- Abates com a arma evoluem maestria até o nível 5; cada nível aumenta o bônus de dano e reduz a recarga da habilidade, com mínimo de 30 segundos.
- /poderarma ativa a habilidade da arma segurada; /maestriaarma consulta os níveis. Os dados de maestria ficam persistidos por jogador e tipo de arma.
- Itens são identificados pelo nome e ainda podem ser afetados por renomeação em bigorna. Requer teste de sintaxe e runtime em Paper real.


### Arenas cooperativas de raid (0.60.0)
- A administração configura os pontos de surgimento das três salas com `/raidarena configurar 1`, `/raidarena configurar 2` e `/raidarena configurar 3`, posicionando-se no local desejado. Os três pontos devem ficar no mesmo mundo.
- O líder inicia com `/raidarena normal|heroica|pesadelo`. São exigidos pelo menos dois membros online do grupo, no mesmo mundo e a até 24 blocos do líder; níveis mínimos 10/20/35.
- Sala 1: três Guardiões (zumbis). Sala 2: quatro Sentinelas (esqueletos). Sala 3: Titã da Arena (ravager) com 500/900/1.400 de vida.
- Ao concluir cada uma das duas primeiras salas, cada membro registrado recebe um baú virtual, aberto por `/raidbau abrir`; `/raidbau status` consulta a quantidade. O baú entrega aleatoriamente moedas, XP, diamantes ou maçã dourada.
- Ao derrotar o Titã, moedas, XP e diamantes são distribuídos proporcionalmente ao dano registrado; participantes que causaram dano também recebem um item de chefe e um baú. Dificuldades concedem recompensas-base de 800/1.400/2.400 moedas, 500/900/1.500 XP e 3/5/8 diamantes.
- `/raidarena status` consulta a sala e inimigos restantes; `/raidarena cancelar` encerra o encontro. A desconexão do líder remove os inimigos e encerra a sessão.
- Limitação: são pontos de surgimento configurados manualmente, não estruturas construídas automaticamente nem instâncias isoladas. A implementação usa mobs vanilla e precisa de teste de sintaxe e runtime em Paper real; o workflow de GitHub não comprova execução. Os ataques especiais do Titã usam dano e efeitos de poção; balanceamento e interação com armaduras precisam ser verificados em jogo.


### Evolução de armas lendárias (0.62.0)
- Cada arma lendária pode receber até três níveis de evolução, persistidos por jogador e tipo de arma, mesmo após reinícios.
- /melhorararma espada|machado|arco exige que o jogador segure a arma correspondente e tenha 1 barra de netherita, 4 diamantes e 750 moedas por nível.
- Cada nível acrescenta +2 de dano contra criaturas; no arco, o nível é registrado no disparo e aplicado quando a flecha atinge uma criatura.
- /evolucaoarma mostra o progresso das três armas. O lore da arma segurada é atualizado no aprimoramento.
- A evolução usa variáveis persistentes do Skript; não cria identificador NBT/PDC. Renomear a arma em bigorna ainda pode impedir o reconhecimento. É necessário validar sintaxe e combate em Paper real.


### Armaduras lendárias evolutivas (0.63.0)
- Cada peça da armadura de classe pode evoluir até o nível III; o progresso fica salvo por jogador e peça.
- `/evoluirarmadura capacete|peitoral|calcas|botas` exige a peça da própria classe equipada no slot correto e custa 1 barra de netherita, 2 diamantes e 500 moedas por nível.
- `/evolucaoarmadura` consulta os níveis das quatro peças.
- Com o conjunto completo equipado, `/guardialendaria` ativa Resistência e Absorção temporárias; a potência depende da soma dos níveis das peças e há recarga de 90 segundos.
- O conjunto completo também reduz dano recebido: 1 ponto quando a soma dos níveis é 4–7 e 2 pontos a partir de 8.
- A identificação das peças continua baseada no nome do item; renomear em bigorna pode impedir o reconhecimento. Sintaxe, efeitos e equilíbrio precisam ser validados em Paper real; Actions verifica empacotamento, não runtime Skript.


### Artefatos lendários e conjuntos (0.64.0)
- `/artefato loja` lista oito artefatos distribuídos em quatro espaços: anel, amuleto, relíquia e charme.
- `/artefato comprar <nome>` desbloqueia permanentemente um artefato usando moedas; `/artefato equipar <nome>` equipa o artefato no espaço correspondente; `/artefato remover <espaco>` libera o espaço; `/artefato status` mostra os espaços e a contagem dos conjuntos.
- Conjunto Solar: Anel Solar, Amuleto Aurora, Insígnia do Guardião e Charme do Vento. Conjunto Abissal: Anel Abissal, Amuleto Abissal, Insígnia Abissal e Charme Abissal.
- Cada artefato concede efeitos passivos enquanto equipado. Duas peças do mesmo conjunto ativam um bônus adicional; quatro peças desbloqueiam `/despertarartefato`, com efeitos por 10 segundos e recarga de 120 segundos.
- Artefatos são desbloqueios virtuais persistentes, não itens físicos; isso evita duplicação e perda por morte. Os efeitos, sintaxe e balanceamento precisam de validação em Paper real. GitHub Actions valida empacotamento, não execução Skript.


### Árvores de talentos por classe (0.65.0)
- Cada classe possui três talentos exclusivos, com passivas ou bônus de combate. `/arvoreclasse` consulta a árvore e `/aprenderclasse <talento>` desbloqueia um talento usando um ponto.
- `/resgatarpontosclasse` entrega um ponto por marco de cinco níveis alcançados, sem permitir resgatar o mesmo marco duas vezes.
- `/supremaclasse` desbloqueia no nível 30, consome 50 de mana e tem recarga de 180 segundos. Cada classe possui uma suprema própria: Avatar de Guerra, Cataclismo Arcano, Execução Sombria ou Chuva Celestial.
- Pontos, talentos e marcos resgatados são persistentes por jogador. As habilidades usam entidades vanilla; dano em área, efeitos, balanceamento e sintaxe precisam de validação em Paper real. GitHub Actions valida estrutura e empacotamento, não runtime Skript.


### Endgame e prestígio (0.66.0)
- Progressão principal limitada ao nível 100. A XP excedente é descartada ao atingir o limite, evitando acumular XP antes de um prestígio.
- `/endgame` mostra nível, XP, prestígio e fichas. `/prestigio` exige nível 100 e concede um renascimento, até 10 vezes.
- Cada prestígio reinicia nível e XP, mas preserva classe, especialização, atributos, talentos, equipamentos, pets e guilda. Recompensa: 5 pontos de atributo, 1.000 moedas e 1 ficha de prestígio.
- Cada prestígio aumenta permanentemente a XP recebida em 5%, até +50% no prestígio 10. As fichas ficam contabilizadas para futuras recompensas de endgame; ainda não têm loja de troca.
- A integração da nova curva precisa ser testada em Paper real. GitHub Actions verifica empacotamento, não sintaxe/runtime Skript.


### Loja de prestígio (0.67.0)
- `/lojaprestigio` lista quatro melhorias permanentes compradas com fichas recebidas ao renascer.
- `/vitalidadeeterna` custa 1 ficha e concede Regeneração I; `/forcaeterna` custa 2 e adiciona 2 de dano contra criaturas; `/guardiaoeterno` custa 2 e concede Resistência I; `/menteeterna` custa 3 e acelera a regeneração de mana em +2 por ciclo.
- Cada melhoria é única por personagem. Os efeitos são aplicados enquanto o jogador está online.
- Necessário validar os efeitos, aliases e sintaxe em uma instância Paper real; o workflow de empacotamento não executa o Skript.


### Títulos cosméticos (0.68.0)
- `/titulos` lista títulos disponíveis e marcos necessários; `/titulo equipar <nome>` equipa e `/titulo remover` remove.
- Aprendiz (nível 10), Veterano (25), Campeão (50), Lenda (100), Renascido (prestígio 1), Ascendente (5) e Eterno (10).
- O título equipado aparece no `/perfil`. Os títulos são cosméticos e não concedem atributos ou vantagens de combate.


### Conquistas (0.69.0)
- `/conquistas` mostra o progresso de caça, construção e PvP.
- Caça: 10, 50 e 100 criaturas derrotadas; Construção: 100 e 500 blocos quebrados; PvP: 5 e 25 vitórias.
- Cada marco concede moedas e XP automaticamente uma única vez por jogador. Progresso e desbloqueios são persistidos nas variáveis do Skript.
- A validação disponível no GitHub Actions é de empacotamento. Eventos, recompensas e sintaxe precisam de teste em Paper com Skript instalado.


### Ranking global (0.70.0)
- `/rpgranking` (aliases `/rankingrpg` e `/toprpg`) mostra os dez melhores jogadores atualmente online.
- A pontuação combina prestígio, nível, vitórias PvP e conquistas; prestígio tem maior peso, seguido de nível.
- O ranking é calculado em tempo real e não exige banco de dados externo. Jogadores offline não aparecem nesta versão.
- A sintaxe e o comportamento do comando precisam de validação em Paper com Skript; o workflow do repositório valida estrutura/empacotamento, não runtime.


### Temporadas competitivas (0.71.0)
- Administração: `/rpgtemporada iniciar <nome>` inicia uma temporada e `/rpgtemporada encerrar` finaliza e registra o campeão entre os jogadores online naquele momento.
- Pontuação sazonal independente das estatísticas permanentes: 25 pontos por vitória PvP e 5 por criatura derrotada.
- `/rankingtemporada` (alias `/toptemporada`) mostra o top 10 online; `/pontostemporada` consulta os próprios pontos e `/historicotemporadas` lista campeões registrados.
- Os dados são separados por número de temporada; iniciar outra temporada não apaga níveis, moedas, kills PvP nem pontuações anteriores.
- Limitação: o campeão é escolhido entre jogadores online no encerramento e o ranking exibe apenas jogadores online. Não há premiação automática nesta versão. Eventos e sintaxe precisam de teste em Paper com Skript; Actions verifica estrutura/empacotamento, não runtime.


### Recompensas de temporadas (0.72.0)
- Ao encerrar a temporada, o campeão registrado recebe 2.000 moedas e 500 XP pendentes, além do título sazonal exibido no `/perfil`.
- Participantes que alcançaram pelo menos 100 pontos recebem 300 moedas e 100 XP pendentes.
- `/recompensatemporada` consulta e resgata as recompensas uma única vez; os valores pendentes ficam associados ao UUID e podem ser resgatados mesmo após reconectar.
- A pontuação e os prêmios de temporadas anteriores permanecem salvos. O título sazonal é cosmético.
- Requer validação no Paper/Skript real. O workflow automatizado verifica empacotamento/estrutura, não execução dos eventos.


### Temporadas automáticas (0.73.0)
- `/rpgtemporadaauto iniciar <dias>` inicia uma temporada e programa seu encerramento; a duração aceita é de 1 a 90 dias.
- Ao atingir o prazo, o servidor encerra a temporada pelo fluxo normal, calcula campeão e recompensas e inicia automaticamente a próxima temporada.
- `/rpgtemporadaauto status` mostra se a rotação está ativa e o término previsto. `/rpgtemporadaauto parar` desativa a rotação futura; a temporada em andamento continua e poderá ser encerrada manualmente com `/rpgtemporada encerrar`.
- O encerramento possui uma trava para evitar processamento duplicado. O campeão é calculado a partir de todos os participantes registrados, inclusive quem estiver offline.
- `/rpgtemporada iniciar <nome>` continua disponível para temporadas manuais. Temporadas automáticas usam nomes numerados.
- O agendador verifica o prazo uma vez por minuto; o horário efetivo pode atrasar até aproximadamente um minuto.
- Requer validação em Paper/Skript real: o workflow do GitHub verifica apenas estrutura e empacotamento.


### Modo solo da Raid Arena, /spawn, /party e menu RPG
- A Raid Arena aceita um único participante válido; não é mais obrigatório ter dois membros online no grupo.
- Quando apenas um jogador participa, o Titã recebe 60% da vida configurada para a dificuldade escolhida. Em grupo, a vida original permanece.
- `/party` é um alias de `/grupo`; os demais comandos de grupo continuam disponíveis, como `/grupocriar`, `/grupoconvidar <jogador>`, `/grupoaceitar` e `/gruposair`.
- `/spawn` teleporta o jogador ao ponto de spawn do mundo atual.
- O primeiro acesso entrega uma bússola encantada chamada **MENU RPG**. Clique com o botão direito para abrir o menu de atalhos. `/menurpg` (alias `/menu`) abre o menu manualmente e `/menuitem` entrega uma bússola substituta caso o item seja perdido.
- Os atalhos incluem Spawn, Perfil, Raid Arena normal, Party, Baú de Raid, Atributos e Ajuda.
- Requer recarga e validação no Paper/Skript real; o workflow do GitHub verifica estrutura e empacotamento, não a execução dos eventos e inventários.
