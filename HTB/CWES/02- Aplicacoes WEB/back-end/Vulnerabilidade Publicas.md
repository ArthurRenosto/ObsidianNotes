Identificamos a versao dos componentes da aplicacao web e depois procuramos exploits para ela

procuramos por bancos de dados com exploits publicos e buscamos por vulnerabilidades com pontuacao 8-10 que geralmente sao RCE

# Sistema de pontuacao de vulnerabilidades (CVSS)

O [Common Vulnerability Scoring System (CVSS)](https://en.wikipedia.org/wiki/Common_Vulnerability_Scoring_System) é um padrão de código aberto da indústria para avaliar a gravidade das vulnerabilidades de segurança. Este sistema de pontuação é frequentemente usado como uma medição padrão para organizações e governos que precisam produzir pontuações de gravidade precisas e consistentes para as vulnerabilidades de seus sistemas. Isso ajuda na priorização de recursos e na resposta a uma determinada ameaça.

As pontuações do CVSS são baseadas em uma fórmula que usa várias métricas: `Base`, `Temporal`, e `Environmental`. Ao calcular a gravidade de uma vulnerabilidade usando CVSS, o `Base`métricas produzem uma pontuação que varia de 0 a 10, modificada pela aplicação `Temporal`e `Environmental`métricas. O [National Vulnerability Database (NVD)](https://nvd.nist.gov) fornece pontuações CVSS para quase todas as vulnerabilidades conhecidas e divulgadas publicamente. Neste momento, o NVD só fornece `Base`pontuações baseadas nas características inerentes de uma determinada vulnerabilidade. Os atuais sistemas de pontuação em vigor são CVSS v2 e CVSS v3. Existem várias diferenças entre os sistemas v2 e v3, nomeadamente alterações ao `Base`e `Environmental`grupos para contabilizar métricas adicionais. Mais informações sobre as diferenças entre os dois sistemas de pontuação podem ser encontradas [aqui](https://www.balbix.com/insights/cvss-v2-vs-cvss-v3).

