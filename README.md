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
- Armas de classe: Cajado Arcano, Adaga Sombria e Arco do Batedor.
- Armaduras de classe com quatro peças e bônus de conjunto.
- Espada do Aprendiz e Couraça do Guardião aprimoráveis até +3.
- Loja, receitas, itens nomeados e raridades visuais.
- Missão inicial, linha de história e contrato diário de caça a esqueletos.
- Regiões informativas por mundo.
- Masmorra com chefe.
- Guildas com convite, transferência de liderança, expulsão, chat e banco.
- Recompensas diárias.

## Instalação
1. Faça backup do servidor.
2. Instale Paper 26.3 e uma versão do Skript compatível com ela.
3. Opcionalmente instale ViaVersion.
4. Copie server/plugins/Skript/scripts/ para plugins/Skript/scripts/.
5. Execute /sk reload all e examine o console.
6. Teste em servidor separado antes de produção.

## Comandos principais
- /rpgajuda, /perfil, /atributos, /upar <forca|defesa|agilidade|inteligencia>
- /classe, /habilidades, /habilidade, /especializar
- /saldo, /pagar <jogador> <valor>
- /missoes, /resgatar, /recompensadiaria
- /npc <guia|ferreiro|explorador>
- /missaoaceitar <madeira|zumbis>, /minhasmissoes, /missaoentregar
- /rpgloja, /comprar <espada|armadura|arco|comida>
- /rpgcraft, /fabricar <espada|armadura|arco>
- /fabricarclasse <cajado|adaga|arco>
- /fabricararmadura <capacete|peitoral|calcas|botas>
- /equipamento, /aprimorar
- /contrato, /contrato aceitar, /contrato entregar
- /masmorra
- /guilda, /guildacriar, /guildaconvidar, /guildaaceitar, /guildasair, /guildainfo
- /guildatransferir, /guildaexpulsar, /guildchat, /guildabanco, /guildasaldo
- /regiao, /rpgmundos, /rpgregiao definir
- /rpgxp, /rpgmoedas

Permissão administrativa: rpg.admin.

## Limitações conhecidas
- Itens especiais são identificados pelo nome; bigorna ou renomeação pode afetar os bônus. Ainda não há identificador persistente NBT/PDC.
- As raridades são visuais, exceto os bônus programados nos itens descritos.
- Bônus do arco de classe dependem do evento de dano e precisam ser validados com flechas no servidor.
- Armaduras de classe são identificadas por nome; conjunto Guerreiro reduz dano, Mago e Assassino aumentam dano corpo a corpo, Arqueiro recebe velocidade.
- NPCs da história são diálogos por comando, não entidades físicas com skin.
- Regiões ainda não bloqueiam entrada por nível.
- A masmorra ainda é um encontro simples com criatura vanilla, sem arena instanciada ou mecânicas complexas.
- Guildas ainda não têm guerras, cargos ou sistema de níveis.
- Não há HUD customizada, mapa próprio ou eventos mundiais.

## Validação
O GitHub Actions faz verificações estruturais e empacota ZIP. Isso não comprova sintaxe Skript nem execução em Paper 26.3. É obrigatório testar /sk reload all e os sistemas em um servidor de homologação antes de produção.
