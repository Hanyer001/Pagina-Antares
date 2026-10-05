# Página de Antares

Página oficial de presentación y descarga de Antares para Windows.

- **Sitio publicado:** https://hanyer001.github.io/Pagina-Antares/
- **Versión presentada:** 0.3.2.
- **Instalador:** 25,6 MB (25599036 bytes).
- **Código de la aplicación:** [Hanyer001/Antares](https://github.com/Hanyer001/Antares).
- **Descargas y actualizaciones:** [antares-actualizaciones](https://github.com/Hanyer001/antares-actualizaciones/releases/latest).

## Novedades de 0.3.2

La página refleja la corrección de los enlaces de audio y la extracción nativa de Windows con `rusty_ytdl`. La aplicación conserva yt-dlp para búsquedas y listas. Las funciones, los enlaces y el tamaño del instalador deben corresponder al código y al paquete publicados.

## Estructura

`index.html` es el archivo servido por GitHub Pages desde la raíz de la rama `main`. Contiene el HTML, el CSS y el JavaScript de la página; no necesita npm ni una compilación.

`landing-antares/index.html` conserva la copia de trabajo de la misma página. Al modificarla, sincroniza ambos archivos para evitar que se publique una versión diferente. `landing-antares/docs/` documenta el producto y el diseño.

## Descargas

Los botones apuntan a la dirección estable:

https://github.com/Hanyer001/antares-actualizaciones/releases/latest/download/Antares-Setup.exe

El JavaScript consulta la API pública de GitHub para mostrar la versión y el tamaño del instalador más reciente. Si la consulta no responde, utiliza los valores de respaldo de `CONFIG`, actualizados a 0.3.2 y 25,6 MB. Los valores de la sección de métricas también se actualizan con cada paquete.

## Revisar y publicar

1. Comprueba la release estable del repositorio de actualizaciones y el tamaño real de su `Antares-Setup.exe`.
2. Actualiza la versión, el tamaño y las notas visibles en los dos archivos HTML y en este README.
3. Abre `index.html` para revisar la página y prueba los enlaces de descarga y los elementos interactivos.
4. Sube los cambios a `main`; el despliegue de GitHub Pages publica el contenido de la raíz.
5. Comprueba el sitio publicado y que el botón descargue el instalador de la versión nueva.

Los instaladores y `latest.json` se publican como archivos de una release en `antares-actualizaciones`. Las claves de firma y las credenciales permanecen fuera de los repositorios.

Android se presenta como próxima incorporación: el sitio ofrece actualmente el instalador de Windows.
