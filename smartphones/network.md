# Monitorar o tráfego de rede

Monitorar o tráfego de rede de um telefone é uma das melhores maneiras de identificar atividades mal-intencionadas sem interagir com o telefone celular e, portanto, contornar qualquer mecanismo que o malware possa ter desenvolvido para evitar a detecção. Mas isso requer uma ferramenta externa para registrar o tráfego e algum conhecimento de rede para identificar o tráfego suspeito.

Limitações

Muitos aplicativos móveis e malwares agora habilitam o “SSL Pinning”, o que dificulta descriptografar o tráfego. A única maneira de contornar o SSL Pinning é fazer o _root/jailbreak_ do dispositivo e usar ferramentas como Frida. No entanto, para o objetivo da perícia, só precisamos fazer isso se houver forte suspeita de que o tráfego mal-intencionado esteja oculto por meio da criptografia SSL Pinning.

## Monitorar consultas de DNS

Em vez de monitorar todo o tráfego de rede, o que exige uma configuração complexa, podemos monitorar apenas as consultas de DNS. A maioria dos sistemas operacionais permite que os usuários configurem seus próprios servidores DNS. Podemos configurar nosso próprio servidor DNS para registrar as consultas e apontar o dispositivo em teste para ele.

Podemos implantar nosso próprio servidor DNS com:

* Pi-hole
* Adguard Home

Ou usar um servidor DNS baseado em nuvem, como o NextDNS. A desvantagem dos servidores DNS baseados em nuvem é que eles poderão ver as consultas dos dispositivos.

Um provedor de DNS em nuvem é o NextDNS, que permite configurar um servidor DNS sem a necessidade de uma conta. Ele também oferece aplicativos para os principais sistemas operacionais, que permitem configurar o dispositivo para usar o servidor personalizado. Primeiro, acesse [https://my.nextdns.io/start](https://my.nextdns.io/start) para criar uma _Configuration ID_ temporária que deve ser inserida no aplicativo NextDNS. Então, todas as consultas de DNS feitas pelo telefone serão registradas na guia _Logs_.



![Consultas de DNS registradas no NextDNS](../.gitbook/assets/Screenshot_20220506_165152.png)

## Monitorar o tráfego de rede completo de um roteador WiFi

Uma maneira de monitorar o tráfego de rede do seu telefone é gravar o tráfego diretamente de um roteador WiFi usado pelo seu telefone celular. Dependendo do seu roteador WiFi, pode ser possível registrar o tráfego diretamente dele (usando uma ferramenta como [tcpdump](https://www.tcpdump.org/)).

Se não for possível registrar o tráfego usando o roteador WiFi real, é possível construir facilmente um roteador usando um [Raspberry Pi](https://www.raspberrypi.org/) e o software [RaspAP](https://raspap.com/) (consulte [aqui](https://howtoraspberrypi.com/create-a-wi-fi-hotspot-in-less-than-10-minutes-with-pi-raspberry/) para acessar um tutorial sobre como instalá-lo).

Depois que o roteador estiver instalado, você poderá se conectar a ele usando SSH e começar a capturar o tráfego usando [tcpdump](https://www.tcpdump.org/). Em seguida, conecte o telefone celular que deseja testar a essa rede WiFi e registre o tráfego durante 30 minutos a uma hora.

Após o término da captura, baixe o arquivo pcap em seu computador e analise o tráfego de rede usando o [WireShark](https://www.wireshark.org/). Verifique especialmente os seguintes elementos:

* Conexões com endereços IP sem solicitações de DNS
* Conexões com domínios que não estão listados nas listas de sites mais acessados
* Conexões em portas diferentes das portas 80 e 443

Se você encontrar algum tráfego suspeito para um endereço IP ou domínio, poderá usar as seguintes ferramentas para obter mais informações sobre ele:

* [CentralOps](https://centralops.net/co/) permite ver o proprietário de um IP ou o _whois_ de um domínio (não requer uma conta)
* [RiskIQ](https://community.riskiq.com/home) permite ver o histórico do DNS e tem muitas indicações sobre IPs e domínios maliciosos (requer uma conta, número limitado de consultas com uma conta gratuita)
* O [AlienVault OTX](https://otx.alienvault.com/) é um grande banco de dados de indicadores de software malicioso, no qual você pode pesquisar esse IP ou domínio para ver se há alguma atividade mal-intencionada conhecida a partir dele (requer uma conta, é gratuito).
* [VirusTotal,](https://www.virustotal.com/) principalmente para os malwares mais comuns.

Para configurar um ambiente para análise de tráfego, consulte [este guia](https://mobile-security.gitbook.io/mobile-security-testing-guide/general-mobile-app-testing-guide/0x04f-testing-network-communication).

## Monitore o tráfego de rede com aplicativos no dispositivo

Esses aplicativos geralmente funcionam criando um servidor VPN no dispositivo e configurando o sistema para usar o servidor VPN.

* [NetGuard](https://netguard.me/): para Android, código aberto
* [Lockdown](https://lockdownprivacy.com/firewall): para iOS, código aberto
* [Blokada](https://apps.apple.com/us/app/blokada/id1508341781): para iOS, proprietário

## Como procurar tráfego suspeito?

Os comportamentos a seguir são mais suspeitos:

* Aplicativos ou conexões que geram muito tráfego de dados.
* Aplicativos ou conexões que enviam mais dados do que baixam.
* Conexões que ocorrem periodicamente.
* Nomes de domínio estranhos. Quando encontrados, basta pesquisá-los no Google ou no VirusTotal.
* Uso de portas incomuns.
* Envio ou recebimento de dados quando o usuário não está usando o telefone. Por exemplo, quando está dormindo.

## Use a VPN de emergência do Civil Sphere

O [Civil Sphere Project](https://www.civilsphereproject.org/what-we-do), uma organização nascida do [Stratosphere Research Laboratory da Universidade Técnica Tcheca](https://www.stratosphereips.org/), em Praga, oferece um [serviço de VPN de emergência](https://www.civilsphereproject.org/emergency-vpn) para identificar dispositivos comprometidos.

O serviço de VPN de emergência permite analisar e identificar o tráfego suspeito de um dispositivo móvel usado por jornalistas e ONGs. Sob demanda, a equipe do Civil Sphere lhe enviará credenciais para fazer login na VPN deles com o seu telefone. Durante o uso da VPN, eles gravarão todo o tráfego que sai do seu telefone por um período máximo de três dias. No final da gravação, eles analisarão o tráfego usando técnicas automatizadas e manuais para identificar atividades mal-intencionadas ou problemas de segurança nos aplicativos em execução no seu telefone e enviarão o resultado dessa análise por e-mail.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Uma das limitações dessa técnica é que você precisa fornecer o tráfego de rede do seu celular a uma organização de terceiros (Civil Sphere). Você pode [entrar em contato com eles](https://www.civilsphereproject.org/get-started) para obter mais informações sobre como esses dados são armazenados e usados. A vantagem dessa solução é que você pode contar com eles para analisar o tráfego de rede, o que pode ser um processo complexo e demorado.

Consulte [o site da organização](https://www.civilsphereproject.org/emergency-vpn) para obter mais informações.
