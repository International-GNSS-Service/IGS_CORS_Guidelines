La calibración absoluta de la antena GNSS de la estación debe estar disponible en el [formato IGS ANTEX vigente](https://files.igs.org/pub/data/format/antex14.txt). Este archivo contiene calibraciones a modelos específicos de antena. Aunque el uso de calibraciones de tipo promedio es el estándar actual en el análisis IGS, también se prefiere calibrar individualmente cada antena GNSS utilizada en la red IGS. Se recomienda que las nuevas antenas se calibren mediante un robot o en una cámara. Para que las calibraciones de la antena sean válidas, la antena GNSS debe estar orientada al Norte Verdadero con una precisión de ±5°. No se deben utilizar modelos de calibración de antena relativos.

La antena GNSS debe fijarse de forma rígida y segura a la parte superior del monumento de la estación como se describe en la sección [Estabilidad del Sitio](../../establishment/stability).

Las excentricidades entre el pilar y el Punto de Referencia de la Antena (ARP) deben ser medidas y reportadas en los registros del sitio IGS (IGS log file) y en los encabezados del archivo RINEX con una precisión de ≤1 mm. Se prefiere una excentricidad horizontal de 0 m.

Se recomienda el uso de antenas choke-ring. Estas tienen propiedades muy estables y reconocidas, con una alta mitigación de multipath.

Se desaconseja el uso de protectores (radomos). Aunque brindan cierto nivel de protección, los radomos alteran la ubicación del Centro de Fase de la Antena (APC). Peor aún, dado que la luz ultravioleta afecta las propiedades materiales del radomo, su impacto en la ubicación del APC varía. Sin embargo, las condiciones ambientales como la nieve, el rocío del mar o la posibilidad de que la antena sea utilizada como posadero por aves pueden requerir el uso de un radomo. En este caso, la combinación antena/radomo debe tener una calibración de antena válida. No se deben utilizar radomos cónicos. No retirar los radomos de las antenas GNSS existentes.

La experiencia demuestra que cuando se retira y reemplaza una antena GNSS, se produce un cambio en la posición calculada del sitio, incluso cuando el ARP se reemplaza con precisión. Por lo tanto, no retire la antena por ningún motivo que no sea una falla de hardware o para realizar las inspecciones de conexión locales necesarias. Por esta última razón es obligatorio reflejar esto en los metadatos de la estación. En caso de necesitar cambiar la antena, se debe avisar a los usuarios y centros de análisis (ver apartado [Anuncios](../../data/announcements)).

Elija antenas que sean capaces de rastrear tantas señales GNSS como las posibles en el momento de la compra para reducir la necesidad de quitar una antena para rastrear señales GNSS recientemente disponibles. Para evitar confusiones, en los encabezados y metadatos del archivo RINEX se debe utilizar la [convención de nomenclatura estándar IGS para los modelos de antena](https://files.igs.org/pub/station/general/rcvr_ant.tab).

### Tipo de Antena

- No se permite el uso de antenas únicas ("desconocidas"). Preferiblemente uso de antena choke-ring con elementos Dorne-Margolin.
- Las capacidades de seguimiento de señales satelitales de la antena deben igualar o superar la capacidad del receptor GNSS. Para estaciones nuevas este requisito es obligatorio.
- La antena y los conectores de antena deben ser impermeables a la intemperie y resistentes a la corrosión.

### Calibraciones

- Todas las antenas IGS deberán tener una calibración de antena absoluta IGS válida. Si una antena se calibra individualmente, el archivo ANTEX correspondiente debe estar disponible para IGS.
- Las antenas deben estar calibradas por robot o por una cámara.

### ARP y Excentricidades

- Todas las mediciones de compensación de antena (antenna-offset) se referirán al ARP.
- Las excentricidades (Este, Norte, Arriba) de la antena se deben medir desde el marcador de posición permanente hasta el ARP y se deben informar en los metadatos y encabezados del archivo RINEX con una precisión ≤ 1 mm.

### Radome (cobertor protector de antena)

- Se desaconseja fuertemente el uso de un radomo.
- Si el uso de un radomo es absolutamente necesario, se recomienda el uso de un radomo hemisférico con una calibración de antena absoluta válida.
- No utilizar radomos cónicos.

### Orientación de la Antena

- La antena debe estar orientada al Norte Verdadero con una precisión de ±5°.
- Si la desviación es superior a 5°, la orientación real debe informarse en los metadatos.
