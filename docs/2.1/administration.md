# Administración

## Sistema

Configuración global del sistema. En esta sección es posible reiniciar todos los turnos (archivándolos en el historial) y/o eliminar todos los datos de atención para un nuevo inicio del sistema.

## Unidades

Registro de las unidades de atención del sistema. Unidad de atención es el lugar físico donde se realiza la atención. Por ejemplo: una unidad de salud, un departamento de atención al cliente, o un local comercial.

## Servicios

Registro de los servicios que son realizados en el sistema. Se trata de un registro global, que puede estar disponible o no en las diferentes unidades registradas. Un mismo servicio puede ser atendido en más de una unidad.

## Perfiles

Registro de los perfiles de aceso al sistema. Un perfil define a qué módulos tiene acceso cada usuario. Al usuario se le asigna un perfil a través de la `dotación`, que es la configuración de acceso de un usuario a una `unidad` para el `perfil` elegido.

## Prioridades

Registro de las prioridades de atención. Por defecto existen dos prioridades registradas: `Sin prioridad` y `Prioridad`. Cada prioridad posee un campo `peso` que influye en el orden de la fila. Siendo por defecto `Sin prioridad` peso `0` y `Prioridad` peso `1`.

## Locales

Registro de los lugares desde donde el agente realiza su atención. El local sirve para orientar al cliente, indicándole hacia dónde debe dirigirse al ser llamado. Por ejemplo: consultorio, puesto, caja.

## Módulos

Visualización de los módulos disponibles. Es posible habilitar o desabilitar los módulos instalados.

## Web API

Registro de los clientes `OAuth2` para la integración con otras aplicaciones a través de la API web del sistema.
