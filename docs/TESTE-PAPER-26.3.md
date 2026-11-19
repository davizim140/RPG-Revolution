# Plano de teste — RPG Revolution / Paper 26.3

## Quando testar
**Agora, antes de adicionar mais sistemas.** Esta etapa valida carregamento, comandos e recompensas em um servidor de homologação. Não use o servidor principal nem dados importantes.

## Preparação
1. Crie uma cópia/servidor separado de Paper 26.3.
2. Instale uma versão do Skript compatível com essa versão do Paper.
3. Faça backup da pasta `plugins/Skript/` e do mundo.
4. Copie o conteúdo de `server/plugins/Skript/scripts/` do repositório para `plugins/Skript/scripts/`.
5. Inicie o servidor e execute `/sk reload all`.

## Critério inicial de aprovação
- O console não pode mostrar erros de parsing ou scripts desativados.
- Execute `/rpgajuda`, `/perfil` e `/pontostemporada` para confirmar que os comandos carregaram.
- Se houver qualquer erro no reload, pare o teste e envie o trecho completo do console; não continue para recompensas.

## Teste de temporada manual
1. Com uma conta OP/admin, execute `/rpgtemporada iniciar TESTE`.
2. Execute `/rpgtemporadaauto status`; deve informar rotação automática desativada.
3. Derrote criaturas com um jogador de teste. Cada abate válido deve somar 5 pontos.
4. Consulte `/pontostemporada` e `/rankingtemporada`.
5. Encerre com `/rpgtemporada encerrar`.
6. O jogador com maior pontuação registrada deve ser anunciado como campeão, mesmo que esteja offline no momento do encerramento, desde que tenha pontuado durante a temporada.
7. Entre com o jogador e execute `/recompensatemporada`. Confirme o crédito de moedas/XP e que um segundo resgate não duplica a recompensa.

## Teste de rotação automática
1. Use uma temporada de teste com `/rpgtemporadaauto iniciar 1`.
2. Confirme com `/rpgtemporadaauto status` que a data final foi gravada.
3. Para validar o encerramento automático completo, mantenha o servidor ligado até o prazo expirar. O verificador roda a cada minuto.
4. Confirme que a temporada antiga foi encerrada uma única vez e que a próxima foi iniciada.
5. Para interromper a rotação após o teste, execute `/rpgtemporadaauto parar`.

## Limites desta validação
- O GitHub Actions só verifica estrutura/empacotamento; não executa Paper nem interpreta Skript.
- A rotação automática depende do relógio do sistema do servidor.
- O teste de prazo real de um dia não é instantâneo; não altere variáveis internas manualmente em produção.
- Só considere o sistema aprovado depois de conferir o console e os resultados dentro do servidor.
