## Fuentes de alimentación

Una estación de referencia CORS debe funcionar con una fuente de energía continua y confiable. Tanto la red eléctrica como la energía solar son fuentes de energía primaria adecuadas. La elección entre energía solar y energía primaria de red dependerá del compromiso entre costo, seguridad, disponibilidad y ubicación. Una conexión distante a la red eléctrica puede hacer que la energía solar con un conjunto de baterías sea la opción más económica. Una red eléctrica poco confiable, con importantes fluctuaciones de energía, puede ser causal de preferencia hacia la energía solar, particularmente en áreas rurales.

**Alimentación de red**

Cuando se utilice la red eléctrica, se recomienda un circuito de alimentación específico para el equipo CORS, para reducir el riesgo de que las cargas de energía de otros equipos puedan disparar un disyuntor o un dispositivo de corriente residual e interrumpir la energía al equipo CORS. Es recomendable instalar las tomas de corriente de manera de minimizar la desconexión involuntaria o intencional de la energía al equipo del sitio. Se recomienda instalar protección contra sobretensiones para evitar daños por picos de energía.

**Energía Solar (Photovoltaic)**

La luz solar disponible es el factor clave para el rendimiento en la energía solar. Esta es una función de la latitud y las condiciones climáticas locales. Se puede consultar con las agencias meteorológicas locales sobre el promedio de horas de luz solar disponibles en el área objetivo.

Se requiere un sistema de baterías, para sitios con energía solar y es una fuente de alimentación secundaria común para sitios con energía eléctrica principal. Una fuente de alimentación ininterrumpida (UPS) es una fuente de energía común a corto plazo, que proporciona energía durante el cambio entre las fuentes de energía primaria y secundaria a largo plazo.

Se recomienda una unidad de distribución de energía (PDU) para los sitios CORS. La PDU gestiona y acondiciona el suministro de energía al sitio, a menudo con un mecanismo automático de caída/retroceso para cambiar entre fuentes de energía primaria y secundaria. Una PDU administrada de forma remota controla el sistema de energía dentro de limitaciones preestablecidas y proporciona herramientas, informes y alertas del sistema. Dependiendo de las condiciones ambientales, una PDU también puede apagar y volver a encender equipos menos críticos. Una PDU con un enlace de comunicaciones permite al operador CORS controlar la energía del equipo manualmente desde una ubicación remota.

## Comunicaciones

Un sitio CORS requiere comunicaciones confiables para la transmisión de datos, ya sea directamente a los usuarios o a un centro de datos operativo (ODC). El diseño de este sistema de comunicación es una cuestión central que afecta la transmisión de datos y el control remoto del equipo CORS.

Hay una variedad de opciones de comunicación y proveedores de servicios disponibles. Los sistemas de comunicación comunes para la transmisión de datos entre un sitio CORS y un ODC incluyen:

- ADSL (Línea de abonado digital asimétrica),
- Red de telefonía móvil,
- WAN corporativa (red de área amplia) entre oficinas,
- Enlace satelital de terminal de muy pequeña apertura (VSAT) para ubicaciones remotas.

El diseño del sistema de comunicación depende del ancho de banda de datos requerido, los protocolos de datos utilizados, la latencia aceptable de los datos y los servicios disponibles en el área de destino.

Se recomienda un sistema de comunicación secundario independiente para mejorar la confiabilidad de la estación. Las comunicaciones secundarias son importantes en sitios que ofrecen servicios en tiempo real y en sitios remotos donde el gasto de una visita al sitio excede los costos del sistema de comunicación.

El ancho de banda requerido para la transmisión de datos CORS se ve afectado por una serie de factores que incluyen:

- Operaciones de transmisión normales (es decir, transmisión de datos y descargas de datos regulares),
- Descargas irregulares, como la recuperación de datos almacenados en el receptor después de una interrupción de las comunicaciones,
- Cargas para actualizaciones de firmware del receptor,
- Cargas de ancho de banda adicionales, como soporte al usuario de interfaz gráfica para receptores GNSS, estaciones meteorológicas y dispositivos de administración de red o energía,
- Aumento del volumen general de datos debido a la modernización del GNSS (es decir, señales, satélites y sistemas satelitales adicionales).

Independientemente del método de comunicación utilizado, la latencia de datos desde un sitio CORS hasta el usuario para los servicios de posicionamiento en tiempo real no debe exceder los dos segundos.
