Lo mínimo que una estación IGS CORS debe proporcionar son archivos de observación RINEX diarios con una frecuencia de muestreo de 30 segundos. Una frecuencia de muestreo de 15 segundos es aceptable, pero no recomendada. Además, se solicita a los operadores de estaciones que proporcionen archivos de navegación RINEX[^1].

Se recomienda proporcionar archivos RINEX cada hora con una frecuencia de muestreo de 30 segundos. Se alienta a las estaciones IGS recientemente propuestas a proporcionar archivos RINEX cada hora con una frecuencia de muestreo de 30 segundos y en caso de ser posible, archivos RINEX de alta frecuencia (1 Hz) con una duración de 15 minutos.

Cada archivo de datos RINEX debe enviarse al menos, a dos centros de datos globales de IGS[^2]. Si la estación ya está incluida en una red regional (por ejemplo, APREF, EPN, SIRGAS) y los datos están disponibles públicamente, es suficiente la transmisión a un centro de datos global. La transmisión de datos se coordinará a través del Coordinador de la Red IGS.

Después de una interrupción de la comunicación, los archivos de datos faltantes deben enviarse al(los) centro(s) de datos. Se debe enviar un anuncio explicando los detalles de la interrupción a la comunidad (ver la sección [Anuncios](../announcements) para más información).

La siguiente tabla destaca las cifras claves para el seguimiento de señales, el registro y la transmisión de datos que debe tener como objetivo cada estación IGS CORS.

**Seguimiento de señales y archivado de datos**

- El 99% de las épocas disponibles en un día deben ser completamente observadas, registradas y archivadas (<15 minutos de interrupción por día).
- El 99% de las épocas disponibles en un año deben ser completamente observadas, registradas y archivadas (<91 horas de interrupción total por año).

**Transmisión de datos**

- La latencia para archivar un archivo de datos horario debe ser <5 minutos después del final de cada hora.
- La latencia para archivar un archivo de datos diario debe ser <30 minutos después del final del día.

**Reenvío después de una interrupción**

- Todos los archivos diarios que faltan deben volver a enviarse lo antes posible.
- Los archivos horarios que faltan deben volver a enviarse como mínimo para los últimos tres días completos.

## Datos de alta frecuencia

Para respaldar las aplicaciones en Tiempo Casi Real (NRT), se recomienda a los operadores de estaciones que proporcionen archivos RINEX de observación y navegación de 15 minutos con una frecuencia de datos de 1 Hz (si corresponde). Estos archivos pueden ser generados a partir de transmisiones en tiempo real o ser registrados por el receptor.

Se recomienda a las estaciones que participan en el suministro de datos de alta frecuencia, que proporcionen los archivos con un retraso de 5 minutos o menos desde la última época de observación registrada.

## Datos a tiempo real

A demás de cumplir con los estándares de una estación IGS convencional, las estaciones en tiempo real deben transmitir datos de observación GNSS con un intervalo de datos mínimo de 1 Hz. Todas las estaciones IGS recientemente propuestas deben poder transmitir datos en tiempo real a menos que se consideren valiosas para contribuir al marco de referencia (por ejemplo, al estar ubicadas junto a una estación SLR o VLBI) o estén ubicadas en una región de necesidad geográfica.

Las recomendaciones que debe cumplir una estación IGS en tiempo real se describen en la sección 2 de las [Guidelines for IGS Real-Time Broadcasters and Stations](https://files.igs.org/pub/resource/guidelines/Guidelines_for_IGS_Real_Time_Broadcasters_and_Stations.pdf).

## Datos Meteorológicos

Se recomienda instalar equipos meteorológicos precisos en una estación IGS CORS. Las pautas específicas del sensor se describen en la Sección [Sensores Meteorológicos](../equipment/meteo_sensors.md). Como mínimo, los datos deberán incluir mediciones de presión atmosférica y temperatura y se distribuirán en formato RINEX. Los archivos RINEX meteorológicos deben transmitirse en el mismo horario que los archivos de observación RINEX (cada hora y/o diariamente).

[^1]: Para reducir la cantidad de archivos, se recomienda enviar archivos de navegación mixtos que contengan todos los datos de navegación en un solo archivo.
[^2]: Se puede encontrar una lista de los centros de datos globales de IGS en el sitio web de IGS: [https://igs.org/data-access/#data-centers](https://igs.org/data-access/#data-centers)
