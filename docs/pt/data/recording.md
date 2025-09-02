O mínimo que uma CORS IGS precisa fornecer são ficheiros de observação RINEX diários com uma taxa de amostragem de 30 segundos. Uma taxa de amostragem de 15 segundos é aceitável, mas não encorajada. Além disso, solicita‑se aos operadores das estações que forneçam ficheiros RINEX de navegação[^1].

Recomenda‑se também fornecer ficheiros RINEX horários com uma taxa de amostragem de 30 segundos. Novas CORS IGS são ainda encorajadas a fornecer, se possível, ficheiros RINEX de alta taxa (1 Hz) com uma duração de 15 minutos.

Cada ficheiro RINEX deve ser enviado para pelo menos dois dos centros de dados globais do IGS[^2]. Se a estação já estiver incluída numa rede regional (por exemplo, APREF, EPN, SIRGAS) e os dados forem públicos, a transmissão para um dos centros de dados globais é suficiente. A transmissão de dados será definida com o Coordenador da Rede IGS.

Após uma interrupção de comunicação, os ficheiros de dados em falta devem ser submetidos aos centros de dados. Deve ser enviada à comunidade uma comunicação explicando os pormenores da interrupção (ver secção [Anúncios](../announcements) para mais informações).

A listagem abaixo apresenta as principais métricas para o rastreamento de sinais, gravação e transmissão de dados que devem ser cumpridas por cada CORS IGS.

**Rastreamento de Sinais e Arquivo de Dados**

- 99% das épocas disponíveis num dia são completamente observadas, registadas e arquivadas (<15 minutos de interrupção por dia).
- 99% das épocas disponíveis num ano são completamente observadas, registadas e arquivadas (<91 horas de interrupção total por ano).

**Transmissão de Dados**

- A latência de um ficheiro de dados horário para arquivo deve ser <5 minutos após o final de cada hora.
- A latência de um ficheiro de dados diário para arquivo deve ser <30 minutos após o final do dia.

**Reenvio após Interrupção**

- Todos os ficheiros diários em falta devem ser reenviados o mais rapidamente possível.
- Os ficheiros horários em falta devem ser reenviados pelo menos para os últimos três dias completos.

## Dados de Alta Taxa

Em apoio a aplicações em Quase Tempo-Real (NRT), os operadores das estações são encorajados a fornecer ficheiros RINEX de observação e navegação de 15 minutos com uma frequência de 1 Hz (quando aplicável). Podem ser gerados a partir de fluxos em tempo real ou registados pelo recetor.
As estações que participam na provisão de dados de alta taxa são encorajadas a fornecer os ficheiros com um atraso de 5 minutos ou menos desde a última época de observação registada.

## Dados em Tempo Real

Além de cumprir as normas de uma estação IGS convencional, as estações de Tempo Real (RTK) devem transmitir dados de observação GNSS com um intervalo mínimo de 1 Hz. Todas as novas estações IGS devem ser capazes de transmitir dados em tempo real, excepto se forem consideradas valiosas para contribuir para a realização do referencial (por exemplo, por estarem colocalizadas com uma estação SLR ou VLBI) ou se estiverem localizadas numa região onde não existem outras estações IGS.
As recomendações que devem ser cumpridas por uma estação CORS IGS RTK são descritas na secção 2 das [Guidelines for IGS Real‑Time Broadcasters and Stations](https://files.igs.org/pub/resource/guidelines/Guidelines_for_IGS_Real_Time_Broadcasters_and_Stations.pdf).

## Dados Meteorológicos

Recomenda‑se instalar equipamento meteorológico preciso numa CORS IGS. As Diretrizes específicas para sensores são descritas na secção [Sensores Meteorológicos](../equipment/meteo_sensors.md). No mínimo, os dados devem incluir medições de pressão e temperatura e devem ser distribuídos no formato RINEX. Os ficheiros RINEX de navegação devem ser transmitidos segundo a mesma periodicidade que os ficheiros RINEX de observação (horários e/ou diários).

[^1]: Para reduzir o número de ficheiros, recomenda‑se enviar ficheiros de navegação mistos que contenham todos os dados de navegação num único ficheiro.
    
[^2]: Uma lista dos centros de dados globais do IGS pode ser encontrada no site do IGS: [https://igs.org/data-access/#data-centers](https://igs.org/data-access/#data-centers)
