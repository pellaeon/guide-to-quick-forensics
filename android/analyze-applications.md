# Analisar aplicativos

## Aplicativos de verificação e antivírus

Alguns aplicativos verificam automaticamente os aplicativos instalados no sistema, para ver se eles são conhecidos como aplicações mal-intencionadas.

* [Koodous Antivirus ](https://play.google.com/store/apps/details?id=com.koodous.android)
* [Lookout](https://play.google.com/store/apps/details?id=com.lookout)

Recomendamos extremo cuidado se estiver considerando utilizar esses aplicativos de verificação, que funcionam extraindo e carregando os APKs instalados no sistema para sua própria plataforma, e comparando os APKs com malwares conhecidos. Informações do dispositivo e, provavelmente informações pessoais também podem ser enviadas para a plataforma. Verifique a política de privacidade das plataformas antes de instalar e fazer a varredura com esses aplicativos e faça uma avaliação de risco antes de utilizar estas plataformas.

Como alternativa, há um aplicativo antivírus de código aberto [Hypatia](https://github.com/Divested-Mobile/Hypatia), que utiliza bancos de dados de assinaturas do ClamAV, ESET e da [lista de ameaças direcionadas feita pelo brotherder](https://github.com/botherder/targetedthreats).

Esses aplicativos de scanner e antivírus só podem ver quais outros aplicativos estão instalados e não conseguem inspecionar profundamente o sistema operacional, pois eles próprios estão em _sandbox_. No entanto, malwares de média a alta sofisticação se incorporam ao sistema sem serem exibidos como um aplicativo. O conhecimento desses aplicativos de scanner e antivírus sobre malwares também depende de seus bancos de dados, cujas fontes geralmente vêm de seus clientes corporativos. Assim, os aplicativos de scanner geralmente só conseguem encontrar malwares que se empacotam como aplicativos (que geralmente são de média a baixa sofisticação) e que já são conhecidos. Entretanto, esses scanners podem ser instalados e operados com muita facilidade e, portanto, ainda são úteis como teste de primeira linha.

Após concluir a verificação, desinstale os aplicativos do scanner para evitar a coleta de dados adicionais.

### Extrair pacotes de aplicativos (APKs)

Algumas ferramentas exigem que você extraia os arquivos APK manualmente e os carregue. Abaixo estão algumas ferramentas que podem extrair APKs.

* [Apk Extractor](https://f-droid.org/packages/axp.tool.apkextractor/) (código aberto, última atualização em 2018)
* [Kanade](https://github.com/alexrintt/kanade) (código aberto, última atualização em 2022)
* [Androidqf](https://github.com/mvt-project/androidqf/) (Android Quick Forensics, Perícia Rápida do Android)

Depois que um APK é extraído, também é possível calcular o hash do arquivo (MD5 ou SHA) e pesquisar o hash usando sites como o VirusTotal.com .&#x20;

### Ferramentas online

### Exodus Privacy

O [Exodus Privacy](https://reports.exodus-privacy.eu.org/en/) é uma ferramenta para privacidade. Ele pode analisar aplicativos e listar rastreadores contidos em um aplicativo.

### Hybrid-analysis.com

O [Hybrid-analysis ](https://www.hybrid-analysis.com/)permite que você carregue um arquivo APK para análise. Ele verifica o APK usando vários softwares antivírus e o VirusTotal.

### MobSF

O [MobSF](https://github.com/MobSF/Mobile-Security-Framework-MobSF) descompila o aplicativo e analisa seu conteúdo, listando itens como URLs, arquivos estáticos e atividades. Esses itens podem ser usados para motivar outras análises.

Há uma versão on-line do MobSF disponível em [https://mobsf.live.](https://mobsf.live/)

Você também pode hospedar o MobSF por conta própria ou usar serviços de hospedagem gratuitos, como o Play with Docker, para hospedar uma instância privada do MobSF. O Play with Docker oferece 4 horas de tempo de sessão.&#x20;

Outras ferramentas

Há também outras ferramentas de análise online. As listadas abaixo não são especializadas em APK.

* [https://cuckoo.cert.ee/](https://cuckoo.cert.ee/)
* [https://app.any.run/](https://app.any.run/)
* [https://www.virustotal.com/](https://www.virustotal.com/)

### Interpretação dos resultados da análise

As ferramentas produzirão muitas informações técnicas sobre o aplicativo. Para interpretá-las, seria necessário um conhecimento técnico de como os aplicativos móveis funcionam (por exemplo: o que são provedores de conteúdo, serviços, atividade). No entanto, uma análise parcial poderia ser feita simplesmente verificando se os arquivos, URLs e endereços IP contidos no aplicativo já são conhecidos como maliciosos.
