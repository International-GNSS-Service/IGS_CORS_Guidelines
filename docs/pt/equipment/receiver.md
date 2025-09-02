A listagem abaixo fornece uma visão geral das características recomendadas para os recetores GNSS na data de emissão destas Diretrizes. As novas estações GNSS propostas para o IGS devem satisfazer todas as características listadas. Os operadores de estações já estabelecidas, que não possam ser atualizadas no momento, deverão ter em consideração estas recomendações para futuras atualizações.

### Rastreamento de Sinais

- Devem ser rastreados todos os sinais de fase de portadora, de pseudo‑distância e as relações sinal‑ruído (SNR) disponíveis em todas as frequências. As observações de Doppler são opcionais.
- A suavização das medições de pseudo‑distância deve ser desactivada.
- A mitigação de multitrajetos deve ser desactivada.
- As novas estações devem rastrear pelo menos GPS, GLONASS, Galileo e BeiDou[^1].
- É recomendada a capacidade de poder observar sinais futuros.
- O recetor deve ser configurado para rastrear sinais desde 0° de elevação (5° é aceitável).
- O recetor deve ser configurado para rastrear todos os satélites visíveis (incluindo satélites não saudáveis).
- O recetor tem de sincronizar o instante real de observação com o tempo GPS com uma precisão de 1 milissegundo em relação ao segundo inteiro.

### Saída

- Protocolo RTCM SC‑104 a 1 Hz em várias portas.
- Transmissão de dados brutos proprietários.
- Capacidade de transmitir dados para múltiplos destinos.

### Registo

- Registo contínuo de dados brutos não suavizados.
- Registo de dados RINEX (amostragem mínima: 30 segundos), se não forem gerados externamente ao recetor.
- Registo de dados dos sensores de entrada.

O firmware de um recetor GNSS é um software que controla o rastreamento do dispositivo. Tal como qualquer outro software, um firmware pode ser actualizado para corrigir erros ou melhorar as capacidades de rastreamento do recetor. Em termos gerais, o recetor deve ser operado com a versão estável mais recente do firmware no prazo de 6 meses após a sua disponibilização.

[^1]: As estações localizadas na área de cobertura dos sistemas de satélites regionais QZSS e IRNSS devem também rastrear esses sistemas. A capacidade de rastreamento SBAS é encorajada.
