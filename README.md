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

## Componentes

`index.html` contiene la aplicación. Las páginas públicas de información, privacidad, términos y soporte funcionan sin iniciar sesión. `worker/index.js` verifica sesiones, separa los mundos, limita la IA y valida los pagos. `database/launch.sql` contiene la actualización revisable de PostgreSQL y sus permisos.

El panel del operador se distribuye de forma privada, fuera de este repositorio. Sus operaciones requieren una cuenta administradora con segundo factor; conocer su dirección o el código público del servicio no concede acceso.

## Desarrollo y verificación

Requiere Node.js 24 o posterior. Instala las dependencias con `npm ci` y ejecuta `npm test`. Sirve los archivos por HTTP para las pruebas de interfaz; las funciones conectadas necesitan un entorno de Supabase y un Worker configurados. No uses datos ni credenciales de producción en pruebas locales.

Las pruebas incluidas comprueban sintaxis del cliente, autorización, restricciones infantiles, segundo factor, límites de entrada y firmas de notificaciones. No sustituyen una prueba integral de alta, recuperación de cuenta y pago con cuentas de prueba del proveedor.

## Despliegue

1. Revisar y probar la migración en una copia del esquema. Conservar un respaldo antes de aplicarla.
2. Configurar los secretos del Worker: `SUPABASE_URL`, `SUPABASE_SERVICE_KEY`, `MP_ACCESS_TOKEN`, `MP_WEBHOOK_SECRET` y `DEEPSEEK_KEY`. No publicarlos en GitHub. `MP_TEST_MODE=true` selecciona pagos de prueba.
3. Aplicar la migración y publicar el Worker junto con el cliente compatible, durante una ventana controlada.
4. Configurar en Supabase las URL de redirección autorizadas, el correo de autenticación y los factores de seguridad del operador.
5. Probar confirmación de correo, recuperación, salida de sesiones, separación de perfiles y cobros duplicados antes de habilitar promoción comercial.
6. Verificar la propiedad en Search Console y enviar `sitemap.xml`. Google decide cuándo rastrear e indexar cada página.

El cron del Worker elimina contadores antiguos y vence planes. Los secretos y la configuración de correo se administran en sus respectivos proveedores.

## Estado de esta versión

Preparación de lanzamiento en validación. La existencia del código no certifica que los servicios estén desplegados ni que un cobro real haya sido probado. El lanzamiento internacional, especialmente para menores, requiere verificar las obligaciones aplicables al operador y al mecanismo de consentimiento parental. Los avisos no prometen cumplimiento universal ni seguridad absoluta.

## Licencia y contacto

El código original se distribuye bajo la [licencia MIT](LICENSE). Esta licencia no cambia las licencias de dependencias, marcas o traducciones bíblicas de terceros.

Soporte y reportes de seguridad: **texthumanapp@gmail.com**. Consulta [SECURITY.md](SECURITY.md) para las reglas de seguridad del proyecto.
