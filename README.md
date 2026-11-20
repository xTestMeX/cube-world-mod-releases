# Cube World Mod — launcher e atualizações

Mod comunitário para **Cube World Alpha de 23/07/2013**, com launcher **Windows x64** e **Linux x64 AppImage**. Port Vulkan separado e não incluído.

## Descarregar

Versão pública experimental atual: **0.37.0-coop.preview.53**, launcher **0.2.52**.

- [Windows x64 — launcher EXE](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.53/CubeWorldMod-Windows-x64.exe)
- [Linux x64 — AppImage](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.53/CubeWorldMod-Linux-x64.AppImage)
- [Notas, pacotes e ficheiros de verificação](https://github.com/xTestMeX/cube-world-mod-releases/releases/tag/0.37.0-coop.preview.53)

Cada pessoa precisa da sua própria instalação compatível do jogo. O download **não inclui Cube.exe, Server.exe, bases de dados originais ou saves**. O launcher verifica os executáveis antes de preparar uma cópia isolada. As DLLs do mod continuam x86, como exige o jogo original.

## Carregamento de estruturas — preview.53

O cliente cooperativo reutiliza a planta compilada dos edifícios e inclui a correção da espera na grelha de desenho da preview.52. Quem já tem o launcher pode fechar o jogo e o servidor e escolher **Procurar atualizações**. O anfitrião e os convidados devem usar a mesma versão.

## Verificação antecipada das estruturas — preview.51

A verificação antecipada dos blocos fica ativa por defeito em cooperativo. Quem já tem o launcher pode fechar o jogo e o servidor e escolher **Procurar atualizações**. Tanto o anfitrião como os convidados devem atualizar para a mesma versão.

## Chegada às estruturas — preview.49

O cliente dá prioridade aos edifícios próximos e pede a decoração durante a aproximação. O anfitrião envia os blocos quando o terreno do cliente já os pode receber. Nos chunks intactos, o terreno original pode continuar visível enquanto o edifício é preparado.

Com o jogo e o servidor fechados, abre o launcher ou escolhe **Procurar atualizações**. Atualiza o anfitrião e os convidados para o mod **preview.49** e o launcher **0.2.48**. Podes usar o mesmo mundo. O tempo de carregamento ainda será medido em jogo.

## Estruturas em cooperativo e Armadilha de Caça na preview.48

Os edifícios do mod começam a ser preparados durante a aproximação. O cliente apresenta o edifício em conjunto e verifica o chão, a decoração e os habitantes esperados antes de permitir a entrada. A meta dos 100 ms após o terreno ficar visível aguarda medição em jogo.

A Armadilha de Caça do Scout deteta inimigos que atravessem o gatilho entre duas leituras, em solo e no cooperativo. Pode ficar no chão até seis segundos e imobilizar até três inimigos durante dois segundos.

Fecha o jogo e o servidor e escolhe **Procurar atualizações**. O anfitrião e os convidados devem usar o mod **preview.48** e o launcher **0.2.47**.

## Carregamento das estruturas — preview.47

O cliente verifica os blocos da revisão recebida antes de apresentar a estrutura em conjunto. Se a zona sair da memória antes de a construção terminar, o servidor retoma o trabalho a partir das edições guardadas. A Armadilha de Caça do Scout assenta no chão e fica armada durante seis segundos ou até disparar.

Fecha o jogo e o servidor e escolhe **Procurar atualizações** no launcher. No cooperativo, atualizem o anfitrião e os convidados para a preview.47. A velocidade de aparecimento dos edifícios continua por medir em jogo.

## Escolta e saque partilhado — preview.39

O dono da escolta pode abandoná-la no Diário. Os baús das estruturas largam 2 a 5 itens aleatórios no chão, num único saque por ciclo para todo o grupo. O prisioneiro fica protegido enquanto está preso. O piso da jaula foi ajustado e o servidor responde à interação já com o estado atualizado da porta.

Para atualizar, fecha o jogo e o servidor e escolhe **Procurar atualizações** no launcher. Confirma que tens o launcher **0.2.38** e o mod **preview.39**. Podes voltar ao mesmo mundo.

## Carregamento dos acampamentos — preview.38

Corrige a recusa do modelo da porta da jaula, que podia deixar um acampamento preso em «Local em preparação». O modelo da porta torna a carregar em solo e em cooperativo, com o mesmo limite de memória por modelo.

Os testes com as DLLs distribuídas confirmaram a construção das cinco malhas da jaula. A verificação visual no local afetado continua pendente.

## Jaula, baús e preparação dos locais — preview.37

Corrige o desaparecimento da jaula após Alt+Tab: locais já publicados conservam a prontidão durante o reset gráfico. Pedidos repetidos ou atrasados deixam de rebaixar uma estrutura pronta e de voltar a ativar a proteção que podia expulsar o jogador.

A porta tem eixo e encaixe corrigidos e abre para fora. O prisioneiro fica ancorado e protegido, sem combater, até ser libertado. No cooperativo, **R** permite fechar/reabrir baús já saqueados e a porta libertada, sem duplicar recompensas. Mantém-se **um saque partilhado por baú/ciclo**, entregue diretamente no inventário, com aviso de cada arma no chat. Sem HUD de XP/moedas. A fogueira de um acampamento limpo deixa de oferecer outras missões.

**Atualizar:** anfitrião e convidados fecham jogo e servidor, usam **Procurar atualizações** e deixam o launcher reiniciar. Confirmem **launcher 0.2.36 / mod preview.37** antes de voltar à sessão. Não exige mundo nem perfil novos. Configurações e saves preservados.

Testes curtos de publicação/Alt+Tab, IA, renderer/matrizes x86, quatro orientações, layouts, saque único, fechar/reabrir e falhas de gravação passaram, com builds Windows/Linux, .NET/TLS/UI, assinatura Ed25519 e hashes. Não foi aberto Cube.exe/Server.exe. **Aspeto GPU e gameplay real Windows/Proton precisam de confirmação dos jogadores.** Não se promete eliminar todo o lag: o status inclui métricas leves para investigar se voltar a bloquear.

Render distance: opções acima de 100% funcionam nas verificações, mas o detalhe no cooperativo continua limitado pela configuração **TerrainReach=768**. Este update não aumenta a carga do terreno nem as taxas de rede.

## Jaula física e revisão do mod — preview.36

A jaula dos prisioneiros passa a ser **mobiliário físico em madeira e ferro**, com modelos voxel próprios, interior oco, colisões e porta animada. Elimina os guardas e usa **R** para libertar o prisioneiro e aceitar a escolta; a porta só abre depois de guardar o resgate. O servidor confirma o estado para os convidados. Reabrir o mundo ou renovar o acampamento não duplica peças; mantém os índices dos baús, ciclos e recibos. Jaulas antigas reconhecidas são convertidas no mesmo local.

Inclui a revisão transversal preparada anteriormente: correções de efeitos/dano cooperativo das classes e de precisão de coordenadas, isolamento dos acampamentos por mundo, patrulhas, suporte/terreno em novos altares, ruínas e torres, conclusão de escoltas e espera pela chegada do grupo entre rondas. O launcher recupera reparações interrompidas, preservando configurações e versões anteriores.

**Atualizar:** anfitrião e convidados fecham jogo e servidor, usam **Procurar atualizações** e deixam o launcher reiniciar. Confirmem **launcher 0.2.35 / mod preview.36** antes da sessão nova. Não exige outro mundo ou perfil. Configurações e saves mantidos; o port Vulkan permanece separado.

Testes curtos das instruções originais de colisão/gravação, quatro orientações da porta, prefixos de objetos, resgate, reabertura e 192 layouts passaram, juntamente com compilações Windows/Linux, testes .NET/TLS/UI, assinatura Ed25519 e hashes. Nenhum Cube.exe/Server.exe foi aberto. **A confirmação visual da jaula e a saída do prisioneiro em gameplay Windows/Proton continuam a depender dos jogadores.**

## Correção de classes e skills — preview.34

Corrige respostas de estruturas que podiam sobrescrever o estado de combate, ranks e party, e a captura de entrada que apagava IDs de habilidades nativas. Necromante e Vampiro passam a usar a identidade confirmada por ator/UUID; o anfitrião recupera a classe especial já aceite, conservando ranks, passivas e revisões, sem permitir trocar de personagem/classe. O desenho consulta apenas uma cópia limitada do estado, sem pedidos adicionais de rede ou espera no worker.

**Atualizar:** anfitrião e convidados fecham jogo/servidor, procuram atualizações e deixam o launcher reiniciar. Confirmem **launcher 0.2.33 / mod preview.34** antes de criar uma sessão nova no mesmo mundo. Não exige outro mundo ou perfil. Configurações, equilíbrio e cadência de rede mantidos.

Os testes curtos antes/depois reproduzem as falhas do worker, assinaturas de classe e tecla 1; incluem quatro atores/seis classes, recuperação de UUID/ranks, F6/Fechar, voo/descida, suite .NET/TLS/UI, builds x86 e pacotes assinados. Nenhum Cube.exe/Server.exe foi aberto. **A confirmação real de skills e aparência entre jogadores em Windows/Proton continua pendente.**

## Correção do arranque cooperativo — preview.33

Corrige as validações do servidor que usavam endereços absolutos da base preferida e rejeitavam o executável quando relocava (ASLR). Mantém o hash completo, os opcodes e operandos exatos. O launcher só aceita o estado da instância atual, com as portas esperadas; ficheiros antigos ou parciais deixam de autorizar a entrada. Falhas de ligação ao nativo recebem uma recusa clara, em vez de «Unable to read beyond the end of the stream», e novos registos identificam a fase de arranque.

**Atualizar:** anfitrião e convidados fecham jogo/servidor, procuram atualizações, deixam o launcher reiniciar e confirmam **launcher 0.2.32 / mod preview.33** antes de criar uma sessão nova no mesmo mundo. Não exige outro mundo ou perfil. Configurações, saves, conteúdo e intervalos de rede/geração mantidos.

Testes curtos com o export real da DLL sobre dados PE relocados, configuração ativa copiada e instruções corrompidas; handshake TLS, estados antigos/parciais, portas divergentes e libertação de slots; builds dos dois launchers, interface headless, assinaturas Ed25519 e hashes verificados. **Nenhum Cube.exe/Server.exe foi aberto pelo agente.** Os registos antigos não identificam a fase interna/base: não demonstram que ASLR foi a causa daquela execução específica. O arranque real desta correção continua a precisar de confirmação dos jogadores.

## Edifícios completos e carregamento coordenado — preview.32

Prepara as malhas das estruturas separadamente e publica o conjunto entre frames, incluindo locais que partilham chunks. Verifica os blocos efetivamente recebidos, decoração e habitantes esperados; os NPCs conservam a ativação por proximidade. A entrada no local e o combate são coordenados com a confirmação de cada jogador.

Antecipa pesquisa e replay em zonas carregadas e apresenta a fase de preparação ao chegar diretamente a um edifício incompleto. Revalida após reentrada, religação e reset gráfico; ranks/passivas não reiniciam o cenário. O levantamento do terreno evita cópias de memória por voxel e aplica pausa adaptativa, mantendo os limites de edição/replay.

**Atualizar:** anfitrião e convidados fecham jogo e servidor, procuram atualizações, deixam o launcher reiniciar e confirmam **launcher 0.2.31 / mod preview.32** antes de criar uma sessão nova. Não exige um mundo novo. Configurações, saves, recompensas e regras das expedições conservados.

Compilações, testes curtos x86 de publicação/ownership/reset/colunas/religação/quatro jogadores, testes .NET, interface headless, assinaturas Ed25519 e hashes verificados. Nenhum Cube.exe/Server.exe foi aberto pelo agente. **O aspeto, IA e desempenho reais continuam por confirmar pelos jogadores.** Esta versão conserva o replay nativo; não promete criação instantânea nem aceleração de 10×.

## Necromante, relíquia e HUDs — preview.31

Corrige o clique de **F6 → Fechar** que escapava para ataques nativos do Mage. O **Cajado Ossário** passa a usar a transformação da mão no desenho, sem provocar um ataque nativo. O M1 ganha a aquisição em falta de inimigos e objetos destrutíveis baixos, verifica linha de visão e atualiza o **contador de combo nativo** apenas quando causa dano.

Convidados podem recolher a relíquia através da validação automática do servidor: a oferta e o pedido passam a comparar a mesma identidade pública do local. Guardas, distância, gravação e proteção contra duplicações continuam obrigatórios.

Os baús entregam as **armas aleatórias sem o HUD de 0 XP/0 cobre**. Os atributos gerados pelo jogo são preservados, incluindo nas variantes novas. Corrige o apoio de baús, barris e caixas nas ruínas, conservando índices, estados, ciclos e recibos. Inimigos das estruturas usam o poder nativo **+1/+2**; bosses recebem +2.

Os indicadores **R** dos altares/baús mostram os estados disponível, protegido ou já usado. O marcador do prisioneiro acompanha a matriz desenhada em cada frame, conservando o movimento fracionário mesmo com a precisão do D3D9. Mantém o fundo preto a 75% e os intervalos de rede existentes.

**Atualizar:** anfitrião e convidados fecham o jogo e o servidor, usam **Procurar atualizações**, deixam o launcher reiniciar e confirmam **launcher 0.2.30 / mod preview.31** antes de criar uma sessão nova. Não é necessário um mundo novo. Mantém arena reutilizável, rondas contínuas, contagem inicial de dez segundos e cooldown individual de 45 minutos.

Testes curtos de produção, instruções x86, desenho headless, recibos/rollback, loot, religação e rondas passaram. Ambos launchers foram compilados; manifestos Ed25519 e hashes verificados. Nenhum Cube.exe/Server.exe foi aberto pelo agente. **A confirmação visual e de gameplay entre computadores continua a depender dos jogadores.**

## Guardas, armas e correções cooperativas — preview.30

As torres recebem quatro guardas humanos distribuídos pelos pisos e o baú fica protegido até derrotá-los. Inclui torres existentes no cooperativo; em solo aplica-se às torres geradas após atualizar. O Guardião das Ruínas recebe correções de chão/spawn, libertação de slots de encontros antigos e loot pelo percurso nativo de boss.

Corrige duplicação contínua dos prémios de expedição, cliques de venda/largar itens e armas iniciais no Necromante e regresso dos participantes mortos ao descanso após os companheiros completarem a ronda. Baús de acampamentos, ruínas e torres usam **R**, com validação e recibos independentes; os prisioneiros têm indicador e interação de resgate/escolta. A relíquia de missão usa a sua posição física real, incluindo convidados e contratos já aceites. Diário/ofertas recebem prioridade sem aumentar a frequência global de rede.

O M1 do Necromante exige o **Cajado Ossário em mão**, atinge recursos/objetos destrutíveis nativos e apresenta números de dano confirmado. M2 deixa de usar o efeito incorreto de Maldição. A vida dos esqueletos, guardião e exército desce **45%**, preservando o escalamento por pontos. O M1 da **Lâmina Sanguínea perde 30% do dano**; Garras e Cyclone mantêm-se.

As sete armas especiais participam nos drops nativos e no stock das lojas, preservando os atributos, nível, qualidade e upgrades nativos. Reabrir a loja não rerola o stock. Os **preços de compra nos NPCs duplicam**, mantendo o valor de venda do jogador e o crafting.

O launcher **0.2.29** reinicia automaticamente após uma atualização verificada, com jogo/servidor fechados. Quem atualizar a partir do launcher 0.2.28 deve **fechar/reabrir manualmente uma vez** para carregar o novo launcher. Anfitrião e convidados devem usar preview.30 e iniciar uma sessão nova. Mantém as correções anteriores de terreno, rede e expedições.

Compilações e testes curtos dirigidos, interface headless, assinaturas Ed25519 e hashes passaram. **A confirmação real em Windows/Proton e entre computadores continua a depender dos jogadores.** Nenhum Cube.exe/Server.exe foi aberto pelo agente. Itens já duplicados não são apagados automaticamente, pois podem coincidir com exemplares legítimos. Recuar os recibos dos baús requer o backup do mundo correspondente.

## Vampiro, Necromante e intervalo das expedições — preview.29

O Vampiro recebe **20% de velocidade adicional enquanto flutua/voa** e a **cura da Explosão de Sangue é reduzida em 50%**, incluindo os pontos. Armas normais do Rogue e Presa da Noite são rejeitadas antes de equipar; mantém Garras Carmesim e Lâmina Sanguínea. Armas incompatíveis já equipadas voltam à mochila, com bloqueio dos ataques enquanto essa devolução estiver pendente. O Necromante precisa do primeiro ponto no respetivo nó da árvore X, seguido de Apply, para cada uma das quatro skills. M1/M2 e pontos existentes são conservados; o servidor valida os desbloqueios.

As expedições cooperativas têm **45 minutos de cooldown individual ao terminar/sair**, contando apenas o tempo ligado ao servidor. O registo é persistente por personagem no anfitrião e partilhado entre os seus mundos; anfitriões diferentes têm registos próprios. F6 mostra o tempo restante. Saídas repetidas, fechar o jogo ou reiniciar o servidor não permitem contornar o intervalo. Convites/lobby cancelados e preparações falhadas antes do início não gastam o intervalo. A derrota que termina a participação conta como saída; a espera temporária por companheiros mantém as regras anteriores.

Mantém os limites e frequências da rede/terreno, contagem inicial de dez segundos, rondas contínuas, arena reutilizável e correção das hornets. Testes curtos de regras, persistência, falhas de gravação, ligação/reabertura, interceções x86 e interface headless passaram. **O comportamento real em jogo continua por confirmar.** Nenhum Cube.exe/Server.exe foi aberto pelo agente.

Inclui launcher **0.2.28**, Windows x64 e Linux x64 AppImage. Anfitrião e convidados fecham jogo/servidor, procuram atualizações, fecham/reabrem o launcher e iniciam uma nova sessão na **preview.29**. Teste curto: voar/aterrar e tentar uma arma Rogue; investir um ponto no Necromante; sair de uma expedição, observar F6, desligar e regressar para confirmar a pausa do cooldown.

## Hornets que ficavam paradas — preview.28

Corrige três hornets de cada vaga de seis que recebiam arcos, ativando a distância de paragem de arqueiro do motor apesar de a espécie atacar de perto. Todas passam a usar o perfil de combate próximo dos três exemplares que já funcionavam. Arqueiros humanoides e cultistas mantêm o comportamento à distância. Preserva a contagem inicial de 10 segundos, teleporte, rondas contínuas e limites de rede; sem novos hooks nem aumento da frequência de consultas ou envio de terreno.

A receita real de spawn e as instruções originais do Server.exe reproduziram exatamente três hornets com alcance de arqueiro antes da correção e zero depois. Testes curtos de rondas, contagem inicial e religação, assinaturas nativas, builds Windows/Linux e interface headless passaram. DLLs cliente, auxiliares de rede e INIs preservados por hash. **A perseguição e os ataques completos em jogo ainda precisam de confirmação dos jogadores.** Nenhum Cube.exe/Server.exe foi aberto pelo agente.

Inclui launcher **0.2.27**, Windows x64 e Linux x64 AppImage. Todos fecham jogo e servidor, procuram atualizações, fecham/reabrem o launcher e criam uma sessão nova no mesmo mundo, com anfitrião e convidados na **preview.28**. Teste curto: numa vaga de hornets, permanecer a 15–25 blocos para verificar que as seis avançam; recuar dentro da sala e confirmar a perseguição.

## Contagem inicial das expedições — preview.27

A primeira ronda começa **10 segundos depois da chegada confirmada de todos os participantes**. O chat apresenta **10, 9…1** e anuncia o início. Funciona em solo e cooperativo; as rondas 2–10 continuam na mesma sala, sem repetir este atraso ou carregar novamente. O limite de transferência de 90 segundos é independente da contagem.

Mantém a correção de terreno/teleporte da preview.26, cujo funcionamento foi entretanto confirmado pelo utilizador. Configurações, saves e limites de rede preservados. Testes curtos de solo, servidor, cliente/chat, cancelamento, religação, rondas contínuas, builds, emulação dos hooks e interface headless passaram. **A confirmação visual da nova contagem no jogo continua pendente.** Nenhum Cube.exe/Server.exe foi aberto pelo agente.

Inclui launcher **0.2.26**, Windows x64 e Linux x64 AppImage. Todos devem fechar jogo e servidor, atualizar, fechar/reabrir o launcher e criar uma sessão nova no mesmo mundo. Anfitrião e convidados devem usar **preview.27**. Teste curto: observar a contagem antes dos inimigos, concluir a primeira ronda e continuar para a segunda sem repetir a contagem.

## Terreno 9/9 sem teleporte — preview.26

Corrige a sonda de chegada que comparava os valores RGB dos blocos de ar. Esses valores representam iluminação local e podem diferir entre servidor e cliente, mesmo com o mesmo chão e espaço livre. A diferença foi observada por leitura autorizada de uma sessão existente e reproduzida com o código compilado: a DLL anterior rejeita os mesmos dados e a corrigida aceita-os.

A sonda continua a comparar o tipo de todos os blocos, a cor dos sólidos, o chão, a altura, as colunas carregadas e o espaço livre. Apenas deixa de exigir iluminação RGB igual no ar. **Não é necessário criar outro mundo nem apagar a arena guardada.** Não altera o servidor, os limites de rede ou os saves.

Inclui Windows x64 e Linux x64 AppImage, launcher **0.2.25**. Todos devem fechar jogo e servidor, atualizar, fechar/reabrir o launcher e criar uma sessão nova no mesmo mundo. Anfitrião e convidados devem usar **preview.26**. Testar entrada, primeira ronda, passagem à segunda, extração e outra entrada.

Testes dirigidos antes/depois com os mesmos bytes observados, verificações negativas de chão/espaço ocupado, builds, interface headless, assinaturas e hashes passaram. Não foi iniciado Cube.exe/Server.exe nem se escreveu na memória ou nos saves da sessão observada. **O teste real da nova versão continua pendente.** As otimizações anteriores mantêm-se; não há uma medição de carregamento total 10× mais rápido.

## Chegada, recuperação e carregamento — preview.25

Corrige a validação gráfica que rejeitava parcelas concluídas com lista opaca vazia. Mantém as verificações de chão, sondas, coordenadas XYZ, parcela atual e construção terminada. Ao perder a ligação ou terminar o regresso, limpa a reserva e o estado local da transferência. Uma nova tentativa prefere uma arena guardada livre a um slot vazio; o contador de preparação mostra o progresso atual do anfitrião em vez do 9/9 da tentativa anterior.

A verificação local da transferência passa de 1000 para 100 ms. O estado de entrada recebe prioridade alternada com as restantes consultas, e os reenvios são limitados. Os orçamentos de construção e envio de blocos mantêm-se. **Não é uma medição de carregamento total 10× mais rápido**; os tempos e FPS reais continuam por medir.

Testes antes/depois com instruções nativas de publicação gráfica, regresso após tempo limite, religação, nova tentativa, preferência de cache, contador e consultas passaram. IPC Windows x86 e interface headless verificados; ambos launchers compilados, manifestos assinados e hashes conferidos. Nenhum Cube.exe/Server.exe aberto. **A correção ainda precisa de confirmação real em jogo.**

Todos devem fechar jogo e servidor, atualizar, fechar/reabrir o launcher e confirmar **launcher 0.2.24 / mod preview.25**. O anfitrião cria uma sessão nova, com todos os convidados atualizados. Testar entrada, ronda 2, extração e nova tentativa. Se ocorrer novo limite, testar regresso e nova entrada sem reiniciar o servidor; `classes-alpha.log` inclui agora a etapa exata da espera.

## Rondas contínuas e arena reutilizável — preview.24

As dez rondas decorrem no mesmo salão. **Continuar** avança diretamente para a próxima vaga, mantendo posição e confirmação do cenário, sem novo teleporte ou preparação. Bosses continuam nas rondas 5 e 10; a extração individual e o saque em risco mantêm-se.

A arena cooperativa fica guardada por mundo e slot, até quatro arenas. Depois da primeira construção confirmada, as tentativas seguintes reutilizam a geometria e as coordenadas, incluindo após reabrir o servidor. Os inimigos, tentativas e recibos de prémios continuam independentes. Quando todos saem, liberta a grelha de construção e a reserva de carregamento; as zonas podem sair da memória.

A gravação do terreno e do marcador reutilizável ocorre na mesma transação. Construções parciais e registos antigos sem confirmação seguem a limpeza anterior: a primeira entrada após atualizar pode construir uma vez. A entrada/religação continua a carregar e validar zonas; entre rondas deixa de o fazer. O destino reutilizado fica fixo no mundo, aproximadamente 10 000 blocos da primeira origem, podendo ficar mais longe de outra cidade.

Testes curtos das dez rondas solo/cooperativas, votos, morte/desligação, extração, reutilização sem novas edições, reabertura e falhas transacionais passaram. Ambos launchers compilados e pacotes assinados verificados. Nenhum Cube.exe/Server.exe aberto. O utilizador confirmou o teleporte e primeira ronda da preview.23; **esta mudança ainda precisa de confirmação real em jogo**, sem medições de FPS.

Todos fecham jogo/servidor, atualizam e fecham/reabrem o launcher. Confirmar launcher **0.2.23** e mod **preview.24**, criar sessão nova, passar da ronda 1 para a 2 sem carregar, extrair e iniciar outra tentativa. Repetir uma entrada após reabrir o servidor.

### Correções mantidas da preview.23

Corrige a ordem dos bloqueios na descarga das zonas antigas após o teleporte: o worker podia segurar Terrain e esperar World, enquanto o thread principal segurava World e esperava Terrain. O percurso foi reproduzido nas instruções do executável, a partir dos registos de bloqueio da preview.22. A alteração mantém a remoção/destruição nativas e os escopos originais dos bloqueios.

A zona vazia da barra de título do launcher passa a receber o arrasto. O texto/ícone, duplo clique e botões de minimizar/maximizar/fechar foram verificados por eventos de interface em ambiente headless. Mantém os contadores de 90 segundos por fase e o destino de cerca de 10 000 blocos.

Testes isolados de espera circular, rollback, zonas/regiões, transferência/regresso, dez etapas, recompensas, snapshot/religação e interface passaram. Ambos launchers compilados e pacotes assinados verificados. Não foi aberto Cube.exe/Server.exe pelo agente; o utilizador confirmou posteriormente a entrada e primeira ronda da preview.23. O movimento nativo da janela continua por confirmar.

Se voltar a bloquear, aguardar 8–10 segundos antes de fechar e fornecer `native-run.log`, `native-fault.log` e `classes-alpha.log` da pasta do perfil.

### Correções mantidas da preview.22

A validação de terreno evita cópias de memória repetidas por tile, e os bloqueios adicionais do mesher são libertados antes da fase gráfica. O HUD cooperativo mostra idade sincronizada com o anfitrião e limite de **90 segundos por fase** para preparação e carregamento/validação da chegada. Diagnóstico adicional recolhe threads, memória virtual e exceções perante bloqueios. Configurações e saves preservados.

## Destino das expedições — preview.20

As expedições cooperativas passam a cerca de **10 000 blocos de distância horizontal**, com o chão quatro blocos acima do sólido mais alto no local. A altura do jogador deixa de elevar a arena em 500 metros. O alinhamento à zona e a entrada de cada sala fazem variar ligeiramente a distância.

À data da preview.20, mantinha as dez etapas, cenário, recompensas, remoção e regresso. A preview.24 passa a conservar a arena e a realizar as rondas no mesmo salão. Os quatro slots preferem direções distintas; os journals antigos conservam as coordenadas anteriores para limpeza. As otimizações da preview.19 continuam ativas. A alteração aplica-se ao servidor cooperativo; o percurso solo é independente.

Testes curtos de distância, terreno elevado, limites do mundo, destinos simultâneos, regresso, falhas e limpeza antiga passaram, além das compilações e verificações Windows/Linux. Nenhum Cube.exe/Server.exe foi aberto. **A melhoria real de FPS ainda precisa de confirmação**, incluindo possíveis picos no carregamento do destino.

Todos fecham jogo/servidor, atualizam e fecham/reabrem o launcher. Criar sessão nova, iniciar uma expedição F6 e testar movimentação/inventário durante preparação, entrada e extração.

## Construção de expedições — preview.19

A preview.19 constrói as colunas do topo para baixo e agrupa o envio por zonas gráficas. Na receita completa, reduz as expansões de memória de 452 470 para 31 684, conservando geometria, dimensões e decoração. Estes números medem trabalho redundante, não FPS nem RAM simultânea.

O cliente agrupa rajadas de alterações antes de reconstruir geometria e iluminação. Colisões e rede continuam imediatas; a confirmação de chegada exige a malha atualizada. Mantém os limites de envio e as melhorias de latência anteriores.

Testes curtos, builds Windows/Linux, interface headless, assinaturas e hashes passaram sem abrir Cube.exe/Server.exe. **Os FPS reais continuam por confirmar**; uma reconstrução individual de iluminação em colunas altas ainda pode causar uma pausa.

Para atualizar, todos fecham jogo e servidor, usam **Procurar atualizações** e fecham/reabrem o launcher. O anfitrião inicia uma sessão nova. Testar movimentação e abertura do inventário durante a preparação da expedição.

## Alt+Tab Windows e recuperação de expedições

A preview.18 adia a reposição gráfica enquanto o jogo está minimizado ou o dispositivo está perdido, evitando o percurso de bloqueio identificado em fullscreen. Os uploads de terreno distante mantêm a malha anterior e voltam a tentar após falha.

Ao religar depois de um teleporte interrompido, reinicia a confirmação da deslocação por ligação. A chegada exige proximidade XYZ; o painel distingue «A regressar ao mundo» de preparar uma expedição e de esperar pelos restantes participantes. Preserva prémios confirmados e o formato dos saves.

Testes isolados de dispositivo perdido/restauro, religação, prémios, builds e UI headless passaram sem abrir Cube.exe/Server.exe. **A confirmação real do Alt+Tab no Windows continua pendente.** Mantém as melhorias anteriores de latência e os limites de trabalho. Todos devem fechar jogo/servidor, atualizar e fechar/reabrir o launcher antes de criar uma nova sessão.

## Expedições próximas e desempenho

Até à preview.19, a preview.17 colocava a arena cooperativa na zona próxima do organizador, pelo menos **500 metros acima da entrada**, em vez de teleportar para milhões de metros. Mantém as dez salas e a decoração. A limpeza espera pelo regresso dos jogadores; um journal permite retomar a remoção após interrupção. A implementação solo anterior mantém-se separada.

A compactação seletiva do histórico impede acumular repetidamente as mesmas ações de construção/remoção. Preserva alterações alheias e mantém a sincronização limitada a 1024 ações por jogador/tick. O arranque Windows foi confirmado pelo utilizador na preview.16 e as respetivas correções mantêm-se.

Para o terreno distante, acima de 100% de distância, reduz picos de trabalho: máximo quatro uploads de malhas por tick, orçamento suave de 2 ms e provas de memória apenas quando há trabalho. Não reduz o detalhe escolhido. **O ganho real de FPS no Windows ainda não foi medido.** A arena elevada aumenta a memória das colunas nativas; apagar os blocos não devolve imediatamente toda essa capacidade.

Testes curtos de ciclo, gravação falhada, crash, quatro repetições do histórico e replay grande passaram; compilação Windows/Linux e 22 assinaturas nativas verificadas. Não foi aberto Cube.exe/Server.exe. Desenho, navegação e desempenho reais precisam da confirmação dos jogadores.

Fecha jogo/servidor, atualiza todos os participantes e fecha/reabre o launcher. Cria uma sessão nova, inicia uma expedição F6, extrai ambos e repete uma vez para confirmar a remoção e reutilização.

## Instalação

1. Descarrega o launcher para o teu sistema. No Linux, permite a execução da AppImage nas propriedades do ficheiro (ou usa `chmod +x CubeWorldMod-Linux-x64.AppImage`).
2. Abre o launcher e, em **Configuração**, seleciona a pasta do jogo que contém `Cube.exe`, `Server.exe` e os dados originais. No Linux, instala a Steam e o Proton Experimental; o launcher também permite escolher outro Proton.
3. Cria um perfil solo ou cooperativo. Os personagens são criados dentro do jogo. Perfis, saves e configurações são separados da instalação original.
4. Usa **Jogar solo**, **Criar sessão** ou **Entrar com convite**, conforme o caso.

O launcher inclui runtime .NET e o mod; não é necessário instalar .NET separadamente.

## Apagar perfis

No separador **Jogar**, seleciona o perfil e clica em **Apagar perfil**. Confirma apenas se pretendes remover definitivamente todos os personagens, progressão, configurações e mundos solo desse perfil. Cancelar ou fechar a confirmação conserva tudo. A remoção fica bloqueada enquanto o jogo/servidor estiver em utilização. Os outros perfis, mundos do servidor e instalação original são preservados.

## Cooperativo experimental

Até **quatro jogadores**, incluindo o anfitrião. Todos devem usar a mesma versão do pacote.

- Anfitrião: seleciona um mundo, coloca o IP público/DNS no campo de convite, cria a sessão e partilha o convite `cwmod://...` em privado.
- Amigos: selecionam um perfil cooperativo e usam **Entrar com convite**.
- Dentro do jogo: **Connect to server → 127.0.0.1**, tanto no anfitrião como nos convidados. Este endereço liga o jogo à ponte local do launcher; o IP público pertence ao convite.
- Para ligação direta pela Internet, o anfitrião encaminha **TCP 12345** para o IP local do seu PC. Em CGNAT poderá ser necessária uma rede privada virtual ou outro anfitrião acessível. Não abras a porta nativa diretamente.
- Mantém launcher e servidor em execução durante a sessão. O convite contém uma credencial; partilha-o apenas com os participantes.

Inclui as seis classes, skills e conteúdo de missões/estruturas/expedições integrado no mod clássico. **É uma pré-versão, não uma versão estável.** Compilação e testes simulados não provam que todo o conteúdo funciona numa sessão real Windows/Linux. O autor confirmou melhorias de latência na sua sessão; a confirmação completa entre amigos permanece pendente. `CoopReady=false` continua explícito.

## Próximas atualizações

O launcher verifica automaticamente o canal público ao abrir. Também podes usar **Procurar atualizações**; fecha primeiro o jogo e o servidor. Os updates só ficam disponíveis quando o autor publica uma nova versão.

Canal atual: [manifesto experimental assinado](https://raw.githubusercontent.com/xTestMeX/cube-world-mod-releases/main/channels/preview.json). A assinatura Ed25519 autentica o manifesto, e SHA-256 verifica cada ficheiro. Configurações e saves permanecem fora das pastas de versões. O launcher conserva a versão anterior e, a partir da versão 0.2.29, substitui-se e reinicia automaticamente após a atualização verificada. Um launcher anterior precisa de ser fechado e reaberto manualmente uma vez.

Se usas um launcher local anterior a **0.2.11**, descarrega esta AppImage/EXE uma vez. O novo launcher migra o antigo endereço oficial de atualização; endereços personalizados são preservados.

## Fontes e dependências

Cada release inclui os fontes correspondentes do mod/launcher, `SHA256SUMS` e avisos/licenças de terceiros. Apenas ficheiros próprios e dependências redistribuíveis são publicados. O jogo original, os mundos, os personagens, convites e chaves privadas de publicação não são distribuídos.

Projeto comunitário não oficial, sem afiliação com os criadores de Cube World.
