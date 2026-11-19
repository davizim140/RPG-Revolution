## 0.27.0 - Proteção adicional de territórios
- Explosões deixam de destruir blocos dentro de territórios reivindicados.
- Pistões posicionados dentro de territórios não podem estender ou retrair.
- O dano de explosões a entidades não é bloqueado; pistões externos que avançam para dentro ainda exigem validação em servidor Paper.

## 0.26.0 - Guerra por territórios
- Abates PvP de membros das guildas em guerra dentro de um território geram progresso de captura.
- Cinco pontos transferem o território; abates defensivos reduzem o progresso.
- A guilda conquistadora recebe 250 moedas no banco, respeitando o limite de três territórios.
- /guildterritorioguerra (alias /gtg) consulta o progresso no local.

## 0.25.0 - Territórios de guilda
- Líder pode reivindicar até três áreas quadradas de 33x33 blocos por 500 moedas do banco.
- Áreas reivindicadas bloqueiam quebra, colocação e interação de blocos por jogadores de outras guildas.
- /guildterritorio ajuda|reivindicar|info|abandonar.
- Corrigido o cargo inicial do fundador: agora recebe o papel de líder.

## 0.24.0 - Hierarquia e permissões de guilda
- Adicionados os cargos líder, oficial e membro.
- Líder pode promover/rebaixar oficiais; oficiais podem convidar e expulsar membros comuns.
- /guildacargos lista os cargos dos integrantes.
- Ajuda corrigida e atualizada com os comandos de cargos.

# Changelog

## 0.21.0 - Evolução individual das sombras
- Sombras permanentes ganham XP ao derrotar monstros.
- Evolução individual até o nível 10, com bônus graduais de velocidade, força e resistência.
- /sombranivel <1-5> consulta o nível e a experiência de cada sombra.
- Dados de evolução são limpos ao libertar ou detectar a morte da sombra.


## 0.20.0 - Extração permanente de sombras
- Monarca tem 15% de chance de extrair uma sombra ao derrotar diretamente um monstro.
- Até cinco sombras permanentes por jogador; /exercito lista e /libertar <1-5> remove uma sombra.
- Sombras permanentes seguem o Monarca, recebem alvos quando ele combate e não podem causar dano ao próprio invocador.
- Sombras permanentes são esqueletos Wither nomeados conforme o inimigo derrotado; podem morrer em combate.


## 0.19.0 - Classes do Exército das Sombras
- Invocação passa a criar três soldados especializados: Tanque (golem de ferro), Guerreiro (esqueleto wither) e Arqueiro (esqueleto com arco).
- Cada função recebe efeitos próprios; os bônus de rank continuam escalando com o nível do Monarca.
- Limite de três soldados ativos e status atualizado em /sombras.


## 0.18.0 - Evolução do Exército das Sombras
- Rank dos soldados agora acompanha o nível do Monarca: C (nível 1+), B (10+), A (25+) e S (50+).
- Cada rank aplica efeitos de combate progressivamente melhores; o rank é definido no momento da invocação.
- /sombras agora informa nível do Monarca, rank atual e quantidade de soldados ativos.


## 0.17.0 - Exército das Sombras
- Monarca das Sombras pode invocar dois soldados (esqueletos wither) por 45 segundos com /invocar.
- Invocação custa 50 de mana e usa recarga compartilhada de 60 segundos.
- Soldados recebem alvos quando o Monarca ataca criaturas ou é atacado; dano dos soldados contra o próprio invocador é cancelado.
- /sombras mostra quantos soldados ainda estão ativos.


## 0.16.0 - Despertares para todas as classes
- Guerreiro: 3% de chance de despertar como Colosso; /furia concede força III e resistência II.
- Mago: 3% de chance de despertar como Arquimago; /arcano concede regeneração II e resistência I.
- Arqueiro: 3% de chance de despertar como Olho Celestial; /precisao concede velocidade III e visão noturna.
- Cada despertar tem passiva de dano, custo de mana e recarga próprios; /despertar exibe os poderes.


## 0.15.0 - Despertar de classe: Monarca das Sombras
- Ao escolher Assassino pela primeira vez, o personagem tem 3% de chance de despertar.
- Despertados recebem +2 de dano e desbloqueiam /sombra: velocidade III, força II e invisibilidade por 10 segundos, com custo de 35 mana e recarga de 30 segundos.
- /despertar mostra o status e os poderes; o despertar é permanente.


## 0.14.0 - Invasão mundial
- Adicionado evento manual de invasão com cinco inimigos resistentes.
- Participantes que acertarem os invasores recebem 200 moedas e 100 XP quando a invasão termina.
- Administração pode iniciar ou encerrar com /invasao iniciar|encerrar.


## 0.13.0 - Encontros de masmorra mais seguros
- Adicionado /masmorra cancelar para encerrar o encontro voluntariamente.
- O chefe é removido quando o jogador desconecta, evitando encontros órfãos.
- O UUID do chefe continua vinculando a recompensa ao encontro individual.


## 0.12.0 - HUD do personagem
- Adicionada HUD na action bar com nível, XP, vida e mana, atualizada a cada 2 segundos.
- Adicionado /rpghud on|off para controle individual.
- Corrigida a documentação do alcance atual da proteção de regiões.


## 0.11.0 - Regiões com nível mínimo
- Regiões configuradas agora bloqueiam teletransportes entre mundos quando o personagem não atende ao nível mínimo.
- /regiao mostra o nível exigido e o nível atual do jogador.
- Adicionado /rpgregiao remover para retirar a configuração do mundo atual.


## 0.10.0 - NPCs físicos
- Adicionado gerenciamento administrativo de NPCs com aldeões vanilla.
- Clique com o botão direito nos NPCs para abrir os diálogos existentes de guia, ferreiro e exploradora.
- Comandos /rpgnpc criar e /rpgnpc limpar; sem Citizens ou addons de Skript.


## 0.9.0 - Grupos e progressão cooperativa
- Criados grupos com convite, entrada, saída, expulsão e encerramento pelo líder.
- Integrantes online no mesmo mundo e a até 16 blocos recebem parte do XP e moedas por abates.
- Ajuda e documentação atualizadas.

## 0.8.0 - Armaduras, guildas e contratos
- Adicionadas quatro peças de armadura por classe e bônus ao completar o conjunto.
- Guerreiro recebe redução de dano; Mago e Assassino recebem bônus corpo a corpo; Arqueiro recebe velocidade.
- Guildas agora permitem transferência de liderança, expulsão, chat e banco compartilhado.
- Contrato diário de caça a 10 esqueletos, com 150 moedas e 100 XP.

## 0.7.0 - Equipamentos exclusivos de classe
- Mago pode fabricar Cajado Arcano.
- Assassino pode fabricar Adaga Sombria.
- Arqueiro pode fabricar Arco do Batedor.

## 0.6.0 - Atributos e aprimoramento de equipamentos
- Espada do Aprendiz aplica bônus de dano, escalando até +3.
- Couraça do Guardião reduz dano recebido, escalando até +3.
- /aprimorar consome diamantes e moedas.

## 0.5.0 - Artesanato e raridades
- Receitas próprias para espada incomum, couraça épica e arco épico.

## 0.4.0 - NPCs e linha de história
- Diálogos por comando e missões persistentes de coleta e caça.

## 0.3.0 - Sistemas de mundo e comunidade
- Regiões informativas, loja, masmorra, guildas e recompensa diária.

## 0.2.0 - Classes
- Quatro classes, habilidades ativas, mana e especializações.

## 0.1.0 - Fundação
- Personagens, níveis, XP, atributos, economia e missão inicial.
- Workflow de verificação estrutural e empacotamento ZIP.
