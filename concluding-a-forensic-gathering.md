# Concluindo uma coleta de evidências forenses

Para concluir uma coleta de evidências forense, você deve sempre:

1. Informar o usuário sobre os resultados
2. Preservar as evidências&#x20;
3. Restaurar o dispositivo ao seu estado original

### Infecções por malware

Se forem encontradas infecções por malware em um dispositivo, aplica-se o procedimento usual de _Resposta a Incidentes_:

1. Contenção
2. Erradicação
3. Recuperação
4. Lições aprendidas / retenção de evidências

Consulte o guia em inglês [_Computer Security Incident Handling Guide_](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-61r2.pdf) do NIST (National Institute of Standards and Technology, ou Instituto Nacional de Normas e Tecnologia, em tradução livre) para obter mais informações.

O procedimento de resposta a incidentes muda muito dependendo das situações. Por exemplo:

1. Um aplicativo que rouba os contatos do usuário foi instalado e usado: avalie se o vazamento dos contatos do usuário colocaria alguém em perigo. Caso contrário, simplesmente remova o aplicativo.
2. Um _malware_ que tenta roubar os cookies de login de outros aplicativos: altere as senhas de todas as contas de login, faça logout de todas as sessões e faça login novamente. Se o malware abusar e violar as proteções do sistema, faça o reset do sistema para a configuração original ou formatação, e instale as atualizações mais recentes do sistema. Se o hardware do dispositivo estiver desatualizado, peça ao usuário para trocar por um novo dispositivo, se as condições permitirem.
