## 0.52.0 - Combate montado
- Abates de monstros enquanto o jogador monta seu próprio cavalo concedem 10 XP à montaria.
- Ataques montados contra monstros recebem bônus de dano conforme o nível, limitado a +3.
- Investida desbloqueia no nível 5 e concede efeitos de combate ao cavaleiro e à montaria por 8 segundos, com recarga de 60 segundos.
- Novo comando /montariacombate status|habilidade.

## 0.51.0 - Árvore de talentos dos pets
- Adicionado sistema de pontos de talento: 1 ponto a cada dois níveis do pet após o nível 1.
- Cada talento custa um ponto e pode ser adquirido uma única vez; pontos gastos e talentos são persistentes.
- Lobo: Mordida, Guardião e Rastreador. Gato: Ronronar, Reflexo e Vigia. Papagaio: Corrente, Plumagem e Observador.
- Efeitos de suporte são mantidos enquanto o pet estiver vivo e invocado.
- Novos comandos /pettrilha e /pettalento.

## 0.50.0 - Acessórios de pets
- Adicionados Coleira de Caça para lobos, Amuleto Vital para gatos e Pena Celeste para papagaios.
- Cada acessório custa 300 moedas, é comprado uma única vez e fica desbloqueado permanentemente.
- Bônus passivos são aplicados enquanto o pet correspondente está invocado: força, regeneração ou velocidade.
- Novo comando /petacessorio com loja, compra, equipamento, remoção e status.

## 0.49.0 - Pets companheiros
- Adicionados três companheiros adotáveis: lobo, gato e papagaio, cada um com função e habilidade próprias.
- 5% de chance de adoção Rara; raridade amplia a habilidade e concede resistência adicional.
- Comandos /pet, /pet adotar, chamar, guardar, status e habilidade.
- Lobos auxiliam no combate ao atacar monstros enfrentados pelo dono; abates evoluem o companheiro até o nível 10.
- Gatos e papagaios também evoluem quando o dono derrota monstros enquanto o pet está invocado; habilidades melhoram no nível 5.
- Dados de espécie, raridade e evolução ficam persistidos por jogador; pets ativos são recolhidos ao desconectar.

## 0.48.0 - Montarias evolutivas e corcéis raros
- Cavalos domados ganham 5 XP a cada 8 blocos percorridos pelo próprio dono montado.
- Níveis aumentam velocidade e força de salto gradualmente, preservando os atributos-base individuais e aplicando limites.
- Reprodução de cavalos em território da própria guilda tem 5% de chance de gerar um Corcel Raro, com bônus de vida, velocidade e salto.
- Novo comando /montaria exibe nível, XP, distância e raridade.
- Dados de evolução são persistidos por UUID da montaria.

## 0.47.0 - Pecuária de guilda
- Alimentar animais com alimentos correspondentes dentro do território da própria guilda registra alimentações e concede 2 XP, com limite por animal a cada 30 segundos.
- Reproduções iniciadas por jogadores dentro do território próprio concedem 20 XP e atualizam estatísticas pessoais e coletivas.
- Adicionada progressão individual de pecuária, com 25 moedas por nível e bônus de 75 moedas nos níveis múltiplos de 5.
- Títulos próprios de pecuária são desbloqueados nos níveis 5, 10 e 15.
- Novo comando /guildpecuaria.

## 0.46.0 - Níveis e recompensas de agricultura
- Cada colheita madura válida concede 5 XP de agricultura.
- A cada nível, o jogador recebe 50 moedas; múltiplos de 5 concedem bônus adicional de 100 moedas e desbloqueiam títulos nos níveis 5, 10 e 15.
- /guildcolheita exibe nível e XP de agricultura individual.
- XP e nível são persistidos por jogador.

## 0.45.0 - Estatísticas de fazenda de guilda
- Adicionado contador individual e coletivo para colheitas maduras de trigo, cenoura, batata, beterraba e verruga do Nether dentro do território da própria guilda.
- Novo comando /guildcolheita consulta os totais.
- O recurso é apenas estatístico: não altera itens, XP ou moedas.

## 0.44.0 - Proteção de plantações em territórios
- Cancela alterações de blocos provocadas por entidades dentro de territórios, incluindo pisoteio de terreno agrícola e mudanças feitas por mobs.
- Cancela explicitamente o evento de ovelhas comendo grama dentro das áreas protegidas.
- Membros da guilda proprietária continuam podendo colher manualmente; a proteção geral de quebra/colocação permanece inalterada.
- A proteção genérica também afeta Endermen e blocos móveis; requer teste de runtime no Paper.

## 0.43.0 - Auditoria de limpeza de itens
- Limpezas confirmadas registram horário, administrador, UUID, mundo, território, posição e quantidade removida.
- Novo comando administrativo /rpgitenslog consulta o histórico persistente.
- O histórico não tem rotação automática nesta versão.

## 0.42.0 - Limpeza administrativa de itens em territórios
- Adicionado /rpgitenslimpar para administradores dentro do território atual.
- A remoção exige o argumento CONFIRMAR e informa que todos os itens dropados da área serão removidos, inclusive itens legítimos.
- A limpeza é manual; não há remoção automática nem filtro confiável de idade/autor do item.

## 0.41.0 - Proteção contra despawn de itens em territórios
- Cancela o desaparecimento natural de itens dropados enquanto estiverem dentro de territórios reivindicados.
- Fora da área protegida, o temporizador normal de despawn continua funcionando.
- Atenção: itens podem se acumular em territórios; a administração deve fazer limpeza periódica quando necessário.

## 0.40.0 - Proteção de pilhas de itens na fronteira de territórios
- Impede que itens dropados dentro e fora de um território se fundam em uma única pilha ao se encontrarem na fronteira.
- Mantém o comportamento normal de fusão quando os dois itens estão do mesmo lado da fronteira.
- A proteção de movimento por água já existente continua bloqueando itens que tentem sair da área reivindicada.

## 0.39.0 - Protecao de itens contra portais\n- Impede que entidades de itens dropados dentro de territorios sejam transportadas por portais do Nether ou do End para fora da area reivindicada.\n- A regra se aplica a entidades de item, nao a jogadores ou mobs.\n- Depende do evento `on entity portal` do Skript (suporte a entidades desde Skript 2.5.3); requer teste em servidor Paper real.\n\n## 0.38.0 - Contencao de itens nas fronteiras\n- Impede que entidades de itens dropados atravessem para fora de territorios reivindicados.\n- A regra bloqueia movimentos de saida independentemente da causa; o evento de movimento nao identifica com seguranca o jogador que empurrou o item.\n- Requer Paper 1.16.5+ e Skript compativel; ainda necessita teste no servidor real.\n\n## 0.37.0 - Proteção ambiental de itens dropados\n- Impede que itens no chão recebam dano de fogo, queimadura, lava e explosões dentro de territórios reivindicados.\n- Ataques diretos de jogadores não são bloqueados por esta regra.\n- A proteção atua no evento de dano das entidades de item; requer validação em servidor Paper real.\n\n## 0.36.0 - Proteção de itens dropados\n- Impede que jogadores de outras guildas recolham itens do chão dentro de territórios reivindicados.\n- Membros da guilda proprietária continuam podendo recolher itens normalmente.\n- A regra se aplica ao evento de coleta de itens por jogadores; coleta por funis continua coberta pelas proteções anteriores.\n\n## 0.35.0 - Proteção contra destruição de veículos com inventário\n- Cancela dano e destruição de veículos que expõem inventário, como carrinhos com baú ou funil, dentro de territórios reivindicados.\n- Veículos sem inventário não são afetados por esta regra.\n- A proteção usa os eventos nativos vehicle damage e vehicle destroy do Skript.\n\n## 0.34.0 - Proteção de inventários móveis
- Bloqueia a abertura de inventários de entidades dentro de territórios por jogadores de outras guildas.
- Inclui carrinhos com baú e outros veículos com inventário reconhecidos pelo evento de abertura do Skript.

## 0.33.0 - Proteção contra coleta automática
- Bloqueia coleta de itens do chão por funis dentro de territórios reivindicados.
- O evento nativo do Skript também cobre carrinhos com funil.
- Mantém o bloqueio de transferências automáticas entre inventários protegidos.

## 0.32.0 - Proteção de inventários e funis
- Bloqueia transporte automático de itens quando o inventário de origem ou destino está dentro de território reivindicado.
- Corrige referências de bloco nos verificadores de explosão e pistões.
- A interação manual com baús continua protegida pelo bloqueio de clique em blocos para jogadores de fora da guilda.

## 0.31.0 - Proteção contra dispensers e droppers
- Bloqueia ativações de dispensers e droppers instalados dentro de territórios reivindicados.
- Corrige as referências aos blocos avaliados nos handlers de explosão e pistões.
- Dispensers externos apontados para dentro ainda não são bloqueados; mecanismos internos também ficam bloqueados para a guilda proprietária.

## 0.30.0 - Proteção contra pistões externos
- Eventos de extensão e retração verificam os blocos movidos por pistões.
- A checagem considera a área reivindicada e uma margem de um bloco para bloquear movimentos que alcancem a borda.
- A proteção ainda requer teste de runtime em Paper; não substitui validação de mecanismos complexos.

## 0.29.0 - Proteção contra fluxo de líquidos
- Fluxos de água e lava são cancelados quando a origem está dentro do território ou na margem externa de um bloco.
- A margem evita que um fluxo iniciado imediatamente fora atravesse a borda em uma etapa.

## 0.28.0 - Proteção contra fogo em territórios
- Eventos de ignição e propagação de fogo são cancelados dentro de territórios reivindicados.
- A proteção também impede fogo natural dentro da área; não altera dano de entidades.

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

## 0.49.0 - Pets companheiros
- Adicionados três companheiros adotáveis: lobo, gato e papagaio, cada um com função e habilidade próprias.
- 5% de chance de adoção Rara; raridade amplia a habilidade e concede resistência adicional.
- Comandos /pet, /pet adotar, chamar, guardar, status e habilidade.
- Lobos auxiliam no combate ao atacar monstros enfrentados pelo dono; abates evoluem o companheiro até o nível 10.
- Dados de espécie, raridade e evolução ficam persistidos por jogador; pets ativos são recolhidos ao desconectar.
