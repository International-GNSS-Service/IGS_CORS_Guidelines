La tabla siguiente ofrece una descripción general de las características recomendadas del receptor a la fecha de publicación de estas Directrices. Las nuevas estaciones GNSS propuestas para el IGS deberán cumplir todas las características enumeradas. Los operadores de estaciones establecidas que no pueden actualizarse, al momento de la publicación de estas guías, deberán tener en cuenta estas recomendaciones para futuras actualizaciones.

### Seguimiento de señal

- Seguimiento del total de la fase portadora disponible, pseudorange y relación señal-ruido (SNR) por frecuencia. Las observaciones Doppler son opcionales.
- Sin suavizado de las mediciones de pseudorange.
- La mitigación multipath debe estar deshabilitada.
- Las estaciones recientemente propuestas deben rastrear al menos GPS, GLONASS, Galileo y BeiDou[^1].
- Se prefiere la capacidad de observar señales futuras.
- Configurar el Receptor para rastrear señales hasta 0° de elevación (5° es aceptable).
- Configurar el Receptor para seguimiento de todos los satélites a la vista (incluidos satélites en mal estado).
- El receptor debe sincronizar el instante real de observación con el tiempo del GPS dentro de 1 milisegundo del segundo completo.

### Salidas

- Actualmente RTCM SC-104 a 1 Hz en múltiples puertos.
- Transmisión de datos crudos en formato propietario.
- Capaz de transmitir datos a múltiples ubicaciones.

### Registro

- Registro continuo de datos crudos sin suavizar.
- Registro de datos RINEX (mínimo: muestreo de 30 segundos, si no se generan fuera del receptor).
- Registro de datos del sensor de entrada.

El firmware de un receptor GNSS es un software informático que controla el seguimiento del dispositivo. Al igual que con cualquier otro software, se puede actualizar el firmware para corregir errores o mejorar las capacidades de seguimiento del receptor. Antes de actualizar, se debe probar minuciosamente el nuevo firmware y solo considerarlo en estaciones donde se beneficie con el cambio. En general, el receptor debe operar con el firmware estable más reciente dentro de los 6 meses posteriores a su lanzamiento.

[^1]: Las estaciones ubicadas en la huella de los sistemas satelitales regionales QZSS e IRNSS realizarán un seguimiento adicional de estos. Se fomenta la capacidad de seguimiento SBAS.
