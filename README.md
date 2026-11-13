# Llamada112IA

Entrena la llamada al 112 mientras reanimas, solo con la voz. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/llamada112ia/

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

- Simula, **solo con la voz**, la llamada al 112 ante una parada cardiorrespiratoria en un adulto mientras el estudiante hace compresiones en un maniquí. El estudiante dice «comenzamos», suena el tono de llamada (425 Hz) y contesta un operador simulado.
- Tres escenarios: en casa (con un relevo que llega), polideportivo con desfibrilador (DEA) y en la calle con boqueadas (respiración agónica).
- El operador sigue el protocolo de RCP guiada por teléfono (motivo → dirección → consciencia → respiración → instrucciones → compresiones), corrige como un operador real (dirección incompleta, dudas sobre la respiración, «paro») y anima durante toda la reanimación. Duración configurable de 2 a 6 minutos; al cumplirse, «llega la ambulancia».
- Metrónomo opcional a 110 por minuto. Para terminar antes: «terminar la simulación».
- Informe calculado por el código: explicó qué pasa, dirección completa, confirmó que no responde y no respira con normalidad, tiempo hasta reconocer la parada y hasta la primera compresión (frente a los objetivos de la AHA: < 90 s y < 150 s), continuidad, aviso del DEA o del relevo. Descarga en Word y CSV; historial de intentos en el navegador.
- Ejemplo de demostración sin micrófono ni clave. Español, inglés y portugués.

## Cómo se usa la IA

**Opcional.** Sin clave funciona con el operador de guion. Con la propia clave de OpenAI, Google Gemini o Anthropic Claude, las respuestas del operador las redacta la IA con el mismo protocolo (recortadas a 3 frases); los recordatorios periódicos y el final siguen siendo del guion. La evaluación la hace siempre el código; si la IA falla, continúa el guion. La clave se guarda solo en el navegador.

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

## Cómo citar

Borrás Rocher, F. y Caturla Such, J. (2026). *Llamada112IA* (v1.0.0) [Software]. (DOI en trámite)

## Licencia

MIT. Véase [LICENSE](LICENSE).
