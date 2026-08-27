No reconhecimento ativo, interagimos diretamente com o alvo para a coleta de informações.

| Técnica                | Descrição                                                                              | Ferramentas                                 | Risco de detecção                                                  |
| ---------------------- | -------------------------------------------------------------------------------------- | ------------------------------------------- | ------------------------------------------------------------------ |
| Port Scanning          | Identifica portas e serviços                                                           | Nmap, Masscan, Unicornscan                  | **Alta:** IDS e firewalls                                          |
| Vulnerability Scanning | Procura vulnerabilidades conhecidas como miss configuration e softwares desatualizados | Nessus, OpenVAS, Nikto                      | **Alta:** enviam payloads de exploração que podem ser detectados   |
| Network Mapping        | Mapeia a topologia de rede do alvo, seus dispositivos e seus relacionados              | Traceroute, Nmap                            | **Médio/Alto:** Aumenta o tráfego de rede e pode ser suspeito      |
| Web Spiring            | Mapeia a estrutura do site, páginas, diretórios e arquivos                             | Burp Suite Spider, OWASP ZAP Spider, Scrapy | **Médio/Baixo:** Pode ser detectado se não devidamente configurado |
| Banner Grabbing        | Pega banners exibidos por serviços                                                     | Netcat, curl                                | **Baixo:** Interação mínima                                        |
| OS Fingerprinting      | Identifica o OS                                                                        | Nmap, Xprobe2                               | **Baixa:** Interação mínima                                        |
| Service Enumeration    | Determina a versão dos serviços em execução                                            | Nmap                                        | **Baixa:** Interação mínima                                        |
