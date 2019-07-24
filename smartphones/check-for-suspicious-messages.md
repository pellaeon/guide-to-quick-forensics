# Verificar mensagens suspeitas

As mensagens que contêm links são um vetor de ataque comum.

<figure><img src="../.gitbook/assets/Captura de Tela 2024-12-11 às 22.18.08.jpg" alt="Uma mensagem contendo um link que infecta o alvo com o malware Cytrox Predator. "><figcaption><p>Uma mensagem contendo um link que infecta o alvo com o malware Cytrox Predator. Fonte: <a href="https://citizenlab.ca/wp-content/uploads/2021/12/Fig-7.png">Citizen Lab</a></p></figcaption></figure>

Os links podem ser enviados de qualquer aplicativo de mensagens instantâneas ou SMS. Há alguns tipos de links maliciosos:

| Alvo do Link                                                                              | Objetivo do Atacante                                                 | Sofisticação | Mitigação                                                      |
| ----------------------------------------------------------------------------------------- | -------------------------------------------------------------------- | ------------ | -------------------------------------------------------------- |
| Site de _phishing_, como uma página da web que se parece com a página de login do Google  | Enganar o usuário para que ele insira dados pessoais ou senhas       | Baixo        | Verificar nomes de domínio da página da web e certificados SSL |
| Download de aplicativo                                                                    | Convencer o usuário a fazer download e instalar o aplicativo         | Baixo        | Não instalar aplicativos fora das lojas de aplicativos         |
| Página da web contendo _exploits_ da web, como XSS (Cross Site Scripting)                 | Roubar cookies de sessão online ou operar a sessão aberta no momento | Média        | Não clicar em links enviados por pessoas desconhecidas         |
| Página da web que explora uma vulnerabilidade de um navegador.                            | Explorar a vulnerabilidade do navegador ou do aplicativo             | Alta         | Não clique em links enviados por pessoas desconhecidas         |

### Salvando mensagens

1. Copie a mensagem inteira, inclusive o link, para a área de transferência
2. Como alternativa, salve uma captura de tela contendo o texto completo
3. Se possível, arquive o link usando a [_Wayback Machine_](https://web.archive.org/).

### Verificação de links

Basta pesquisar o link no Google ou colar o link em sites como o [VirusTotal](https://www.virustotal.com).
