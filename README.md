Informe de recorrido
Aplicación web instalable (PWA) para llevar el informe de un recorrido de patrullaje. Se arma la ruta tocando puntos en un mapa, se llenan los datos del recorrido y todo se exporta en una sola imagen JPG.
Funciones
Datos del recorrido: fecha, hora, cantón, distrito, unidad patrulla, oficial chofer y oficiales asistentes (se pueden agregar los que hagan falta).
Mapa de la ruta: al tocar el mapa se agregan puntos numerados y se dibuja la ruta. Muestra la cantidad de puntos y los kilómetros totales.
Arrastrar un punto lo mueve.
Deshacer el último punto.
Borrar toda la ruta.
Botón para ir a la ubicación actual.
Anotaciones: campo grande de texto libre.
Exportar a JPG: genera una imagen con los datos, el mapa con la ruta y las anotaciones. Se puede guardar o compartir (si el aparato lo permite).
Guardado automático: la información se conserva en el aparato aunque se cierre la app.
Informe nuevo: limpia todo para empezar otro recorrido.
Archivos
Archivo
Para qué sirve
index.html
La aplicación completa (diseño y lógica)
manifest.webmanifest
Datos para instalarla como app (nombre, colores, íconos)
sw.js
Service worker: permite abrirla sin conexión
icon-192.png, icon-512.png
Íconos de la app
README.md
Este documento
Instalación
La app se publica con GitHub Pages:
Subir todos los archivos a un repositorio público, sueltos en la raíz.
En Settings > Pages, elegir Deploy from a branch, rama main, carpeta / (root).
Abrir el enlace https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/.
Instalar:
Android (Chrome): menú ⋮ > Instalar app.
iPhone (Safari): Compartir > Agregar a inicio.
Abrir la app una vez con internet para que guarde lo necesario.
Uso
Llenar los datos del recorrido. La fecha y la hora se llenan solas con el momento actual y se pueden cambiar.
Tocar el mapa en el orden del recorrido para armar la ruta. El primer punto es verde y el último rojo.
Escribir las anotaciones.
Tocar Guardar JPG (o Compartir) para obtener la imagen del informe.
Limitaciones
El mapa usa mosaicos de OpenStreetMap, por lo que se necesita internet para ver zonas nuevas y para exportar el JPG con el mapa. Sin conexión funcionan los formularios y las zonas del mapa ya visitadas.
Los informes se guardan solo en el aparato donde se llenan, no en un servidor. Solo se conserva el informe actual; al empezar uno nuevo se borra el anterior, por eso conviene exportar el JPG antes.
Cambiar de navegador o borrar los datos del sitio elimina el informe guardado.
Tecnología
HTML, CSS y JavaScript sin dependencias de instalación.
Leaflet 1.9.4 para el mapa.
Mapa base © OpenStreetMap contributors.
Actualizar la app
Subir al repositorio el archivo modificado con el mismo nombre. Si no se ven los cambios, cerrar y abrir la app dos veces. Si se cambia mucho el contenido, conviene editar CACHE en sw.js (por ejemplo, de recorrido-v1 a recorrido-v2) para forzar la actualización.
