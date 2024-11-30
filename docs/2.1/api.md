# API

Rutas API de Novo SGA.

| Método | URI | Descripción |
| --- | --- | --- |
| POST | /api/token | Autentica al usuario devolviendo el token de acceso. |
| GET | /api/unidades | Devuelve todas las unidades disponibles. |
| GET | /api/prioridades | Devuelve todas las prioridades disponibles. |
| GET | /api/servicos | Devuelve los servicios globales. |
| GET | /api/locais | Devuelve los locales de atención. |
| GET | /api/usuarios | Devuelve los usuarios del sistema. |
| POST | /api/distribui | Genera un nuevo turno de atención. Requiere autenticación, un access_token válido y activo. |
| GET | /api/print | Imprime el ticket de un turno ya generado. Requiere autenticación, un access_token válido y activo, un hash. |
