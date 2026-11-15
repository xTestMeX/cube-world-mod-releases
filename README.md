# Cube World Mod — launcher e atualizações

Mod comunitário para **Cube World Alpha de 23/07/2013**, com launcher **Windows x64** e **Linux x64 AppImage**. Port Vulkan separado e não incluído.

## Descarregar

Versão pública experimental atual: **0.37.0-coop.preview.16**, launcher **0.2.15**.

- [Windows x64 — launcher EXE](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.16/CubeWorldMod-Windows-x64.exe)
- [Linux x64 — AppImage](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.16/CubeWorldMod-Linux-x64.AppImage)
- [Notas, pacotes e ficheiros de verificação](https://github.com/xTestMeX/cube-world-mod-releases/releases/tag/0.37.0-coop.preview.16)

Cada pessoa precisa da sua própria instalação compatível do jogo. O download **não inclui Cube.exe, Server.exe, bases de dados originais ou saves**. O launcher verifica os executáveis antes de preparar uma cópia isolada. As DLLs do mod continuam x86, como exige o jogo original.

## Correção do arranque cooperativo Windows

A preview.16 corrige uma verificação que ainda recusava o arranque pelo convite quando o Windows carregava o jogo noutra base de memória (ASLR). O adaptador de rede passa a validar dois endereços IAT pela base real, mantendo o SHA-256 e os restantes bytes exatos. Conserva as correções anteriores das classes e do carregamento da DLL, sem alterar Cube.exe nem desativar ASLR.

Os novos registos identificaram a rejeição no bootstrap nativo, antes das classes e da ligação ao mundo. A falha foi reproduzida e corrigida em duas bases de memória com o instalador real; os testes de ligação local, lock e preservação dos registos passaram. Mantêm-se as rotinas que melhoraram a latência e TCP_NODELAY. O servidor e as DLLs de gameplay não mudaram.

Fecha jogo/servidor, atualiza e fecha/reabre o launcher. O convidado deve voltar a entrar pelo convite. A confirmação no Windows físico continua pendente; os testes isolados não substituem essa confirmação. Se voltar a falhar, recolhe `native-run.log`, `client-net.log`, `launcher-process.log` e `classes-alpha.log` da pasta do perfil. O novo `client-net.log` identifica a etapa interna e a base da imagem.

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
