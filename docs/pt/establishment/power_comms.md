## Fonte de Alimentação

Cada estação CORS precisa de ter uma fonte de energia contínua e fiável. Tanto a alimentação pela rede como a energia solar são fontes primárias adequadas. A escolha entre energia solar e rede como fonte principal é determinada pelo equilíbrio entre custo, segurança, disponibilidade e localização. Uma ligação distante à rede eléctrica pode tornar a energia solar associada a um conjunto de baterias uma escolha mais económica. Uma alimentação de rede pouco fiável, com flutuações de energia significativas, também pode tornar a energia solar preferível.

**Alimentação da Rede**

Quando é utilizada alimentação da rede, recomenda‑se um circuito dedicado para o sistema CORS para reduzir o risco que sobrecargas de outros equipamentos possam acionar disjuntores e interromperem a energia do sistema CORS. Deve serem instaladas tomadas próprias de forma a minimizar a desconexão inadvertida ou intencional da alimentação do equipamento. Recomenda-se a instalação de dispositivos de proteção contra sobretensões de modo a prevenir danos decorrentes de picos de tensão.

**Energia Solar (Fotovoltaica)**

A luz solar disponível é o factor fundamental para o desempenho solar. Este factor depende da latitude e das condições climáticas locais. Pode consultar as agências meteorológicas locais para obter as horas médias de luz solar disponíveis na área de interesse.

É necessário um sistema de baterias para sítios alimentados a energia solar, que pode constituir uma fonte de energia secundária em locais com alimentação de rede primária. Uma Fonte de Alimentação Ininterrupta (UPS) destina-se apenas a funcionar como reserva de curto prazo perante falhas momentâneas ou quedas de tensão, não devendo ser considerada um substituto de um sistema de alimentação secundária de longo prazo, como uma instalação solar com baterias.

Recomenda-se a utilização de uma Unidade de Distribuição de Energia (PDU) em estações CORS. A PDU gere e condiciona o fornecimento de energia ao local, frequentemente com mecanismos automáticos de comutação entre as fontes primária e secundária. Uma PDU com gestão remota permite controlar o sistema de energia dentro de limites pré-definidos e disponibiliza ferramentas, relatórios e alertas. Dependendo das condições ambientais, a PDU pode também desligar e voltar a ligar equipamentos menos críticos. Uma PDU com ligação de comunicações permite ao operador da estação GNSS controlar remotamente a alimentação dos equipamentos.

## Comunicações

Uma estação CORS requer comunicações fiáveis para a transmissão de dados, quer directamente para os utilizadores, quer para um Centro de Dados Operacional (ODC). O design deste sistema de comunicação é uma questão central que afecta a transmissão de dados e o controlo remoto do equipamento da estação.

Existe uma gama de opções de comunicação e prestadores de serviços disponível. Os sistemas de comunicação comuns para a transmissão de dados entre uma estação CORS e um ODC incluem:

- ADSL (Asymmetric Digital Subscriber Line),
- Rede móvel,
- Rede WAN (Wide Area Network) entre escritórios,
- Ligação por satélite (e.g., VSAT) em locais remotos.

O design do sistema de comunicação depende da largura de banda de dados necessária, dos protocolos de dados utilizados, da latência de dados aceitável e dos serviços disponíveis na área pretendida.

Recomenda‑se um sistema de comunicação secundário independente para melhorar a fiabilidade do sítio. As comunicações secundárias são importantes em estações que oferecem serviços em tempo real e em sítios remotos onde o custo de uma visita ao local excede os custos do sistema de comunicação.

A largura de banda requerida para a transmissão de dados de uma CORS é influenciada por vários factores, incluindo:

- Operações normais de transmissão (ou seja, streaming de dados e downloads regulares de dados),
- Downloads irregulares, como a recuperação de dados armazenados no recetor após uma interrupção de comunicação,
- Uploads para actualizações de firmware do recetor,
- Requisitos adicionais de largura de banda, como acesso à interface gráfica dos recetores GNSS, estações meteorológicas e dispositivos de gestão de rede ou de energia,
- Aumentos globais no volume de dados devido à modernização do GNSS (ou seja, sinais, satélites e sistemas adicionais).

Independentemente do método de comunicação utilizado, a latência dos dados de uma estação CORS até ao utilizador para serviços de posicionamento em tempo real não deve exceder dois segundos.
