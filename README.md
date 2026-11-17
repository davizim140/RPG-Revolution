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
- Criação automática de personagem, perfil, níveis, XP e pontos de atributo.
- Força, defesa, agilidade e inteligência ligadas à progressão.
- Economia, transferências entre jogadores e comandos administrativos.
- Missão inicial de caça e recompensa diária.
- Quatro classes: Guerreiro, Mago, Assassino e Arqueiro.
- Habilidades ativas, mana, recarga e especializações no nível 20.
- Cadastro informativo de regiões por mundo.
- Loja de equipamentos e suprimentos com moedas do RPG.
- Encontro repetível com chefe de masmorra a partir do nível 5.
- Guildas com criação, convites, entrada, consulta e saída de membros.

## Instalação
1. Faça backup do servidor.
2. Instale Paper 26.3 e uma versão do Skript compatível com ela.
3. Instale ViaVersion se quiser aceitar clientes de outras versões.
4. Copie a pasta server/plugins/Skript/scripts/ para plugins/Skript/scripts/ no servidor.
5. Execute /sk reload all e confira o console.
6. Teste em um servidor separado antes de usar em produção.

## Comandos
- /rpgajuda, /perfil, /atributos, /upar <forca|defesa|agilidade|inteligencia>
- /classe, /classe <guerreiro|mago|assassino|arqueiro>
- /habilidades, /habilidade, /especializar
- /saldo, /pagar <jogador> <valor>
- /missoes, /resgatar, /recompensadiaria
- /rpgloja, /comprar <espada|armadura|arco|comida>
- /masmorra
- /guilda, /guilda criar <nome>, /guilda convidar <jogador>, /guilda aceitar, /guilda info, /guilda sair
- /regiao, /rpgmundos
- /rpgregiao definir <nome> <nivel-minimo> (admin; configura o mundo atual)
- /rpgxp <jogador> <quantidade> e /rpgmoedas <jogador> <saldo> (admin)

Permissão administrativa: rpg.admin.

## Limites conhecidos desta versão
- Regiões são cadastradas por mundo e exibem nível recomendado; o bloqueio de acesso por nível ainda não está implementado.
- A loja entrega itens vanilla nomeados; não há sistema de raridade, atributos próprios de item ou inventário customizado.
- O chefe é um zumbi vanilla com vida aumentada; não há arena instanciada, mecânicas especiais ou geração automática de dungeon.
- Guildas ainda não têm transferência de liderança, chat próprio, banco ou guerras.
- NPCs, HUD customizada, crafting próprio, eventos mundiais e grupos de dungeon ainda não estão implementados.

## Validação
O GitHub Actions verifica a estrutura dos arquivos, procura marcadores de placeholder e empacota a distribuição. Isso **não valida a sintaxe do Skript nem substitui o teste real de carregamento e jogabilidade** em Paper 26.3. Não use em produção antes de testar /sk reload all e os comandos em um servidor de homologação.
