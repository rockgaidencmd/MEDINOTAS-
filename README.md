# MEDINOTAS 360 — prototipo experimental

Aplicación estática para **pacientes ficticios únicamente**. Permite simular ocho camas, episodios independientes, indicaciones, borradores de cambios, historial, grabación temporal de audio y dictado de voz a texto en vivo.

## Dictado experimental

La opción «Dictar texto» utiliza Web Speech API del navegador cuando está disponible. No transcribe audios ya grabados ni adjuntos. Algunos navegadores procesan voz en servidores externos: **no introducir datos de pacientes reales**. Requiere micrófono y normalmente HTTPS. Revisar nombres de medicamentos, cantidades y negaciones. Los textos se guardan en el almacenamiento local del navegador, sin sincronización ni respaldo.

## Límites de seguridad

- Sin autenticación, autorización, auditoría, cifrado de datos clínicos ni backend.
- Audios de grabación temporales en memoria: se pierden al recargar la página.
- Dictado no es transcripción clínica validada, no es IA que interpreta órdenes, y no crea órdenes automáticamente.
- No apto para uso asistencial. No introducir historias clínicas, fotografías ni audios identificables.

## Despliegue

Sitio HTML estático: importar el repositorio en Vercel con preset «Other», sin build.

## Whisper experimental en navegador

En la lista de audios, pulsa «Transcribir con Whisper (prueba)». Se utiliza @huggingface/transformers 3.8.1 desde jsDelivr y el modelo onnx-community/whisper-tiny (cuantizado, WASM). La primera ejecución requiere descargar código y pesos; puede consumir mucha memoria/datos y fallar en Android. Esta implementación **no está validada en el dispositivo del usuario**. No es procesamiento en segundo plano: mantén la pestaña abierta. Los audios permanecen en memoria y desaparecen al recargar. La cancelación descarta resultados pero puede no interrumpir inmediatamente una inferencia en ejecución. Solo usar datos ficticios.
