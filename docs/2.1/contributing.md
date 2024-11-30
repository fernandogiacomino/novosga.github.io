# Guía de contribución

Hay varias formas de contribuir con NovoSGA:

## Reportando Problemas

- Ingrese a la sección Issues del repositorio.
- Verifique si el problema ya fue reportado para evitar duplicados.
- Ofrezca el máximo de información posible sobre el problema, incluyendo:
    - Versión de NovoSGA
    - Sistema operativo y versión de PHP
    - Pasos para reproducir el problema
    - Logs y screenshots, si es posible


## Sugerencias de Mejoras y Funciones

Se usted tiene alguna idea de nuevas funcionalidades o mejoras, habra una Issue de sugerencia con una descripción detallada. Discuta su idea con la comunidad para ponerse de acuerdo antes de iniciar el desarrollo.


## Respondiendo dudas

Ayude a otros usuarios respondiendo dudas sobre el uso o la instalación del sistema.

- [Foro de discusión](https://discuss.novosga.org/)
- [Grupo de Telegram](https://t.me/novosga)

## Documentación

Cree que falta alguna información importante sobre el sistema, o falta claridad en la documentación de Novo SGA? Ayude a vovler nuestra documentación más clara e integral.

Al final de cada página hay un link para realizar la edición de la misma. En caso que desee solicitar una nueva sección, basta con abrir un nuevo Pull Request en el siguiente repositorio:

https://github.com/novosga/novosga.github.io/

Toda la documentación queda en la ruta `/docs`.


## Desarrollo

### Pre-requisitos

Para comenzar, verifique si posee los siguientes pre-requisitos:

- **Git**: para control de versión
- **Composer**: para gestionar dependencias PHP
- **PHP**: verifique la versión definida en el archivo `composer.json`

### Proceso de Contribución

#### 1. Crie o fork do repositório

Haga click en "Fork" en la página de [NovoSGA](https://github.com/novosga/novosga) para crear una copia del repositorio en su cuenta de GitHub.

#### 2. Clone el repositorio Forkado

Clone el repositorio en su máquina local usando el siguiente comando:

```bash
git clone https://github.com/seu-usuario/novosga.git
cd novosga
```

#### 3. Cree un branch

Use branches para cada alteración o mejora. El nombre del branch debe ser descriptivo sobre lo que está sendo feito:

```bash
git checkout -b mi-contribución
```

#### 4. Instale dependencias

Asegúrese que todas las dependencias están instaladas.

```bash
composer install
```

#### 5. Implemente los cambios

Haga los cambios necesarios en el código y escriba testeos que cubran las funcionalidades añadidas o los bugs corregidos. Compruebe que el código esté limpio, documentado y que siga las prácticas de clean code.

#### 6. Ejecute los test y análisis de código

Antes de enviar sus modificaciones, ejecute todos los testeos para garantizar que todo esté funcionando correctamente.

```bash
./vendor/bin/phpunit
./vendor/bin/phpcs
./vendor/bin/phpstan --memory-limit=1g
```

#### 7. Haga el commit de los cambios

Escriba mensajes de commit claros y concisos. Use el siguiente modelo para mensajes de commit:

- `feat:` Para nuevas funcionalidades
- `fix:` Para corrección de bugs
- `docs:` Para cambios en la documentación
- `style:` Ajustes de formato y estilo
- `refactor:` Refactorización de código
- `test:` Adición o modificación de test

```bash
git commit -m "fix: corregido bug en la autenticación de usuarios"
```

#### 8. Envíe sus modificaciones
Envíe sus modificaciones para su repositorio GitHub:

```bash
git push origin mi-contribución
```

#### 9. Cree un Pull Request

En GitHub, vaya hasta su repositorio forkado y cliquee en New Pull Request. Describa claramente el cambio e incluya referencias a cualquier issue relacionada.

> Ejemplo de descripción: "Este PR resuelve el problema #123 e implementa la funcionalidad de login via autenticación OAuth."

### Normas de código

Para mantener un código consistente, siga estas normas de estilo:

- Use PSR-12 como estilo de formato en PHP.
- Nombre las variables y métodos de forma clara y descriptiva.
- Evite duplidos de código.
- Añada documentación para clases, métodos y funciones complejas.

### Revisión de Pull Request

Los administradores de NovoSGA revisarán su Pull Request y podrán sugerir cambios. Recuerde:

- Sea receptivo del feedback.
- Esté dispuesto a discutir su implementación.
