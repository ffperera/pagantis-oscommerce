pagantis-oscommerce
================

Módulo de pago de pagantis.com para osCommerce (v.2.3.x)

## Instrucciones de Instalación

1. Crea tu cuenta en Pagantis.com si aún no la tienes [desde aquí](https://bo.pagantis.com/users/sign_up)
2. Descarga el módulo de [aquí](https://github.com/pagantis/pagantis-oscommerce/releases)
3. Instala el módulo en tu tienda oscommerce:

Sube los ficheros de la carpeta /catalog de este módulo, manteniendo la estructura de directorios. 

ext/modules/payment/pagantis/callback.php
includes/modules/payment/pagantis.php
includes/languages/espanol/modules/payment/pagantis.php
includes/languages/english/modules/payment/pagantis.php

Si tu tienda tiene más idiomas, copia el fichero de idiomas en la carpeta correspondiente y edítalo para ajustar los textos
includes/languages/OTRO_IDIOMA/modules/payment/pagantis.php


4. Desde el panel de osCommerce de tu tienda, accede a Modulos > Pago. Pulsa el botón Instalar Módulo y selecciona el módulo Pagantis.
5. Una vez instalado, selecciona el módulo Pagantis de la lista de módulos disponibles y pulsa Editar. 
6. Configura el código de cuenta y la clave de firma con la información de tu cuenta que encontrarás en [el panel de gestión de Pagantis](https://bo.pagantis.com/api). Ten en cuenta que para hacer cobros reales deberás activar tu cuenta de Pagantis.
7. MUY IMPORTANTE: Añade en [la sección de notificaciones HTTP](https://bo.pagantis.com/notifications) de Pagantis la URL de notificación de tu tienda. Puedes ver más abajo instrucciones para saber la URL de tu comercio.


## URLs de notificación

Para que los pedidos se completen y los pedidos cobrados a través de Pagantis aparezcan como pagados, debes indicar la URL de notificación en el backoffice de Pagantis, que se corresponde con la URL del fichero callback.php en tu tienda. 

Ejemplos:

- Si tu tienda está en el dominio http://www.mitienda.es, la URL será: http://www.mitienda.es/ext/modules/payment/pagantis/callback.php
- Si tu tienda está en el subdominio http://shop.midominio.com, la URL será: http://shop.mitienda.es/ext/modules/payment/pagantis/callback.php
- Si tu tienda está en la carpeta "catalog" del dominio http://www.midominio.com, la URL será: http://www.mitienda.es/catalog/ext/modules/payment/pagantis/callback.php


### Soporte

Si tienes alguna duda o pregunta no tienes más que escribirnos un email a [soporte.tpv@pagantis.com] o a través de Twitter a [@PagantisDev](https://twitter.com/PagantisDev)


### Release notes

#### 1.0.0

- Versión inicial
