# Verificar se foi feito root no telefone

## O que é _root_?

_Root_ (raíz, em tradução literal) é uma conta de superusuário do sistema em todos os sistemas Android (na verdade, todos os sistemas operacionais do tipo UNIX, incluindo Linux, macOS e iOS). O usuário _root_ tem permissão para realizar qualquer ação no sistema. Normalmente, apenas alguns processos do sistema são executados como _root_ (mas isso não se aplica a todos). Os aplicativos de usuário nunca são executados como _root_, mas sim em contas com menos privilégios (contas normais).

Às vezes, os usuários querem personalizar o sistema de uma forma não permitida para contas normais, como remover os aplicativos integrados instalados pelo fornecedor (_bloatware_) para liberar espaço de armazenamento. Nesse caso, os usuários precisam fazer o _root_ do sistema, o que significa obter o controle direto da conta _root_ no sistema.

O _rooting_ (literalmente enraizamento, mas aqui com o sentido de ganhar acesso e privilégios de usuários root) geralmente envolve:

1. Desbloquear o carregador de inicialização do dispositivo.
2. "Fazer _flash_ " um “sistema operacional de recuperação” personalizado (geralmente chamado apenas de “recuperação”), que é um sistema operacional mínimo que fica em uma partição de armazenamento separada. O objetivo original da recuperação é instalar atualizações do sistema.
3. Usando a recuperação personalizada, fazer o _flash_ (instalação) do pacote de root.

No processo de root, importantes recursos de segurança do sistema são desativados (como o desbloqueio do carregador de inicialização). Um sistema com root também adiciona mais vetores de ataque ao sistema.

## Procure aplicativos relacionados ao root

Quando um telefone tem acesso ao root (à raiz), o processo geralmente envolve a instalação de um aplicativo para gerenciar o acesso à raiz, na maioria das vezes o [Magisk](https://github.com/topjohnwu/Magisk) (ou [SuperSU](http://www.supersu.com/) em versões antigas do Android). Uma primeira etapa é verificar se o aplicativo Magisk está instalado. Você pode verificar diretamente o ícone no menu principal ou ir para **Configurações > Aplicativos** e procurar o aplicativo.

![](../.gitbook/assets/supersu.png)

## Verificar com o Root Verifier

O Root Verifier é um aplicativo [open source](https://github.com/abcdjdj/RootVerifier-APP) que verifica se um telefone Android está enraizado (rooted) por meio de diferentes técnicas. Você pode instalá-lo na [Google Play Store ](https://play.google.com/store/apps/details?id=com.abcdjdj.rootverifier) ou no [repositório F-Droid](https://f-droid.org/packages/com.abcdjdj.rootverifier/) .&#x20;

NB: Para instalar via F-Droid, será necessário ativar a carga lateral, ou _sideloading_. O que recomendamos fazer pontualmente e com muito cuidado. Veja a sessão Aplicativos com carregamento lateral (sideload) no capítulo [Revisar Aplicativo Instalados](applications.md).

Depois de instalado, você pode iniciar o aplicativo. A interface é muito simples, você só precisa clicar em “CHECK” e aguardar o resultado.

![](../.gitbook/assets/rootverifier1.png) ![](../.gitbook/assets/rootverifier2.png)
