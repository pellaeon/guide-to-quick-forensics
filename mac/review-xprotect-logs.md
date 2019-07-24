# Revisar logs do XProtect

O [XProtect](https://book.hacktricks.xyz/macos-hardening/macos-security-and-privilege-escalation/macos-security-protections/macos-gatekeeper#xprotect/) é um recurso **anti-malware** incorporado ao macOS. O XProtect **verifica qualquer aplicativo quando ele é iniciado ou modificado pela primeira vez em seu banco de dados** de malware conhecido e tipos de arquivos não seguros. Quando você faz download de um arquivo por meio de determinados aplicativos, como Safari, Mail ou Messages, o XProtect verifica automaticamente o arquivo. Se ele corresponder a algum malware conhecido em seu banco de dados, o XProtect **impedirá a execução do arquivo** e o alertará sobre a ameaça.

Para a varredura do sistema em segundo plano, o macOS usava anteriormente o MRT. Desde 2022, um novo módulo [XProtect Remediator](https://book.hacktricks.xyz/macos-hardening/macos-security-and-privilege-escalation/macos-security-protections/macos-gatekeeper#xprotect/) foi adicionado ao macOS.

Para verificar os resultados da verificação do XProtect Remediator, use o [XProCheck](https://eclecticlight.co/2022/09/05/xprocheck-a-new-utility-to-inspect-anti-malware-scans/). No entanto, a Apple não publicou detalhes sobre o Remediator, portanto, os registros podem ser difíceis de entender.
