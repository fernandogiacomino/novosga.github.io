# Configuración

Por defecto Novo SGA viene con un archivo llamado `config/app.default.php` donde estan las configuraciones básicas del sistema. Para personalizar algún valor o añadir nuevas configuraciones cree una copia del archivo default renombrándolo `config/app.php`.

!> Nunca modifique directamente el archivo `app.default.php`. En caso de futuras atualizaciones ese archivo será sobrescrito y se perderán sus modificaciones.

```php
<?php

use Novosga\Entity\Unidade;
use Novosga\Entity\Usuario;

return [
    'queue' => [
        /**
         * Queue ordering
         * @param Unidade $unidade
         * @param Usuario $usuario (optional)
         * @return array
         */
        'ordering' =>  function (Unidade $unidade, Usuario $usuario = null) {
            $ordering = [];

            if ($usuario) {
                // peso servico x usuario
                $ordering[] = [
                    'exp' => 'servicoUsuario.peso',
                    'order' => 'DESC',
                ];
            }

            return array_merge($ordering, [
                // priority
                [
                    'exp'   => 'prioridade.peso',
                    'order' => 'DESC',
                ],
                // peso servico x unidade
                [
                    'exp'   => 'servicoUnidade.peso',
                    'order' => 'DESC',
                ],
                // dataChegada
                [
                    'exp'   => 'atendimento.dataChegada',
                    'order' => 'ASC',
                ]
            ]);
        },
    ]
];
```
