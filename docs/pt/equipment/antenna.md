A calibração absoluta da antena GNSS da estação deve estar disponível no [formato ANTEX actual do IGS](https://files.igs.org/pub/data/format/antex14.txt). Este ficheiro contém calibrações por modelo de antena. Embora a utilização de calibrações médias por tipo de antena seja a norma actual nas análises do IGS, é preferível calibrar individualmente cada antena GNSS utilizada na rede do IGS. Recomenda‑se que as novas antenas sejam calibradas por robot ou em câmara anecoica. Para que a calibração da antena seja válida, a antena deve ser orientada para o Norte verdadeiro com uma precisão de ±5°. Modelos de calibração relativos não devem ser utilizados.

A antena GNSS deve estar fixada de forma rígida e segura ao topo do monumento da estação, conforme descrito na secção [Estabilidade do Local](../../establishment/stability).

As excentricidades entre o Marco (ponto de referência da estação) e o Ponto de Referência da Antena (ARP) devem ser medidas e comunicadas no registo da estação IGS e nos cabeçalhos RINEX com uma precisão ≤ 1 mm; uma excentricidade horizontal de 0 m é preferível.

O uso de antenas choke‑ring é recomendado. Têm propriedades muito estáveis e bem compreendidas, com elevada mitigação de multitrajetos.

O uso de radomes é desencorajado. Embora ofereçam algum nível de protecção contra as intempéries, os radomes alteram a localização do Centro de Fase da Antena (APC). Pior ainda, como a luz ultravioleta afecta as propriedades do material do radome, o seu impacto na localização do APC varia. No entanto, condições ambientais como queda de neve, maresia ou a probabilidade de a antena servir de poleiro para aves podem exigir o uso de um radome. Nesse caso, a combinação antena/radome deve ter uma calibração de antena válida. Não devem ser utilizados radomes cónicos. Não devem ser removidos os radomes de antenas GNSS existentes.

A experiência mostra que, quando uma antena GNSS é retirada e recolocada, ocorre uma alteração na posição calculada da estação mesmo quando o ARP é recolocado de forma precisa. Portanto, não retire a antena por qualquer razão que não seja falha de hardware ou para realizar levantamentos locais necessários. É obrigatório registar qualquer operação na antena nos metadados da estação. Se precisar de mudar a antena, os utilizadores e os centros de análise devem ser avisados previamente (ver secção [Anúncios](../../data/announcements)).

Escolha antenas capazes de rastrear o maior número possível de sinais GNSS planeados no momento da compra para reduzir a necessidade de remover uma antena para rastrear novos sinais GNSS. Para evitar confusão, a convenção de nomenclatura padrão do IGS para [modelos de antenas](https://files.igs.org/pub/station/general/rcvr_ant.tab) deve ser utilizada nos cabeçalhos RINEX e nos metadados da estação.

### Tipo de Antena

- O uso de antenas desconhecidas (não listadas no ficheiro ANTEX do IGS) não é permitido. O uso de antenas choke‑ring com elementos Dorne‑Margolin é preferido.
- As capacidades de rastreamento da antena devem corresponder ou exceder a capacidade do recetor GNSS. Para novas estações este requisito é obrigatório.
- A antena e os conectores devem ser à prova de intempéries e resistentes à corrosão.

### Calibrações

- Todas as antenas IGS devem ter uma calibração absoluta válida no ficheiro ANTEX do IGS. Se uma antena for calibrada individualmente, o ficheiro ANTEX correspondente deve ser disponibilizado ao IGS.
- As antenas devem ser calibradas por robot ou em câmara anecoica.

### ARP e Excentricidades

- Todas as medições de deslocamento da antena devem referir‑se ao ARP.
- As excentricidades (Este, Norte, Vertical) do ponto de referência da estação até ao ARP devem ser medidas e registadas nos metadados e nos cabeçalhos RINEX com uma precisão ≤ 1 mm.

### Radome

- O uso de radomes é fortemente desencorajado. Se o uso de um radome for absolutamente necessário, recomenda‑se a utilização de um radome hemisférico com uma calibração de antena válida.
- Não utilizar radomes cónicos.

### Orientação da Antena

- A antena deve ser orientada para o Norte verdadeiro com uma precisão de ±5°.
- Se a orientação diferir mais de 5°, a orientação real deve ser indicada nos metadados.
