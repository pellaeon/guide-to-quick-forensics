# Verificação de dispositivos remotamente

Durante a época de confinamento em razão da pandemia COVID-19, adicionamos algumas etapas que podem ajudar a verificar remotamente os dispositivos potencialmente comprometidos. Por enquanto, elas incluem apenas soluções para computadores Windows e MacOS usando [Teamviewer](https://www.teamviewer.com/pt/?coupon=CMP-PR-BF24) e [Chrome Remote Desktop](https://remotedesktop.google.com/?pli=1\&hl=pt-BR), pois ainda não temos nenhuma solução satisfatória para smartphones.

## Limitações da perícia remota

### O problema da confiança

Em qualquer solução de área de trabalho remota que dependa de uma plataforma de terceiros, há uma questão importante de confiança. Quando você instala um software de acesso remoto desse tipo, precisa saber que a empresa que desenvolve a solução pode usar o software para acessar o seu computador, mas também pode gravar qualquer interação que você tenha por meio da solução. Portanto, é muito importante usar uma solução em que você confie, com base em seu modelo de ameaças.

Neste guia, usamos dois softwares:

* O [Teamviewer](https://www.teamviewer.com/pt/), desenvolvido pela TeamViewer AG, uma empresa alemã com sede em Göppingen.
* O [Chrome Remote Desktop](https://remotedesktop.google.com/?pli=1\&hl=pt-BR), desenvolvido pelo Google e integrado ao ecossistema do Google (o que exige o uso de contas do Google).

O Teamviewer teve vários problemas de segurança no passado, a empresa FireEye alegou que sofreu ataque de um [grupo patrocinado pelo Estado chinês em outubro de 2019](https://www.securitynewspaper.com/2019/10/14/fireeye-confirms-that-apt14-group-hacked-teamviewer-attackers-would-have-accessed-billions-of-devices/). Tendemos a confiar mais no Google por suas capacidades de segurança mas, dependendo do seu modelo de ameaças, o Teamviewer pode ser uma opção melhor. Estamos usando o Teamviewer para Windows, aqui, porque a Área de Trabalho Remota do Chrome ainda não é compatível com o MacOS (não permite compartilhamento de arquivos).

### O problema de precisar de acesso online

Outro problema com a verificação de dispositivos remotamente é que eles precisam de acesso à internet. Conforme explicado anteriormente, isso pode acarretar riscos para o usuário. Se o dispositivo estiver realmente comprometido e sendo monitorado remotamente, as operadores do monitoramento poderão identificar que o usuário está recebendo suporte técnico, o que poderá resultar em retaliação contra a pessoa a quem você está tentando apoiar.

Antes de prestar qualquer suporte remoto, você deve se certificar de abordar esse risco com a pessoa que está recebendo suporte.

## Algumas informações sobre o processo

Para executar a verificação de um dispositivo remotamente, é necessário conversar previamente com a pessoa para informá-la de que:

* Ela deverá instalar um software de área de trabalho remota antes
* Ela deverá permanecer na frente do computador durante a verificação para inserir a senha de administrador (uma verificação que geralmente dura de 30 minutos a uma hora)
* Ela deverá remover o software de área de trabalho remota depois

Lembre-se de que [confiança](trust.md) é uma parte fundamental de qualquer suporte de segurança, portanto, certifique-se de que o processo esteja claro para a pessoa que você está apoiando e que ela consinta com isso.
