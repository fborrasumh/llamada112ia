# Llamada112IA

Entrena la llamada al 112 mientras reanimas, solo con la voz. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/llamada112ia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.24209094.svg)](https://doi.org/10.5281/zenodo.24209094)

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

- Simula, **solo con la voz y con el móvil en manos libres**, la llamada al 112 ante una parada cardiorrespiratoria en un adulto mientras el estudiante hace compresiones en un maniquí. El estudiante dice «comenzamos», suena el tono de llamada (425 Hz) y contesta un operador simulado.
- Quien llama es un **ciudadano formado en soporte vital básico con DESA**: ya ha valorado la consciencia y la respiración y ha abierto la vía aérea, así que el operador recoge el motivo y la dirección y pasa directamente a las compresiones torácicas, con instrucciones breves.
- Dos escenarios: **domicilio** (antes de llegar la ambulancia, el operador pide abrir la puerta del portal y la de casa y volver a las compresiones) y **polideportivo con DESA** (el DESA, con voz propia, pide los parches, analiza, indica «ritmo desfibrilable» y la descarga; el estudiante debe decir «¡apartaos!», comprobar que nadie toca a la víctima y decir «descarga»).
- El operador corrige como uno real (dirección incompleta, «paro», descarga sin medida de seguridad) y anima durante toda la reanimación. La llamada dura 3 minutos; al cumplirse, «llega la ambulancia». Metrónomo opcional a 110 por minuto (calla durante el análisis y la descarga). Para terminar antes: «terminar la simulación».
- Informe calculado por el código: explicó qué pasa, informó de que no responde y no respira, dirección completa, tiempo hasta reconocer la parada y hasta la primera compresión (frente a los objetivos de la AHA: < 90 s y < 150 s), continuidad, aviso de la llegada del DESA, medida de seguridad y descarga, apertura de las puertas. Descarga en Word y CSV; historial de intentos en el navegador.
- Ejemplo de demostración sin micrófono ni clave. Español, inglés y portugués.

## Cómo se usa la IA

**Opcional.** Sin clave funciona con el operador de guion. Con la propia clave de OpenAI, Google Gemini o Anthropic Claude, las respuestas del operador las redacta la IA con el mismo protocolo (recortadas a 3 frases); la voz del DESA, el aviso de las puertas, los recordatorios periódicos y el final siguen siendo del guion. La evaluación la hace siempre el código; si la IA falla, continúa el guion. La clave se guarda solo en el navegador.

## Privacidad

Los informes se guardan solo en el navegador (IndexedDB). El reconocimiento de voz lo hace el navegador: en Chrome y Edge el audio se procesa en los servidores de Google o Microsoft. En el modo con IA, la transcripción de lo que dice el estudiante sale hacia su proveedor, tras un aviso previo con muestra. Se recomienda usar solo los datos ficticios del escenario.

## Límites

- No mide la profundidad, el ritmo ni la posición de las manos: para eso hace falta un maniquí con retroalimentación o un instructor.
- La evaluación se basa en palabras clave de la transcripción; el reconocimiento de voz puede equivocarse. Revisa la conversación del informe.
- Reconocimiento de voz: Chrome y Edge (escritorio y Android); Safari irregular; Firefox no (se puede practicar escribiendo).
- Hace falta un toque inicial («Preparar la llamada») porque el navegador lo exige para el micrófono y el sonido.
- No sustituye un curso de soporte vital básico. Las direcciones de los escenarios son ficticias.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Juan Manuel Caturla Such (Universidad Miguel Hernández de Elche).


ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

## Cambios

- **1.1.0** — Tras la evaluación con el profesorado: reanimador formado en SVB con DESA (sin preguntas de consciencia, respiración ni vía aérea; compresiones directas con instrucciones breves); escenario «Domicilio» con apertura de puertas; DESA simulado por voz con medida de seguridad y descarga; se retira el escenario de la calle; duración fija de 3 minutos; nuevo título «Llamar al 112 con manos libres (móvil)».
- **1.0.0** — Primera versión.

## Cómo citar

Borrás Rocher, F. y Caturla Such, J. (2026). *Llamada112IA* (v1.1.0) [Software]. DOI: [10.5281/zenodo.24209094](https://doi.org/10.5281/zenodo.24209094)

## Licencia

MIT. Véase [LICENSE](LICENSE).
