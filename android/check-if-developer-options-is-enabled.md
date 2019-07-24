# Verificar se as opções do desenvolvedor estão ativadas

Se a Depuração USB em [Opções do Desenvolvedor](https://developer.android.com/studio/debug/dev-options) estiver habilitada, é possível controlar um telefone usando o Android Debug Bridge (ADB) via USB ou via WiFi, se a Depuração WiFi estiver habilitada. O ADB também pode permitir que invasores coloquem executáveis ​​no telefone em `/data/local/tmp` e o executem como usuário do sistema `shell`.

A menos que o telefone sob verificação esteja sendo usado para desenvolvimento de aplicativos Android, **não é normal que a Depuração USB esteja habilitada.** Você deve descobrir o motivo e quando o usuário a habilitou.

Se a Depuração USB estiver habilitada, você deve:

* Verificar se há aplicativos instalados via ADB e, em caso positivo, analisar esses aplicativos.
* Verificar se há arquivos suspeitos em `/data/local/tmp`

Depois de determinar que nenhum malware foi instalado usando o ADB, a Depuração USB deve ser desabilitada.

Para usuários de alto risco, verificar os dois itens acima não é suficiente, pois há muitas outras maneiras pelas quais o ADB pode ser usado para infectar um dispositivo, e também pode ser possível que, após a infecção, o invasor tenha apagado seus rastros. Portanto, recomendamos limpar o dispositivo de fábrica antes de continuar a usá-lo.
