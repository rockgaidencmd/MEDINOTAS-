# MEDINOTAS 360 — prototipo v0.3

Aplicación estática de demostración con ocho expedientes ficticios, indicaciones, propuestas de cambio, historial, grabación o carga de audios de prueba y simulación de egresos.

## Uso

Abrir `index.html` desde un servidor HTTPS (por ejemplo Vercel). El micrófono requiere HTTPS y permiso del navegador.

## Límites importantes

- Solo datos ficticios: **NO usar historias clínicas, fotos o audios reales**.
- Sin cuentas, sin servidor, sin IA ni transcripción automática.
- Indicaciones e historial guardados únicamente en `localStorage` del dispositivo.
- Los audios permanecen temporalmente en memoria y se pierden al recargar o cerrar.
- No es un dispositivo médico ni una historia clínica electrónica.
- Toda validación es una simulación, no una orden médica.

## Publicación

Importar el repositorio en Vercel como sitio estático, sin comando de build. El repositorio es público: no subir información de pacientes ni credenciales.
