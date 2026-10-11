# PWA Matemáticas · IES La Laboral

**Estado:** prototipo v0.1 · curso 2026–2027 · no aprobado como herramienta institucional.

## Qué hace

- Portada y navegación adaptadas a móviles.
- Editor de situaciones de aprendizaje por sentidos matemáticos.
- Registro de evidencias con criterio, producto e instrumento.
- Matrices criterio → evidencia y producto → criterio.
- Alertas de criterios registrados sin evidencia.
- Planes de refuerzo vinculados a dificultades y nuevas evidencias.
- Exportación/importación JSON, impresión a PDF desde el navegador.
- Manifest y service worker para instalación y uso básico sin conexión tras la primera visita.

## Publicar en Vercel

1. Descomprime el ZIP. Dentro verás `index.html`, `app.js`, `styles.css`, `manifest.webmanifest`, `sw.js`, `vercel.json` y `icons/`.
2. En GitHub, crea un repositorio **privado** y sube **el contenido de la carpeta**, conservando los archivos en la raíz del repositorio.
3. Accede a https://vercel.com/new, inicia sesión y elige **Import Git Repository**. Autoriza GitHub si te lo solicita y selecciona el repositorio.
4. En **Framework Preset** elige **Other** (sitio estático). No se necesita comando de compilación; deja **Build Command** vacío y **Output Directory** sin definir. Pulsa **Deploy**.
5. Vercel proporcionará una dirección `https://...vercel.app`. Ábrela en un navegador.
6. En Android (Chrome), usa el menú del navegador > **Instalar aplicación** o **Añadir a pantalla de inicio**. En iPhone (Safari), menú Compartir > **Añadir a pantalla de inicio**. La instalación depende del navegador y del sistema operativo.

**Importante:** el repositorio privado no convierte automáticamente la URL publicada en privada. No subas documentos sensibles ni datos personales.

## Pruebas recomendadas

- Abrir en ordenador y móvil.
- Crear situación con códigos de prueba (no usar códigos ficticios como oficiales).
- Crear una evidencia vinculada a un criterio y comprobar las dos matrices.
- Crear un plan de refuerzo y cerrarlo.
- Descargar una copia JSON, importarla en otro navegador y comprobar los datos.
- Tras la primera carga, desconectar Internet y volver a abrir la aplicación para comprobar la caché local.
- Verificar la instalación PWA en el navegador elegido.

## Límites y seguridad

- Los datos se guardan en `localStorage` del navegador. **No hay cuentas, servidor, sincronización, copias automáticas ni control de acceso**.
- Cada docente tendrá sus propios datos; el enlace no comparte las fichas creadas.
- No introducir nombres, calificaciones, expedientes ni información personal del alumnado.
- No hay integración con Moodle ni Google Drive, ni consulta curricular automática.
- Los documentos oficiales y acuerdos deben verificarse y aprobarse por los órganos correspondientes.
- Antes de usarla como aplicación institucional hay que estudiar alojamiento, condiciones de servicio, accesibilidad, protección de datos, autenticación y almacenamiento autorizado.

## Actualizaciones

Modifica los archivos del repositorio; Vercel volverá a desplegar la versión actualizada. Si se cambia la lógica de caché del service worker, incrementa el nombre `CACHE` en `sw.js`.
