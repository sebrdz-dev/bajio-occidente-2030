# BAJÍO-OCCIDENTE 2030 — Paquete web universal

Versión exportada: 7 de noviembre de 2026. Sitio estático en español de Bajío Ventures y Fundación Konrad Adenauer. **No depende de un dominio específico**: puede instalarse en un dominio propio o en cualquier subdirectorio de un alojamiento web que sirva HTML y archivos estáticos.

## 1. ¿Dónde puedo publicarlo?

Ejemplos válidos:

- `https://www.kithub.mx/bajio-occidente-2030/`
- `https://www.bajiooccidente.com/` (si el dominio completo se destina al evento)
- `https://www.bajiooccidente.com/foro/`
- `https://www.bajioventures.com/bajio-occidente-2030/`

**El mismo ZIP funciona en cualquiera de esas opciones**, siempre que `index.html` y `assets/` permanezcan juntos en el mismo directorio. Las rutas de imágenes y logotipos son relativas. No hay que modificar el código para cambiar de dominio o carpeta.

## 2. Qué contiene el paquete

```text
bajio-occidente-2030/
├── index.html
├── README-INSTALACION.md
└── assets/
    ├── logo-bajio-ventures.svg
    ├── logo-kas.svg
    ├── guanajuato-dusk.webp
    ├── eje-energia.webp
    ├── eje-industria.webp
    ├── eje-talento.webp
    ├── eje-innovacion-metaverso.webp
    ├── eje-cooperacion-internacional.webp
    ├── flyer-oficial.webp
    └── flyer-oficial.png
```

El diseño, los estilos y la interacción están integrados en `index.html`. No se necesitan Node.js, compilación, base de datos ni otras dependencias para servir este sitio. La tipografía carga desde Google Fonts cuando hay conexión a Internet; existen fuentes alternativas del sistema.

## 3. Instalación en un hosting con cPanel / administrador de archivos / FTP

1. Abre el administrador de archivos o FTP del alojamiento web del dominio que elijas. Identifica su carpeta pública (a menudo `public_html/`, `httpdocs/` o `www/`; varía según el proveedor).
2. Decide si el evento vivirá en la **raíz del dominio** o en una **subcarpeta**. Si ya existe un sitio, usa una subcarpeta para no sobrescribir su página principal.
3. Extrae **el contenido** de este ZIP en esa ubicación: `index.html` y la carpeta `assets/` deben quedar directamente ahí, al mismo nivel. Evita una carpeta duplicada adicional.
4. Abre la URL definitiva y comprueba que carguen el encabezado, los cinco ejes, el cartel, los logotipos y los botones.
5. Prueba el sitio en computadora y móvil; verifica las acciones de navegación, el enlace de registro y la ampliación del cartel.
6. Si tenías una versión previa, reemplaza los archivos del directorio del evento y limpia la caché del navegador/CDN si sigues viendo el diseño anterior.

## 4. Si la web de destino usa WordPress, Wix, Webflow u otro CMS

Este es un sitio HTML independiente. **No basta con subir el ZIP a la biblioteca de medios de WordPress ni a un editor visual:** esas funciones no siempre permiten publicar HTML, CSS y JavaScript arbitrarios. El administrador o proveedor de hosting debe instalar el contenido en el directorio público del dominio, o adaptar el diseño a una plantilla/componente compatible con el CMS. El paquete sí funciona sin adaptación en un hosting estático o servidor web convencional.

## 5. Enlaces y funciones que ya están configurados

- Registro y confirmación de asistencia: `https://luma.com/frr99igb` (servicio externo; no hay formulario ni base de datos en este paquete).
- Cómo llegar: enlace externo de Google Maps.
- Guardar la fecha: enlace externo de Google Calendar.
- Contacto: `german@bajioinvest.com`.
- Las imágenes están empaquetadas localmente en `assets/`, incluida la imagen de **Innovación educativa** con realidad mixta y gemelos digitales.

## 6. Ajustes opcionales de SEO y vista previa al compartir

El sitio está configurado **sin una dirección canónica fija** para poder reutilizarse en varios dominios. El cartel de redes sociales se indica en `og:image` mediante ruta relativa, que funciona para encontrar el archivo dentro del sitio, pero **algunas redes sociales exigen una URL absoluta** para mostrar una miniatura enriquecida.

Cuando elijas el dominio principal definitivo, puedes mejorar las vistas previas en redes y evitar contenido duplicado si:

1. Cambias `og:image` en `index.html` por la URL HTTPS completa del archivo, por ejemplo `https://www.bajiooccidente.com/assets/flyer-oficial.png` (si lo publicas en la raíz de ese dominio).
2. Añades, si lo deseas, `<meta property="og:url" content="https://TU-DOMINIO-Y-RUTA/">`.
3. Añades, si lo deseas, `<link rel="canonical" href="https://TU-DOMINIO-Y-RUTA/">` para indicar cuál será la versión principal si publicas copias en diferentes dominios.

**Estos cambios son opcionales para que la página funcione.** Son recomendables cuando decidas cuál será la URL pública principal.

## 7. Verificación antes de anunciar la página

- Validar fecha, dirección, horario y programa final del evento.
- Confirmar que el registro en Luma permanezca abierto y con los recordatorios deseados.
- Verificar que el sitio esté servido por **HTTPS** y que los logotipos cuenten con autorización de las organizaciones.
- Si se publica en dos dominios, elegir un dominio principal para difundir el enlace y, de ser necesario, redirigir el otro o configurar la dirección canónica.

## 8. Mantenimiento

Para cambiar textos, enlaces o secciones, edita `index.html`. Para cambiar una imagen, reemplaza el archivo correspondiente de `assets/` o actualiza su ruta dentro del HTML. Conserva los nombres y la estructura de directorios. Cuando hagas una nueva publicación, comprueba el resultado después de limpiar la caché.

Este paquete **no modifica** la web oficial ni publica archivos automáticamente. Está listo para subirlo con las credenciales y el procedimiento de tu hosting.
