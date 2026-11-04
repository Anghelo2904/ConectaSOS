# ConectaSOS — versión instalable para iPhone (PWA)

## Cómo instalar en iPhone

1. **Publica esta carpeta completa** en un alojamiento HTTPS (por ejemplo, GitHub Pages, Netlify o Vercel). No basta con abrir `index.html` desde Archivos del iPhone.
2. Abre la URL pública en **Safari** del iPhone.
3. Toca **Compartir → Agregar a pantalla de inicio**. Activa **Abrir como app web** si aparece y pulsa **Agregar**.
4. Se instalará un icono llamado ConectaSOS. Ábrelo y crea tu cuenta de práctica.

## Mapa

- El mapa **dentro de la app** utiliza datos cartográficos reales de OpenStreetMap mediante Leaflet, y muestra zonas coloreadas para practicar la interpretación de alertas.
- La opción **Abrir Google Maps** abre el mapa de Valparaíso en una pestaña o app aparte. Las zonas de práctica de ConectaSOS no se transfieren a Google Maps.
- Integrar Google Maps **dentro** de la app, conservando las áreas coloreadas, requeriría la API de Google Maps, una clave propia y configurar facturación en Google Cloud. Para este proyecto estudiantil, el mapa incorporado ya cumple la función de visualizar zonas.
- El mapa requiere conexión a internet. El resto de la aplicación puede seguir funcionando parcialmente tras instalarse y cargarla por primera vez.

## Aviso importante

La cartografía muestra ciudades reales, pero los **riesgos, ubicaciones familiares y alertas no se obtienen de fuentes oficiales**. Son escenarios de práctica. Los mensajes no salen del dispositivo, y registro/contraseña se guardan en el navegador, sin servidor ni seguridad de producción. **No usar para solicitar auxilio ni para tomar decisiones en una emergencia.** No introducir información sensible ni contraseñas personales.

## Contenido

- `index.html`: aplicación completa con registro, inicio, alertas, contactos, mapa y chat de práctica.
- `manifest.webmanifest`: instalación como web app.
- `sw.js`: servicio para guardar archivos locales y permitir una carga parcial sin conexión.
- `icons/`: íconos iOS y PWA.

## Desarrollo local

Desde la carpeta ejecuta `python3 -m http.server 8000` y entra a `http://localhost:8000`. Para probar instalación en iPhone, utiliza un enlace **HTTPS** público.

## Personalización

En **Más → Apariencia y comodidad**, cada persona puede alternar entre tema azul oscuro y tema blanco, y reorganizar con flechas los accesos rápidos y las opciones del menú. Los cambios se guardan localmente en ese navegador mediante localStorage; no se sincronizan entre dispositivos. El botón «Restablecer diseño original» recupera los valores iniciales.
