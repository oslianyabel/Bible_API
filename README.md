# AI Assistant API

## Descripción

Este proyecto proporciona una API que sirve como intermediaria entre una aplicación web o un bot de Telegram y una Inteligencia Artificial centralizada, conocida como "IA madre". La API permite enviar mensajes desde la web o Telegram y recibir respuestas contextuales en formato de texto. La inteligencia detrás de estas respuestas se basa en el contexto de las interacciones previas, asegurando que las respuestas sean relevantes y coherentes.

## Características

- **Conexión Web y Telegram**: La API permite la integración tanto con aplicaciones web como con bots de Telegram, facilitando el acceso a las capacidades de la IA desde múltiples plataformas.
- **Respuestas Contextuales**: La IA madre procesa el contexto de las conversaciones anteriores para generar respuestas precisas y coherentes.
- **Formato de Respuesta en Texto**: Las respuestas de la IA son devueltas en formato de texto, lo que simplifica la integración en diferentes interfaces de usuario.
- **Escalabilidad**: Diseñada para manejar múltiples solicitudes simultáneamente, ideal para aplicaciones con gran volumen de usuarios.
- **Fácil Implementación**: La API está diseñada para ser fácil de integrar con cualquier sistema, proporcionando endpoints claros y bien documentados.

## Diagrama

![App Screenshot](https://back.jumotech.com/uploads/API_endpoint_e72e3f0447.png)

## Endpoints

### `POST /api/chat`

**Descripción:** Envía un mensaje a la IA y recibe una respuesta basada en el contexto.

- **Parámetros de la solicitud:**
  - `platform` (string): Indica la plataforma desde donde se envía el mensaje (`web`, `telegram`, etc.).
  - `user_id` (string): Identificador único del usuario que envía el mensaje.
  - `message` (string): El mensaje que se quiere enviar a la IA.
  - `context` (string, opcional): Contexto adicional para ayudar a la IA a generar una respuesta más precisa.

- **Ejemplo de solicitud:**
  ```json
  {
    "platform": "telegram",
    "user_id": "12345",
    "message": "¿Cuál es el estado del proyecto?",
    "context": "estado del proyecto actual"
  }


