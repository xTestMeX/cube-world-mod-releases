# Cube World Mod — launcher e atualizações

Mod comunitário para **Cube World Alpha de 23/07/2013**, com launcher **Windows x64** e **Linux x64 AppImage**. Port Vulkan separado e não incluído.

## Descarregar

Versão pública experimental atual: **0.37.0-coop.preview.23**, launcher **0.2.22**.

- [Windows x64 — launcher EXE](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.23/CubeWorldMod-Windows-x64.exe)
- [Linux x64 — AppImage](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.23/CubeWorldMod-Linux-x64.AppImage)
- [Notas, pacotes e ficheiros de verificação](https://github.com/xTestMeX/cube-world-mod-releases/releases/tag/0.37.0-coop.preview.23)

Cada pessoa precisa da sua própria instalação compatível do jogo. O download **não inclui Cube.exe, Server.exe, bases de dados originais ou saves**. O launcher verifica os executáveis antes de preparar uma cópia isolada. As DLLs do mod continuam x86, como exige o jogo original.

## Teleporte das expedições e arrasto — preview.23

Corrige a ordem dos bloqueios na descarga das zonas antigas após o teleporte: o worker podia segurar Terrain e esperar World, enquanto o thread principal segurava World e esperava Terrain. O percurso foi reproduzido nas instruções do executável, a partir dos registos de bloqueio da preview.22. A alteração mantém a remoção/destruição nativas e os escopos originais dos bloqueios.

A zona vazia da barra de título do launcher passa a receber o arrasto. O texto/ícone, duplo clique e botões de minimizar/maximizar/fechar foram verificados por eventos de interface em ambiente headless. Mantém os contadores de 90 segundos por fase e o destino de cerca de 10 000 blocos.

Testes isolados de espera circular, rollback, zonas/regiões, transferência/regresso, dez etapas, recompensas, snapshot/religação e interface passaram. Ambos launchers compilados e pacotes assinados verificados. **Não foi aberto Cube.exe/Server.exe; a confirmação real da entrada na expedição e do movimento nativo da janela continua pendente.**

Todos fecham jogo/servidor, atualizam e fecham/reabrem o launcher. Confirmar launcher **0.2.22** e mod **preview.23**, criar sessão nova, arrastar a janela e testar entrada/inventário/extração após a primeira etapa. Se bloquear, aguardar 8–10 segundos antes de fechar e fornecer `native-run.log`, `native-fault.log` e `classes-alpha.log` da pasta do perfil.

### Correções mantidas da preview.22

A validação de terreno evita cópias de memória repetidas por tile, e os bloqueios adicionais do mesher são libertados antes da fase gráfica. O HUD cooperativo mostra idade sincronizada com o anfitrião e limite de **90 segundos por fase** para preparação e carregamento/validação da chegada. Diagnóstico adicional recolhe threads, memória virtual e exceções perante bloqueios. Configurações e saves preservados.

## Destino das expedições — preview.20

As expedições cooperativas passam a cerca de **10 000 blocos de distância horizontal**, com o chão quatro blocos acima do sólido mais alto no local. A altura do jogador deixa de elevar a arena em 500 metros. O alinhamento à zona e a entrada de cada sala fazem variar ligeiramente a distância.

Mantém as dez etapas, cenário, recompensas, remoção e regresso. Os quatro slots preferem direções distintas; os journals antigos conservam as coordenadas anteriores para limpeza. As otimizações da preview.19 continuam ativas. A alteração aplica-se ao servidor cooperativo; o percurso solo é independente.

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

Canal atual: [manifesto experimental assinado](https://raw.githubusercontent.com/xTestMeX/cube-world-mod-releases/main/channels/preview.json). A assinatura Ed25519 autentica o manifesto, e SHA-256 verifica cada ficheiro. Configurações e saves permanecem fora das pastas de versões. O launcher conserva a versão anterior e prepara a sua própria substituição ao fechar.

Se usas um launcher local anterior a **0.2.11**, descarrega esta AppImage/EXE uma vez. O novo launcher migra o antigo endereço oficial de atualização; endereços personalizados são preservados.

## Fontes e dependências

Cada release inclui os fontes correspondentes do mod/launcher, `SHA256SUMS` e avisos/licenças de terceiros. Apenas ficheiros próprios e dependências redistribuíveis são publicados. O jogo original, os mundos, os personagens, convites e chaves privadas de publicação não são distribuídos.

Projeto comunitário não oficial, sem afiliação com os criadores de Cube World.
