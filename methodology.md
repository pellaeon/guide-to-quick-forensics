# Metodologia

A metodologia para realizar análises forenses rápidas pode ser bastante [ad-hoc](https://pt.wikipedia.org/wiki/Ad_hoc) e com o tempo você desenvolverá a sua própria metodologia. Este guia deve ajudar nesse processo. Em geral, ao tentar fazer a triagem de uma possível infecção, você procurará qualquer anomalia que possa identificar no dispositivo. Essas anomalias, por exemplo, podem ser:

1. Aplicativos e processos em execução no dispositivo que você e a proprietária do dispositivo não reconhecem. Aplicativos e processos que apresentam algumas características incomuns, como nomes e locais de arquivos suspeitos ou tentativas de ocultação.
2. Como o _spyware_ normalmente deseja sobreviver a um desligamento do dispositivo, você procurará aplicativos que busquem ter persistência no dispositivo e, portanto, estejam registrados para abrirem/executarem de forma automática na inicialização.
3. Conexões de rede suspeitas com infraestrutura e serviços que você e a proprietária do dispositivo não reconhecem.
4. Contas, perfis ou configurações que não pertencem à proprietária do dispositivo.

Embora não seja possível compilar uma lista de verificação exaustiva de anomalias precisas a serem observadas, o processo de desenvolvimento de uma metodologia forense rápida e robusta exigirá _treinar o seu olhar_, inspecionando o maior número de dispositivos possível. Eventualmente, você começará a reconhecer padrões em vários sistemas operacionais e se tornará mais rápida e eficiente para descartar aplicativos legítimos e identificar aqueles que se destacam. Isso requer prática.

**Atenção**: a metodologia que descrevemos neste guia depende muito do uso de ferramentas que estão disponíveis publicamente e são altamente populares. Por esse motivo, _malwares_ mais sofisticados podem ser capazes de enganar ou evadir-se dessas ferramentas e levar você a acreditar que está vendo um sistema limpo. Portanto, **essa metodologia precisa ser considerada o melhor esforço possível.** Você deve levar em conta a possibilidade de falsos negativos e ajustar sua avaliação de acordo com isso (especialmente em relação à [segurança](safety.md) da proprietária do dispositivo).

## Considerações sobre processos legais

Em algumas circunstâncias, é possível que a proprietária do dispositivo tenha interesse em entrar com uma ação legal contra os autores do ataque que você está documentando ou, talvez, contra os produtores da tecnologia usada para o ataque. Esse pode ser o caso, por exemplo, de vítimas de violência doméstica ou talvez de ativistas que buscam provar a vigilância ilegal de suas comunicações.

Se você acredita que a pessoa que está ajudando pode estar interessada em qualquer forma de litígio judicial, especialmente com base no seu trabalho, talvez seja necessário adaptar sua metodologia. As regras e as práticas recomendadas para a coleta de evidências digitais admissíveis em um tribunal podem variar de país para país, e de jurisdição para jurisdição. Geralmente, para proteger a integridade do dispositivo e garantir a [cadeia de custódia](https://pt.wikipedia.org/wiki/Cadeia_de_cust%C3%B3dia), a aquisição de dados (especialmente de telefones) pode ser muito restrita.

Você deve se informar sobre as leis e as práticas padrão da jurisdição em que normalmente opera. Idealmente, você deve buscar orientação de especialistas forenses locais e talvez até mesmo buscar a assistência de uma empresa forense credenciada.
