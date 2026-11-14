# Cube World Mod — launcher e atualizações

Mod comunitário para **Cube World Alpha de 23/07/2013**, com launcher **Windows x64** e **Linux x64 AppImage**. Port Vulkan separado e não incluído.

## Descarregar

Versão pública experimental atual: **0.37.0-coop.preview.14**, launcher **0.2.13**.

- [Windows x64 — launcher EXE](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.14/CubeWorldMod-Windows-x64.exe)
- [Linux x64 — AppImage](https://github.com/xTestMeX/cube-world-mod-releases/releases/download/0.37.0-coop.preview.14/CubeWorldMod-Linux-x64.AppImage)
- [Notas, pacotes e ficheiros de verificação](https://github.com/xTestMeX/cube-world-mod-releases/releases/tag/0.37.0-coop.preview.14)

Cada pessoa precisa da sua própria instalação compatível do jogo. O download **não inclui Cube.exe, Server.exe, bases de dados originais ou saves**. O launcher verifica os executáveis antes de preparar uma cópia isolada. As DLLs do mod continuam x86, como exige o jogo original.

## Correção do arranque Windows

O launcher 0.2.13 corrige um bloqueio reproduzido no carregamento da DLL. A thread principal permanece em execução durante o carregamento; a inicialização ocorre na thread da janela Cube quando esta fica pronta. Inclui diagnóstico da etapa, erro remoto e saída do processo em `launcher-debug.log`/`native-run.log` e `classes-alpha.log`.

Quem recebeu «Mod injection failed (Windows error 0)» deve atualizar, fechar/reabrir o launcher e tentar novamente. A confirmação no PC Windows afetado ainda é necessária; os testes Win32 isolados sob Proton não substituem essa verificação. As bibliotecas de rede mantêm as melhorias de latência anteriores.

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
