---
descrição: >-

  Esta página serve como minha nota para configurar o monitoramento do tráfego
  de rede no

  Linux.
---

# Nota: Monitoramento do tráfego de rede no Linux

## Configurar o compartilhamento de WiFi

Usando o KDE

1. Conecte um adaptador WiFi que suporte o modo AP.
2. Clique com o botão direito do mouse no ícone "Rede" na barra de tarefas. Clique em _Configure Network Connections_ (Configurar conexões de red&#x65;_)_.
3. Clique em _Add,_ selecione _WiFi (Shared)._
4. Na guia WiFi, defina:
   1. SSID: o que você quiser
   2. Limit Device (Dispositivo limite): selecione o adaptador que você acabou de conectar.
   3. Wireless Security (Segurança sem fio): configure uma senha pessoal WPA2
   4. IPv4: _Method_: _Share with other computers_ (Método: Compartilhar com outros computadores)
5. Escolha um nome de conexão (basicamente o nome do perfil de rede)
6. Salvar
7. Clique com o botão esquerdo do mouse no ícone "Rede" e clique em "Conectar" no nome da conexão que você acabou de criar.
8. Agora o AP deve ser iniciado e você deve ver em outros dispositivos o SSID que acabou de configurar.

## Configurar o redirecionamento para o proxy interceptador

Para a perícia móvel, normalmente não é necessário interceptar o tráfego SSL, pois para interceptar o tráfego SSL seria necessário configurar uma autoridade de certificação (CA) SSL autoassinada para o dispositivo móvel, mas a maioria dos aplicativos não confia na CA SSL importada pelo usuário. Para fazer com que os aplicativos confiem na CA autoassinada, seria necessário fazer o _root_ no dispositivo Android, o que não é recomendado, pois, ao realizar perícias, não se deve alterar o dispositivo em questão.
