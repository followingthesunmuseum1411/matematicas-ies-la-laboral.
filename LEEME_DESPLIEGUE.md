# PWA generadora de cuadernillos · IES La Laboral

**Versión 0.4 · Groq (modalidad gratuita con límites)**. Código preparado; **no desplegado ni probado con una clave real**. No se garantiza gratuidad ilimitada ni disponibilidad permanente del plan gratuito.

## Instalación en el GitHub y Vercel ya existentes

1. Descomprimir el ZIP. Subir a la raíz del repositorio los archivos `index.html`, `styles.css`, `app.js`, `manifest.webmanifest`, `sw.js` y la carpeta `api/generate.js`, conservando las rutas. El repositorio es público: **nunca subir claves**.
2. En GroqCloud, crear una clave API en la modalidad gratuita disponible, **sin activar facturación de pago**. Revisar las condiciones vigentes del proveedor, especialmente privacidad y límites.
3. En Vercel > proyecto > Settings > Environment Variables, añadir `GROQ_API_KEY` con esa clave, y `GENERATOR_ACCESS_CODE` con un código largo privado para los docentes. Opcional: `GROQ_MODEL` (por defecto `llama-3.3-70b-versatile`; sujeto a disponibilidad). No configurar `OPENAI_API_KEY`.
4. Volver a desplegar en Vercel. Probar primero con una situación ficticia sin datos personales y 3-4 sesiones. Si el proveedor devuelve error por límite de uso, esperar o usar «Generar borrador sin IA».
5. Revisar todos los cálculos, soluciones, criterios, correspondencia de evidencias e instrumentos y la adecuación didáctica. El cuadernillo se imprime/guarda como PDF desde el navegador; el solucionario docente se descarga por separado.

## Límites y protección

- El profesorado **no necesita cuenta ni clave de API propia**; usa un código de acceso compartido. El administrador debe crear la cuenta gratuita del proveedor y mantener su clave privada en Vercel.
- Un plan gratuito **puede limitar solicitudes y tokens**, rechazar generaciones extensas o cambiar sus condiciones. No hay promesa de servicio gratuito ilimitado. El código de acceso compartido no constituye autenticación fuerte ni una cuota por docente. Antes de abrir a un grupo amplio conviene añadir control de acceso y límites de solicitudes.
- No se introducen **nunca datos personales** ni información interna sensible en las plantillas. La aplicación envía el contenido curricular a Groq para generar el texto: verificar la política del proveedor y la autorización institucional antes del uso ordinario.
- La importación automática admite DOCX, TXT, MD y JSON; no PDF directamente. La lectura DOCX requiere una biblioteca externa. La extracción es orientativa.
- La IA produce un borrador: puede equivocarse en cálculos, no justificar correctamente un criterio o dejar secciones incompletas. Los criterios que no coincidan exactamente con los transcritos en la plantilla se marcan «PENDIENTE DE VALIDACIÓN».
- EVAGD: genera textos de tareas para copiar, no publica automáticamente.
- **No se ha verificado todavía un despliegue ni una generación real**.
