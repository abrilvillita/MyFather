# MyFather

Aprendizaje bíblico en español e inglés con lecciones, actividades y espacios separados para personas adultas y perfiles infantiles supervisados.

[Sitio web](https://myfather.app) · [Privacidad](https://myfather.app/privacy.html) · [Términos](https://myfather.app/terms.html) · [Soporte](https://myfather.app/support.html)

## Funcionamiento

- Las lecciones y actividades habituales no necesitan IA. El chat comienza en **Nada de IA**; las personas adultas pueden elegir **Poca IA** o **IA**. Los perfiles infantiles no envían preguntas al proveedor de IA.
- Entrar a un perfil infantil bloquea esa sesión en el servidor. Para volver al espacio adulto hay que cerrar sesión y autenticarse de nuevo. El servidor comprueba también las solicitudes directas.
- La finalización de lecciones guarda progreso y entrega una recompensa una sola vez. Los días de aprendizaje se calculan usando la zona horaria elegida al comenzar.
- Los precios de referencia se muestran en USD. Antes de continuar a Mercado Pago se muestra el importe concreto en MXN y la fecha del tipo de cambio. Los planes duran 30 días y no tienen renovación automática.
- La tienda habilitada vende mensajes adicionales. Los artículos sin efecto implementado no están disponibles para comprar.
- La ubicación es opcional: el navegador ordena las iglesias aprobadas sin enviar las coordenadas personales a MyFather.

## Archivos de este repositorio

Este repositorio contiene únicamente el sitio público: la aplicación en `index.html`, sus páginas informativas, imágenes, configuración de dominio y archivos para buscadores.

El Worker se administra en Cloudflare. Las migraciones de Supabase, pruebas del servidor y herramientas de operación se conservan por separado. El panel administrativo es privado y no se distribuye aquí. Sus operaciones requieren autorización en el servidor y segundo factor.

## Publicación

Los archivos estáticos se sirven por HTTPS en myfather.app. El cliente necesita un Worker y un proyecto de Supabase compatibles, configurados por el operador. Ninguna clave de servicio, clave de pago ni credencial de administración pertenece a este repositorio.

Antes de publicar una versión hay que comprobar la confirmación de correo, recuperación de contraseña, separación de perfiles y validación de pagos en los servicios privados. La verificación de Search Console y el envío del sitemap permiten solicitar el rastreo; Google decide cuándo indexar las páginas.

## Estado de esta versión

Preparación de lanzamiento en validación. La existencia del código no certifica que los servicios estén desplegados ni que un cobro real haya sido probado. El lanzamiento internacional, especialmente para menores, requiere verificar las obligaciones aplicables al operador y al mecanismo de consentimiento parental. Los avisos no prometen cumplimiento universal ni seguridad absoluta.

## Licencia y contacto

El código original se distribuye bajo la [licencia MIT](LICENSE). Esta licencia no cambia las licencias de dependencias, marcas o traducciones bíblicas de terceros.

Soporte y reportes de seguridad: **texthumanapp@gmail.com**. Consulta [SECURITY.md](SECURITY.md) para las reglas de seguridad del proyecto.
