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
