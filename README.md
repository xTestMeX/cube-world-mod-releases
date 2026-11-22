Warning: truncated output (original token count: 11014)
Total output lines: 367

# Cube World Mod — launcher e atualizações

Mod comunitário para **Cube World Alpha de 23/07/2013**, com launcher **Windows x64** e **Linux x64 AppImage**. Port Vulkan separado e não incluído.

## Descarregar

Versão pública experimental atual: **0.37.0-coop.preview.86**, launcher **0.2.85**.

- [Windows x64 — launcher EXE](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.86/CubeWorldMod-Windows-x64.exe)
- [Linux x64 — AppImage](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.86/CubeWorldMod-Linux-x64.AppImage)
- [Notas, pacotes e ficheiros de verificação](https://github.com/xTestMeX/cube-world-mod-releases/releases/tag/0.37.0-coop.preview.86)

Cada pessoa precisa da sua própria instalação compatível do jogo. O download **não inclui Cube.exe, Server.exe, bases de dados originais ou saves**. O launcher verifica os executáveis antes de preparar uma cópia isolada. As DLLs do mod continuam x86, como exige o jogo original.

## Arquimago e Esconderijo dos Corvos · preview.86

O Arquimago é +3, azul ou laranja. Os itens lançados pelo baú têm o nível e a raridade do boss. Esta versão inclui o Esconderijo dos Corvos renovado e os ajustes de saque e frequência da Cripta Esquecida e do Templo dos Magos.

## Cripta Esquecida · preview.82

A entrada de pedra conduz a um salão subterrâneo de 111 × 81 blocos com galerias, tochas e mobiliário interativo. Um único guardião +4 protege o baú, que larga 2 a 5 itens e partilha o saque em cooperativo. A nova planta surge em zonas novas e adapta a escavação ao terreno. As verificações automáticas correram fora do jogo.

## Entrada e braseiros do Templo dos Magos · preview.81

O cliente cooperativo consulta de novo o anfitrião quando uma confirmação de movimento é rejeitada, deixando avançar o pedido de entrada. As chamas dos 16 braseiros nascem dentro da taça, também nos templos já guardados. Os testes automáticos decorreram fora do jogo.

## Templo dos Magos · preview.80

Bancos, cadeiras e camas usam a altura do assento ou do colchão, incluindo nos templos já guardados. As chamas são contínuas, com brasas pequenas, e a luz ambiente melhora a leitura do salão. A preparação cooperativa processa mais colunas prontas por passagem e evita reescrever blocos iguais. O aspeto e os tempos de carregamento em jogo ficam por confirmar.

## Mobiliário e iluminação do Templo dos Magos · preview.79

O baú tem fundo de tábuas e paredes laterais. Os braseiros têm chamas animadas e os lustres de cristal dão luz. Os bancos, cadeiras e camas do templo grande podem ser usados com `R`, incluindo em templos grandes já guardados. A aparência da iluminação e o alinhamento das poses aguardam confirmação em jogo.

## Implantação do Templo dos Magos · preview.77

O templo pode ser construído em mais terrenos. O gerador avalia até 63 posições por zona sorteada e ajusta a altura do edifício, os pilares e a escadaria. Em terreno junto a água rasa, exige uma ligação seca ao exterior. A planta de 199 × 151 blocos e o sorteio de 50% aplicam-se em solo e em cooperativo. A frequência real ainda depende das zonas exploradas.

## Templo dos Magos · preview.76

O sorteio do Templo dos Magos passou de 10% para 50% em zonas novas, em solo e em cooperativo. A construção exige terreno adequado à planta de 199 × 151 blocos.

## Terreno das estruturas e guardião das ruínas · preview.75

As estruturas podem adaptar terreno natural em zonas novas. A implantação prepara o acesso e as fundações em solo e em cooperativo. Nas ruínas, o servidor volta a tentar criar o guardião no piso correto quando ele falta no encontro. Passaram os testes de geometria, sincronização e recuperação fora do jogo. A validação numa sessão real fica pendente.

## Exploração e carregamento das estruturas · preview.74

Durante a compressão e a gravação do mapa, o cliente liberta o acesso ao terreno. Em cooperativo, reaproveita a estrutura preparada antes da iluminação quando o anfitrião confirma a mesma geometria. Ao recuperar uma zona carregada, agrupa o recálculo da iluminação por chunk. A melhoria de fluidez ainda precisa de ser medida em jogo.

## Consulta de atualizações · preview.73

O launcher consulta primeiro a API de conteúdos do GitHub e usa a referência completa do canal se a API estiver indisponível. Ambos os percursos validam a assinatura do manifesto.

## Exploração e gravação do mapa · preview.72

O cliente agrupa a gravação de cada peça do mapa com a do contador de descoberta e evita reler peças já conhecidas ao preparar o horizonte. Inclui a correção da confirmação das salas da cripta em cooperativo. A redução das pausas durante uma partida continua por medir.

## Entrada e guardas em cooperativo · preview.70

O servidor confirma a entrada com base na revisão do setor já validada pelo cliente. Os guardas recebidos aparecem assim que a geometria e a decoração do setor estão prontas.

## Entrada nas estruturas · preview.69

O cliente cooperativo conserva a confirmação do anfitrião enquanto o terreno está ocupado e volta a validá-la assim que consegue ler a zona. A correção aplica-se aos mundos existentes.

## Mapa e carregamento das estruturas · preview.68

Em solo e cooperativo, o mapa termina a peça atual e cede o acesso ao terreno quando o desenho da paisagem ou a validação de um edifício precisa dele. A opção está ativa por defeito. Esta versão inclui também as correções à distância de visão, ao nível dos encontros e do saque e à Armadilha de Caça do Scout. A melhoria de fluidez em jogo ainda está por medir.

## Templo dos Magos · preview.66

O templo novo mede 199 × 151 blocos. Tem dois pisos, alas ligadas por pontes e 48 peças voxel próprias. A versão também dá prioridade à preparação da entrada mais próxima e evita invalidar locais prontos quando se altera terreno do lado de fora.

O templo tem agora 10% de probabilidade no sorteio por zona nova. A construção exige terreno adequado.


Nas zonas novas, procura o «???» amarelo no mapa. No templo, abre a porta dupla com R, explora os dois pisos e derrota os cinco magos e o Arquimago. O baú lança entre dois e cinco itens para o chão. Em cooperativo, o grupo partilha o saque. Os símbolos do tapete e do altar são decorativos.

## Acampamentos e expedições · preview.62

Os acampamentos de bandidos, cultistas e mortos têm 3,5% de probabilidade cada por zona nova, antes da verificação do terreno. As arenas novas usam o mesmo salão para as dez rondas. A versão também corrige o escurecimento e a sobreposição de superfícies nas fachadas.

## Entrada nos edifícios e preparação gráfica · preview.59

Ao revisitar um edifício em cooperativo, o cliente recupera as partes que já estão desenhadas e volta a pedir a entrada assim que o setor está pronto. Em solo e cooperativo, a opção **Automático** utiliza a gráfica para preparar as faces opacas compatíveis e o relevo distante. Podes selecionar **Preparação pelo CPU** em **Configuração** para comparar a mesma rota.

Fecha o jogo e o servidor e escolhe **Procurar atualizações**. O anfitrião e os convidados devem atualizar para a mesma versão.

## Estruturas e expedições em cooperativo · preview.58

O exterior dos edifícios começa a ser preparado durante a aproximação. À entrada, o cliente confirma o chão, os objetos e os habitantes de cada setor. Nas expedições, a preparação do destino começa na cidade e a chegada é confirmada depois do teleporte. O tempo de aparecimento e a fluidez continuam por medir em jogo.

Para atualizar, fechem o jogo e o servidor e escolham **Procurar atualizações** no launcher. O anfitrião e os convidados devem usar a mesma versão.

## Reenvio de blocos das estruturas — preview.55

O anfitrião confirma se cada pedido entrou na fila, já decorre ou foi adiado. As estruturas carregadas mais próximas recebem prioridade e os restantes pedidos têm turnos reservados. O tempo total de aparecimento e a fluidez aguardam confirmação em cooperativo.

Com o jogo e o servidor fechados, escolham **Procurar atualizações**. O anfitrião e os convidados devem confirmar a **preview.55** antes de jogar.

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

Testes curtos de publicação/Alt+Tab, IA, renderer/matrizes x86, quatro orientações, layouts, saque …4514 tokens truncated…s e hashes conferidos. Nenhum Cube.exe/Server.exe aberto. **A correção ainda precisa de confirmação real em jogo.**

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
